# 两台服务器搭建tendermint+ethermint+geth网络

## 准备工作

创建服务器

服务器1的公网地址：IP1，在服务器1上运行tendermint和geth。

服务器2的公网地址：IP2,在服务器2上运行ethermint。

编译tendermint、ethermint和geth

源码编译的步骤省略。本文以tendermint 0.10.5-acc161f7,ethermint 0.5.3-deb7883和geth 1.6.7-stable的版本演示。

推荐分别将它们加入到PATH中。我们可以通过tendermint help和ethermint help查看它们的用法。

## 初始化tendermint和ethermint

初始化tendermint

    tendermint init --home ~/tmdata

    --home:指定tendermint的数据目录

初始化ethermint

    ethermint --datadir ~/.ethermint init
    --datadir：指定ethermint的数据目录

### 修改配置文件

cd ～/tmdata

vim config.toml

    # This is a TOML config file.
    # For more information, see https://github.com/toml-lang/toml
    
    #proxy_app = "tcp://127.0.0.1:46658"
    proxy_app="tcp://IP2:46658"      #这里添加IP2的地址，tendermint中默认的地址是127.0.0.1
    moniker = "anonymous"
    fast_sync = true
    db_backend = "leveldb"
    log_level = "state:info,*:error"
    
    [rpc]
    laddr = "tcp://0.0.0.0:46657"
    
    [p2p]
    laddr = "tcp://0.0.0.0:46656"
    seeds = ""


注意：在一台机器上启动tendermint+ethermint+geth，不用修改配置文件。但是在多台机器上就得修改，不然tendermint会打印如下的日志：

    E[05-14|03:32:26.653] abci.socketClient failed to connect to tcp://47.75.188.184:46658.  Retrying... module=abci-client connection=query
     
     
### 启动tendermint和ethermint

启动顺序遵循先tendermint后ethermint。

启动tendermint

    tendermint node --home ~/tmdata

启动ethermint

    ethermint --datadir ~/.ethermint --rpc --rpcaddr=0.0.0.0 --ws --wsaddr=0.0.0.0 --rpcapi eth,net,web3,personal,admin  --tendermint_addr="tcp://IP1:46657"

好，至此，tendermint+ethermint连通。

启动geth

我们通过把geth关联到运行的ethermint上（geth和ethermint运行在不同的机器上）：
    
    geth  attach http://IP2:8545

注意：若geth和ethermint运行在一台机器上，关联命令是：

    geth  attach http://localhost:8545

## 关闭ethermint和tendermint

关闭的时候比较讲究，需要先停掉ethermint，再停掉ethermint。否则，重启tendermint会crash。

## 再启动ethermint和tendermint

首先启动tendermint，再次启动ethermint。否则，tendermint程序会crash。


## 注意事项

1、需要打开上面涉及的所有tcp端口号（包括入和出）




