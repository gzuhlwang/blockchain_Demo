## 安装go
注意go的版本。
## 克隆代码

    #mkdir -p $GOPATH/src/github.com/cosmos && cd $GOPATH/src/github.com/cosmos    
    #git clone -b v0.15.0 https://github.com/cosmos/cosmos-sdk 
我们克隆v0.15.0的代码进行编译。v0.15.0的代码依赖tendermint v0.19.0。这一点我们可以在Gopkg.toml中找到依据。

##  编译安装
    #cd cosmos-sdk
    #make get_vendor_deps   //这一步需要下载依赖管理工具dep
    #make install
    #make install_examples
这一步得学会科学上网。否则第二步就会让你放弃。

so far，gaiad和gaiacli及四个例子（分别是basecoind，basecli，democoind和democli）会被安装。这六个可执行程序可以在$GOPATH/bin下面找到。

## 验证安装是否成功 

    #gaiad version
     0.15.0-07842b6
    #gaiacli version
     0.15.0-07842b6

## 用法

    #gaiad help
    Gaia Daemon (server)
    
    Usage:
      gaiad [command]
    
    Available Commands:
      help             Help about any command
      init             Initialize genesis files
      show_node_id     Show this node's ID
      show_validator   Show this node's validator info
      start            Run the full node
      unsafe_reset_all Reset all blockchain data
      version          Print the app version
    
    Flags:
      -h, --help               help for gaiad
          --home string        directory for config and data (default "/root/.gaiad")
          --log_level string   Log level (default "main:info,state:info,*:error")
          --trace              print out full stack trace on errors
    
    Use "gaiad [command] --help" for more information about a command.
每一个版本的子命令列表或许有出入，仔细阅读这个子命令的用法对一个新手来说会少走很多弯路。
    
    # gaiacli help
    Gaia light-client
    
    Usage:
      gaiacli [command]
    
    Available Commands:
      init         Initialize light client
      status       Query remote node for status
      block        Get verified data for a the block at given height
      validatorset Get the full validator set at given height
    
      txs          Search for all transactions that match the given tags
      tx           Matches this txhash over all committed blocks
    
      account      Query account balance
      send         Create and sign a send tx
      transfer
      relay
      bond         Bond to a validator
      unbond       Unbond from a validator
    
      rest-server  Start LCD (light-client daemon), a local REST server
      keys         Add or view local private keys
    
      version      Print the app version
      help         Help about any command
    
    Flags:
      -e, --encoding string   Binary encoding (hex|b64|btc) (default "hex")
      -h, --help              help for gaiacli
          --home string       directory for config and data (default "/root/.gaiacli")
      -o, --output string     Output format (text|json) (default "text")
          --trace             print out full stack trace on errors
    
    Use "gaiacli [command] --help" for more information about a command.
    
## 搭建测试网（1个validator+1个非validator）

### 初始化节点
    
    # gaiad init  --home=$HOME/.gaiad1
    
    # cd $HOME/.gaiad1 && tree
    |-- config
    |   |-- config.toml
    |   |-- genesis.json
    |   |-- node_key.json
    |   `-- priv_validator.json
    `-- data
    # gaiad init  --home=$HOME/.gaiad2    #独立的数据目录
    # cp $HOME/.gaiad1/config/genesis.json $HOME/.gaiad2/config/genesis.json   //共享一个genesis.json
    
