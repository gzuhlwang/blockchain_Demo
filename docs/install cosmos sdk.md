## 安装go
注意go的版本。
## 克隆代码

    #mkdir -p $GOPATH/src/github.com/cosmos && cd $GOPATH/src/github.com/cosmos    
    #git clone -b v0.15.0 https://github.com/cosmos/cosmos-sdk &
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
    
## 搭建测试网