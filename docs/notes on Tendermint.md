# Tendermint

    1、弱同步共识算法

    2、PoS-based BFT 
    
    3、微服务架构
    
    4、lay the foundation of casper and other project(Polkadot)  
    

# Ethermint explorer

    Any Ethereum explorer works!
    
    
# tendermint + ethermint

    Q:panic: Tendermint state.AppHash does not match AppHash after replay. Got 56E81F171BCC55A6FF8345E692C0F86E5B48E01B996CADC001622FB5E363B421, expected ...
    A: It is WAL replay problem! If you would like to know why,shoud look source code. 
    
    
# 基于tendermint开发，需要实现下列接口？
    
    path:github.com/tendermint/abci/types/application.go
    
    // Application is an interface that enables any finite, deterministic state machine
    // to be driven by a blockchain-based replication engine via the ABCI.
    // All methods take a RequestXxx argument and return a ResponseXxx argument,
    // except CheckTx/DeliverTx, which take `tx []byte`, and `Commit`, which takes nothing.
    type Application interface {
    	// Info/Query Connection
    	Info(RequestInfo) ResponseInfo                // Return application info
    	SetOption(RequestSetOption) ResponseSetOption // Set application option
    	Query(RequestQuery) ResponseQuery             // Query for state
    
    	// Mempool Connection
    	CheckTx(tx []byte) ResponseCheckTx // Validate a tx for the mempool
    
    	// Consensus Connection
    	InitChain(RequestInitChain) ResponseInitChain    // Initialize blockchain with validators and other info from TendermintCore
    	BeginBlock(RequestBeginBlock) ResponseBeginBlock // Signals the beginning of a block
    	DeliverTx(tx []byte) ResponseDeliverTx           // Deliver a tx for full processing
    	EndBlock(RequestEndBlock) ResponseEndBlock       // Signals the end of a block, returns changes to the validator set
    	Commit() ResponseCommit                          // Commit the state and return the application Merkle root hash
    }