修改节点2的配置文件
    
    # This is a TOML config file.
    # For more information, see https://github.com/toml-lang/toml
    
    ##### main base config options #####
    
    # TCP or UNIX socket address of the ABCI application,
    # or the name of an ABCI application compiled in with the Tendermint binary
    #proxy_app = "tcp://127.0.0.1:46658"
    proxy_app = "tcp://127.0.0.1:46668"
    
    # A custom human readable name for this node
    moniker = "gaiad2"
    
    # If this node is many blocks behind the tip of the chain, FastSync
    # allows them to catchup quickly by downloading blocks in parallel
    # and verifying their commits
    fast_sync = true
    
    # Database backend: leveldb | memdb
    db_backend = "leveldb"
    
    # Database directory
    db_path = "data"
    
    # Output level for logging, including package level options
    log_level = "main:info,state:info,*:error"
    
   
    [rpc]
    
    # TCP or UNIX socket address for the RPC server to listen on
    #laddr = "tcp://0.0.0.0:46657"
    laddr="tcp://0.0.0.0:46667"      #同一台机器上启多个进程，会报端口占用
    
   
    ##### peer to peer configuration options #####
    [p2p]
    
    # Address to listen for incoming connections
    #laddr = "tcp://0.0.0.0:46656"
    laddr="tcp://0.0.0.0:46666"       #同上
    
    # Comma separated list of seed nodes to connect to
    #seeds = ""
    seeds="81c8c6b270e86bcfa27a270906feb90f72838cfa@0.0.0.0:46656"   #这个地方的格式是ID@IP:port,新版本的tendermint采用这种形式，其中ID可以用gaiad show_node_id --home=$HOME/.gaiad1获得
若在多台机器上分别启node，就不用修改这里！
    
### 启动node   

    gaia start --home=$HOME/.gaia1
    gaia start --home=$HOME/.gaia2    #新开一个终端

### 一些操作

查询账户

    #gaiacli account 9B35301CCE4920D68D1466335852A3BF7FC21695
    其中的地址为validator的地址。
    
    {
          "type": "16542275FBFAB8",
          "value": {
            "BaseAccount": {
              "address": "9B35301CCE4920D68D1466335852A3BF7FC21695",
              "coins": [
                {
                  "denom": "mycoin",
                  "amount": 9007199254740992
                }
              ],
              "public_key": null,
              "sequence": 0
            },
            "name": ""
          }
        }
        
    #curl localhost:46657/validators
    
    {
      "jsonrpc": "2.0",
      "id": "",
      "result": {
        "block_height": 160,
        "validators": [
          {
            "address": "573BA4FEE9167FB1416A5B31158CEBC4426426B8",
            "pub_key": {
              "type": "AC26791624DE60",
              "value": "cApdn9ZAHajfQl+nChMoxeM1WioQgdOayYEJaslCTk4="
            },
            "voting_power": 10,
            "accum": 0
          }
        ]
      }
    }
    
    #cat  $HOME/.gaiad1/config/priv_validators.json
    
    {
    	"address": "573BA4FEE9167FB1416A5B31158CEBC4426426B8",
    	"pub_key": {
    		"type": "AC26791624DE60",
    		"value": "cApdn9ZAHajfQl+nChMoxeM1WioQgdOayYEJaslCTk4="
    	},
    	"last_height": 165,
    	"last_round": 0,
    	"last_step": 3,
    	"last_signature": {
    		"type": "6BF5903DA1DB28",
    		"value": "ni2aVku0oWqGL7pzfeFx+xDDWPoUz/iEYB/Wy54h6mR5oaiETDLyBofX3CUEkNSGbQ72ayWtnWJQfzGP+0OOAg=="
    	},
    	"last_signbytes": "7B2240636861696E5F6964223A22746573742D636861696E2D436536374B45222C224074797065223A22766F7465222C22626C6F636B5F6964223A7B2268617368223A2241303931333839343842324239463831363632454530353232443145343637353542303230434138222C227061727473223A7B2268617368223A2238363037363132424646453532463834383641443845353846354642414346374443374442333941222C22746F74616C223A317D7D2C22686569676874223A3136352C22726F756E64223A302C2274696D657374616D70223A22323031382D30352D31355430363A34333A33312E3433355A222C2274797065223A327D",
    	"priv_key": {
    		"type": "954568A3288910",
    		"value": "095Z4ZJEb2rnJzJxyonEQyp0aunNxVBAzFYm9H8fxOpwCl2f1kAdqN9CX6cKEyjF4zVaKhCB05rJgQlqyUJOTg=="
    	}
    }
    
    pk和address一致！
    
## 总结

本文从0开始完成了安装cosmos sdk，再搭建两个节点的测试网。