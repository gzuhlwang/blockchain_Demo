
tm@node1:~/tmdata/config# tendermint --home ~/tmdata  --consensus.create_empty_blocks=true node --proxy_app=kvstore
I[05-08|08:57:11.126] Starting multiAppConn                        module=proxy impl=multiAppConn

## 进入/proxy/multi_app_conn.go#OnStart的逻辑
I[05-08|08:57:11.126] Starting localClient                         module=abci-client connection=query impl=localClient
I[05-08|08:57:11.126] Starting localClient                         module=abci-client connection=mempool impl=localClient
I[05-08|08:57:11.126] Starting localClient                         module=abci-client connection=consensus impl=localClient

##进入/consensus/replay.go#Handshake的逻辑
I[05-08|08:57:11.126] ABCI Handshake                               module=consensus appHeight=0 appHash=

## 进入/consensus/replay.go#Replay的逻辑
I[05-08|08:57:11.126] ABCI Replay Blocks                           module=consensus appHeight=0 storeHeight=39 stateHeight=39

##进入/consensus/replay.go#replayBlocks的逻辑
I[05-08|08:57:11.126] Applying block                               module=consensus height=1
I[05-08|08:57:11.126] Executed block                               module=consensus height=1 validTxs=0 invalidTxs=0
I[05-08|08:57:11.126] Applying block                               module=consensus height=2
I[05-08|08:57:11.126] Executed block                               module=consensus height=2 validTxs=0 invalidTxs=0
I[05-08|08:57:11.126] Applying block                               module=consensus height=3
I[05-08|08:57:11.126] Executed block                               module=consensus height=3 validTxs=0 invalidTxs=0
I[05-08|08:57:11.126] Applying block                               module=consensus height=4
I[05-08|08:57:11.127] Executed block                               module=consensus height=4 validTxs=0 invalidTxs=0
I[05-08|08:57:11.127] Applying block                               module=consensus height=5
I[05-08|08:57:11.127] Executed block                               module=consensus height=5 validTxs=0 invalidTxs=0
I[05-08|08:57:11.127] Applying block                               module=consensus height=6
I[05-08|08:57:11.127] Executed block                               module=consensus height=6 validTxs=0 invalidTxs=0
I[05-08|08:57:11.127] Applying block                               module=consensus height=7
I[05-08|08:57:11.127] Executed block                               module=consensus height=7 validTxs=0 invalidTxs=0
I[05-08|08:57:11.127] Applying block                               module=consensus height=8
I[05-08|08:57:11.127] Executed block                               module=consensus height=8 validTxs=0 invalidTxs=0
I[05-08|08:57:11.127] Applying block                               module=consensus height=9
I[05-08|08:57:11.127] Executed block                               module=consensus height=9 validTxs=0 invalidTxs=0
I[05-08|08:57:11.127] Applying block                               module=consensus height=10
I[05-08|08:57:11.128] Executed block                               module=consensus height=10 validTxs=0 invalidTxs=0
I[05-08|08:57:11.128] Applying block                               module=consensus height=11
I[05-08|08:57:11.128] Executed block                               module=consensus height=11 validTxs=0 invalidTxs=0
I[05-08|08:57:11.128] Applying block                               module=consensus height=12
I[05-08|08:57:11.128] Executed block                               module=consensus height=12 validTxs=0 invalidTxs=0
I[05-08|08:57:11.128] Applying block                               module=consensus height=13
I[05-08|08:57:11.128] Executed block                               module=consensus height=13 validTxs=0 invalidTxs=0
I[05-08|08:57:11.128] Applying block                               module=consensus height=14
I[05-08|08:57:11.128] Executed block                               module=consensus height=14 validTxs=0 invalidTxs=0
I[05-08|08:57:11.128] Applying block                               module=consensus height=15
I[05-08|08:57:11.128] Executed block                               module=consensus height=15 validTxs=0 invalidTxs=0
I[05-08|08:57:11.128] Applying block                               module=consensus height=16
I[05-08|08:57:11.129] Executed block                               module=consensus height=16 validTxs=0 invalidTxs=0
I[05-08|08:57:11.129] Applying block                               module=consensus height=17
I[05-08|08:57:11.129] Executed block                               module=consensus height=17 validTxs=0 invalidTxs=0
I[05-08|08:57:11.129] Applying block                               module=consensus height=18
I[05-08|08:57:11.129] Executed block                               module=consensus height=18 validTxs=0 invalidTxs=0
I[05-08|08:57:11.129] Applying block                               module=consensus height=19
I[05-08|08:57:11.129] Executed block                               module=consensus height=19 validTxs=0 invalidTxs=0
I[05-08|08:57:11.129] Applying block                               module=consensus height=20
I[05-08|08:57:11.129] Executed block                               module=consensus height=20 validTxs=0 invalidTxs=0
I[05-08|08:57:11.129] Applying block                               module=consensus height=21
I[05-08|08:57:11.129] Executed block                               module=consensus height=21 validTxs=0 invalidTxs=0
I[05-08|08:57:11.129] Applying block                               module=consensus height=22
I[05-08|08:57:11.129] Executed block                               module=consensus height=22 validTxs=0 invalidTxs=0
I[05-08|08:57:11.130] Applying block                               module=consensus height=23
I[05-08|08:57:11.130] Executed block                               module=consensus height=23 validTxs=0 invalidTxs=0
I[05-08|08:57:11.130] Applying block                               module=consensus height=24
I[05-08|08:57:11.130] Executed block                               module=consensus height=24 validTxs=0 invalidTxs=0
I[05-08|08:57:11.130] Applying block                               module=consensus height=25
I[05-08|08:57:11.130] Executed block                               module=consensus height=25 validTxs=0 invalidTxs=0
I[05-08|08:57:11.130] Applying block                               module=consensus height=26
I[05-08|08:57:11.130] Executed block                               module=consensus height=26 validTxs=0 invalidTxs=0
I[05-08|08:57:11.130] Applying block                               module=consensus height=27
I[05-08|08:57:11.130] Executed block                               module=consensus height=27 validTxs=0 invalidTxs=0
I[05-08|08:57:11.130] Applying block                               module=consensus height=28
I[05-08|08:57:11.130] Executed block                               module=consensus height=28 validTxs=0 invalidTxs=0
I[05-08|08:57:11.130] Applying block                               module=consensus height=29
I[05-08|08:57:11.131] Executed block                               module=consensus height=29 validTxs=0 invalidTxs=0
I[05-08|08:57:11.131] Applying block                               module=consensus height=30
I[05-08|08:57:11.131] Executed block                               module=consensus height=30 validTxs=0 invalidTxs=0
I[05-08|08:57:11.131] Applying block                               module=consensus height=31
I[05-08|08:57:11.131] Executed block                               module=consensus height=31 validTxs=0 invalidTxs=0
I[05-08|08:57:11.131] Applying block                               module=consensus height=32
I[05-08|08:57:11.131] Executed block                               module=consensus height=32 validTxs=0 invalidTxs=0
I[05-08|08:57:11.131] Applying block                               module=consensus height=33
I[05-08|08:57:11.131] Executed block                               module=consensus height=33 validTxs=0 invalidTxs=0
I[05-08|08:57:11.131] Applying block                               module=consensus height=34
I[05-08|08:57:11.131] Executed block                               module=consensus height=34 validTxs=0 invalidTxs=0
I[05-08|08:57:11.131] Applying block                               module=consensus height=35
I[05-08|08:57:11.132] Executed block                               module=consensus height=35 validTxs=0 invalidTxs=0
I[05-08|08:57:11.132] Applying block                               module=consensus height=36
I[05-08|08:57:11.132] Executed block                               module=consensus height=36 validTxs=0 invalidTxs=0
I[05-08|08:57:11.132] Applying block                               module=consensus height=37
I[05-08|08:57:11.132] Executed block                               module=consensus height=37 validTxs=0 invalidTxs=0
I[05-08|08:57:11.132] Applying block                               module=consensus height=38
I[05-08|08:57:11.132] Executed block                               module=consensus height=38 validTxs=0 invalidTxs=0
I[05-08|08:57:11.132] Applying block                               module=consensus height=39
I[05-08|08:57:11.132] Executed block                               module=consensus height=39 validTxs=0 invalidTxs=0

## 又回到/consensus/replay.go#Handshake的逻辑
I[05-08|08:57:11.132] Completed ABCI Handshake - Tendermint and App are synced module=consensus appHeight=0 appHash=

## 回到/node/node.go#NewNode的主逻辑中
I[05-08|08:57:11.132] This node is a validator                     module=consensus addr=7A494CED7A75A3F045F4FABE52280A16DED5A65D pubKey=PubKeyEd25519{5F87F716832591C3F48B9AEAAD73504CB628AD329C61F48BEE7E71A2B42F4FAB}
I[05-08|08:57:11.153] Starting Node                                module=main impl=Node
I[05-08|08:57:11.153] Starting EventBus                            module=events impl=EventBus
I[05-08|08:57:11.154] Starting RPC HTTP server on tcp://0.0.0.0:46657 module=rpc-server 
I[05-08|08:57:11.154] Local listener                               module=p2p ip=:: port=46656
I[05-08|08:57:11.154] Getting UPNP external address                module=p2p 
I[05-08|08:57:14.154] Could not perform UPNP discover              module=p2p err="read udp4 0.0.0.0:33435: i/o timeout"
I[05-08|08:57:14.154] Starting DefaultListener                     module=p2p impl=Listener(@10.10.5.202:46656)
I[05-08|08:57:14.154] P2P Node ID                                  module=main ID=252626a28739100229361aa04bb8c0c305d0cbb3 file=/root/tmdata/config/node_key.json
I[05-08|08:57:14.155] Add our address to book                      module=p2p book=/root/tmdata/config/addrbook.json addr=252626a28739100229361aa04bb8c0c305d0cbb3@10.10.5.202:46656
I[05-08|08:57:14.155] Starting P2P Switch                          module=p2p impl="P2P Switch"
I[05-08|08:57:14.155] Starting ConsensusReactor                    module=consensus impl=ConsensusReactor
I[05-08|08:57:14.155] ConsensusReactor                             module=consensus fastSync=true
I[05-08|08:57:14.155] Starting EvidenceReactor                     module=evidence impl=EvidenceReactor
I[05-08|08:57:14.155] Starting PEXReactor                          module=p2p impl=PEXReactor
I[05-08|08:57:14.155] Starting AddrBook                            module=p2p book=/root/tmdata/config/addrbook.json impl=AddrBook
I[05-08|08:57:14.155] Starting MempoolReactor                      module=mempool impl=MempoolReactor
I[05-08|08:57:14.155] Starting BlockchainReactor                   module=blockchain impl=BlockchainReactor
I[05-08|08:57:14.155] Starting BlockPool                           module=blockchain impl=BlockPool
I[05-08|08:57:14.155] Started node                                 module=main nodeInfo="NodeInfo{id: 252626a28739100229361aa04bb8c0c305d0cbb3, moniker: tendermint-node1, network: test-chain-c39DtV [listen 10.10.5.202:46656], version: 0.19.0 ([amino_version=0.9.6 p2p_version=0.5.0 consensus_version=v1/0.2.2 rpc_version=0.7.0/3 tx_index=on rpc_addr=tcp://0.0.0.0:46657])}"
I[05-08|08:57:14.155] Ensure peers                                 module=p2p numOutPeers=0 numInPeers=0 numDialing=0 numToDial=10
I[05-08|08:57:14.155] Will dial address                            module=p2p addr=df8be27e5d6b7f4e774224f4815ce12418497b18@47.75.188.184:46656
I[05-08|08:57:14.156] Dialing peer                                 module=p2p address=df8be27e5d6b7f4e774224f4815ce12418497b18@47.75.188.184:46656
I[05-08|08:57:14.169] Successful handshake with peer               module=p2p peer=47.75.188.184:46656 peerNodeInfo="NodeInfo{id: df8be27e5d6b7f4e774224f4815ce12418497b18, moniker: hk013-data-ethermint-test4, network: test-chain-c39DtV [listen 10.10.5.203:46656], version: 0.19.0 ([amino_version=0.9.6 p2p_version=0.5.0 consensus_version=v1/0.2.2 rpc_version=0.7.0/3 tx_index=on rpc_addr=tcp://0.0.0.0:46657])}"
I[05-08|08:57:14.169] Starting Peer                                module=p2p peer=47.75.188.184:46656 impl="Peer{MConn{47.75.188.184:46656} df8be27e5d6b7f4e774224f4815ce12418497b18 out}"
I[05-08|08:57:14.169] Starting MConnection                         module=p2p peer=47.75.188.184:46656 impl=MConn{47.75.188.184:46656}
I[05-08|08:57:14.169] Added peer                                   module=p2p peer="Peer{MConn{47.75.188.184:46656} df8be27e5d6b7f4e774224f4815ce12418497b18 out}"
I[05-08|08:57:14.372] Added new address                            module=p2p book=/root/tmdata/config/addrbook.json address=252626a28739100229361aa04bb8c0c305d0cbb3@47.75.50.204:46656 total=2
I[05-08|08:57:15.155] Time to switch to consensus reactor!         module=blockchain height=40
I[05-08|08:57:15.155] Stopping BlockPool                           module=blockchain impl=BlockPool
I[05-08|08:57:15.155] SwitchToConsensus                            module=consensus 
I[05-08|08:57:15.156] Ignoring updateToState()                     module=consensus newHeight=40 oldHeight=40
I[05-08|08:57:15.156] Starting ConsensusState                      module=consensus impl=ConsensusState
I[05-08|08:57:15.156] Starting baseWAL                             module=consensus wal=/root/tmdata/data/cs.wal/wal impl=baseWAL
I[05-08|08:57:15.156] Starting TimeoutTicker                       module=consensus impl=TimeoutTicker
I[05-08|08:57:15.164] Catchup by replaying consensus messages      module=consensus height=40
I[05-08|08:57:15.164] Replay: New Step                             module=consensus height=40 round=0 step=RoundStepNewHeight
I[05-08|08:57:15.164] Replay: Vote                                 module=consensus height=39 round=0 type=2 blockID=432438F4F749EEA761DEEB295310E4BAEEF119C5:1:55533247CE47 peer=df8be27e5d6b7f4e774224f4815ce12418497b18
I[05-08|08:57:15.164] Replay: Done                                 module=consensus 
I[05-08|08:57:15.164] Timed out                                    module=consensus dur=-3.02337633s height=40 round=0 step=RoundStepNewHeight
I[05-08|08:57:15.167] enterNewRound(40/0). Current: 40/0/RoundStepNewHeight module=consensus 
I[05-08|08:57:15.167] enterPropose(40/0). Current: 40/0/RoundStepNewRound module=consensus 
I[05-08|08:57:15.167] enterPropose: Our turn to propose            module=consensus proposer=7A494CED7A75A3F045F4FABE52280A16DED5A65D privValidator="PrivValidator{7A494CED7A75A3F045F4FABE52280A16DED5A65D LH:39, LR:0, LS:3}"
I[05-08|08:57:15.170] Signed proposal                              module=consensus height=40 round=0 proposal="Proposal{40/0 1:017707DF102D (-1,:0:000000000000) /A620C6A3461B.../ @ 2018-05-08T08:57:15.167Z}"
I[05-08|08:57:15.178] Received complete proposal block             module=consensus height=40 hash=474341837FEDD18F010BD0BA927C13B3C28DCFB0
I[05-08|08:57:15.178] enterPrevote(40/0). Current: 40/0/RoundStepPropose module=consensus 
I[05-08|08:57:15.179] enterPrevote: ProposalBlock is valid         module=consensus height=40 round=0
I[05-08|08:57:15.182] Signed and pushed vote                       module=consensus height=40 round=0 vote="Vote{1:7A494CED7A75 40/00/1(Prevote) 474341837FED /5360C025D1D6.../ @ 2018-05-08T08:57:15.179Z}" err=null
I[05-08|08:57:15.187] Added to prevote                             module=consensus vote="Vote{1:7A494CED7A75 40/00/1(Prevote) 474341837FED /5360C025D1D6.../ @ 2018-05-08T08:57:15.179Z}" prevotes="VoteSet{H:40 R:0 T:1 +2/3:<nil> BA{2:_x} map[]}"
I[05-08|08:57:15.492] Added to prevote                             module=consensus vote="Vote{0:5948424E0369 40/00/1(Prevote) 474341837FED /7B2460E8A08B.../ @ 2018-05-08T08:57:15.380Z}" prevotes="VoteSet{H:40 R:0 T:1 +2/3:474341837FEDD18F010BD0BA927C13B3C28DCFB0:1:017707DF102D BA{2:xx} map[]}"
I[05-08|08:57:15.492] enterPrecommit(40/0). Current: 40/0/RoundStepPrevote module=consensus 
I[05-08|08:57:15.492] enterPrecommit: +2/3 prevoted proposal block. Locking module=consensus hash=474341837FEDD18F010BD0BA927C13B3C28DCFB0
I[05-08|08:57:15.497] Signed and pushed vote                       module=consensus height=40 round=0 vote="Vote{1:7A494CED7A75 40/00/2(Precommit) 474341837FED /A0A32C1668EE.../ @ 2018-05-08T08:57:15.493Z}" err=null
I[05-08|08:57:15.502] Added to precommit                           module=consensus vote="Vote{0:5948424E0369 40/00/2(Precommit) 474341837FED /EC9D3DC22385.../ @ 2018-05-08T08:57:15.392Z}" precommits="VoteSet{H:40 R:0 T:2 +2/3:<nil> BA{2:x_} map[]}"
I[05-08|08:57:15.505] Added to precommit                           module=consensus vote="Vote{1:7A494CED7A75 40/00/2(Precommit) 474341837FED /A0A32C1668EE.../ @ 2018-05-08T08:57:15.493Z}" precommits="VoteSet{H:40 R:0 T:2 +2/3:474341837FEDD18F010BD0BA927C13B3C28DCFB0:1:017707DF102D BA{2:xx} map[]}"
I[05-08|08:57:15.505] enterCommit(40/0). Current: 40/0/RoundStepPrecommit module=consensus 
I[05-08|08:57:15.509] Finalizing commit of block with 0 txs        module=consensus height=40 hash=474341837FEDD18F010BD0BA927C13B3C28DCFB0 root=0000000000000000
I[05-08|08:57:15.509] Block{
  Header{
    ChainID:        test-chain-c39DtV
    Height:         40
    Time:           2018-05-08 08:57:15.167316692 +0000 UTC
    NumTxs:         0
    TotalTxs:       0
    LastBlockID:    432438F4F749EEA761DEEB295310E4BAEEF119C5:1:55533247CE47
    LastCommit:     E53529AC3D4B6ADBC9A8AF99C74AB8E28DC216E0
    Data:           
    Validators:     0C6826C9E3144741477E258F501A34120642C687
    App:            0000000000000000
    Consensus:       F66EF1DF8BA6DAC7A1ECCE40CC84E54A1CEBC6A5
    Results:        
    Evidence:       
  }#474341837FEDD18F010BD0BA927C13B3C28DCFB0
  Data{
    
  }#
  Data{
    
  }#
  Commit{
    BlockID:    432438F4F749EEA761DEEB295310E4BAEEF119C5:1:55533247CE47
    Precommits: Vote{0:5948424E0369 39/00/2(Precommit) 432438F4F749 /36AF2BED9A5C.../ @ 2018-05-08T08:55:08.598Z}
    Vote{1:7A494CED7A75 39/00/2(Precommit) 432438F4F749 /2FABDF0FE30F.../ @ 2018-05-08T08:55:08.497Z}
  }#E53529AC3D4B6ADBC9A8AF99C74AB8E28DC216E0
}#474341837FEDD18F010BD0BA927C13B3C28DCFB0 module=consensus 
I[05-08|08:57:15.518] Executed block                               module=state height=40 validTxs=0 invalidTxs=0
I[05-08|08:57:15.520] Committed state                              module=state height=40 txs=0 appHash=0000000000000000
I[05-08|08:57:15.520] Recheck txs                                  module=mempool numtxs=0 height=40
I[05-08|08:57:16.505] Timed out                                    module=consensus dur=975.059881ms height=41 round=0 step=RoundStepNewHeight
I[05-08|08:57:16.512] enterNewRound(41/0). Current: 41/0/RoundStepNewHeight module=consensus 
I[05-08|08:57:16.512] enterPropose(41/0). Current: 41/0/RoundStepNewRound module=consensus 
I[05-08|08:57:16.512] enterPropose: Not our turn to propose        module=consensus proposer=5948424E0369980B87246D4F17FAB221240BC569 privValidator="PrivValidator{7A494CED7A75A3F045F4FABE52280A16DED5A65D LH:40, LR:0, LS:3}"
I[05-08|08:57:16.713] Received complete proposal block             module=consensus height=41 hash=30389EFBA291AC4A3C2228F297F9D4F5C01FDCB3
I[05-08|08:57:16.713] enterPrevote(41/0). Current: 41/0/RoundStepPropose module=consensus 
I[05-08|08:57:16.713] enterPrevote: ProposalBlock is valid         module=consensus height=41 round=0
I[05-08|08:57:16.716] Signed and pushed vote                       module=consensus height=41 round=0 vote="Vote{1:7A494CED7A75 41/00/1(Prevote) 30389EFBA291 /691F09299DB5.../ @ 2018-05-08T08:57:16.714Z}" err=null
I[05-08|08:57:16.722] Added to prevote                             module=consensus vote="Vote{0:5948424E0369 41/00/1(Prevote) 30389EFBA291 /A1788C65EAA5.../ @ 2018-05-08T08:57:16.611Z}" prevotes="VoteSet{H:41 R:0 T:1 +2/3:<nil> BA{2:x_} map[]}"
I[05-08|08:57:16.728] Added to prevote                             module=consensus vote="Vote{1:7A494CED7A75 41/00/1(Prevote) 30389EFBA291 /691F09299DB5.../ @ 2018-05-08T08:57:16.714Z}" prevotes="VoteSet{H:41 R:0 T:1 +2/3:30389EFBA291AC4A3C2228F297F9D4F5C01FDCB3:1:3BDFE630E992 BA{2:xx} map[]}"
I[05-08|08:57:16.728] enterPrecommit(41/0). Current: 41/0/RoundStepPrevote module=consensus 
I[05-08|08:57:16.728] enterPrecommit: +2/3 prevoted proposal block. Locking module=consensus hash=30389EFBA291AC4A3C2228F297F9D4F5C01FDCB3
I[05-08|08:57:16.733] Signed and pushed vote                       module=consensus height=41 round=0 vote="Vote{1:7A494CED7A75 41/00/2(Precommit) 30389EFBA291 /D5A52B2482F1.../ @ 2018-05-08T08:57:16.728Z}" err=null
I[05-08|08:57:16.740] Added to precommit                           module=consensus vote="Vote{1:7A494CED7A75 41/00/2(Precommit) 30389EFBA291 /D5A52B2482F1.../ @ 2018-05-08T08:57:16.728Z}" precommits="VoteSet{H:41 R:0 T:2 +2/3:<nil> BA{2:_x} map[]}"
E[05-08|08:57:16.901] Connection failed @ recvRoutine (reading byte) module=p2p peer=47.75.188.184:46656 conn=MConn{47.75.188.184:46656} err=EOF
I[05-08|08:57:16.902] Stopping MConnection                         module=p2p peer=47.75.188.184:46656 impl=MConn{47.75.188.184:46656}
E[05-08|08:57:16.902] Stopping peer for error                      module=p2p peer="Peer{MConn{47.75.188.184:46656} df8be27e5d6b7f4e774224f4815ce12418497b18 out}" err=EOF
I[05-08|08:57:16.902] Stopping Peer                                module=p2p peer=47.75.188.184:46656 impl="Peer{MConn{47.75.188.184:46656} df8be27e5d6b7f4e774224f4815ce12418497b18 out}"
I[05-08|08:57:16.975] Stopping gossipDataRoutine for peer          module=consensus peer="Peer{MConn{47.75.188.184:46656} df8be27e5d6b7f4e774224f4815ce12418497b18 out}"
I[05-08|08:57:16.976] Stopping gossipVotesRoutine for peer         module=consensus peer="Peer{MConn{47.75.188.184:46656} df8be27e5d6b7f4e774224f4815ce12418497b18 out}"
I[05-08|08:57:18.170] Stopping queryMaj23Routine for peer          module=consensus peer="Peer{MConn{47.75.188.184:46656} df8be27e5d6b7f4e774224f4815ce12418497b18 out}"
^Ccaptured interrupt, exiting...
I[05-08|08:57:18.459] Stopping Node                                module=main impl=Node
I[05-08|08:57:18.459] Stopping Node                                module=main 
I[05-08|08:57:18.459] Stopping P2P Switch                          module=p2p impl="P2P Switch"
I[05-08|08:57:18.459] Stopping DefaultListener                     module=p2p impl=Listener(@10.10.5.202:46656)
I[05-08|08:57:18.459] Stopping PEXReactor                          module=p2p impl=PEXReactor
I[05-08|08:57:18.459] Stopping AddrBook                            module=p2p book=/root/tmdata/config/addrbook.json impl=AddrBook
I[05-08|08:57:18.459] Stopping MempoolReactor                      module=mempool impl=MempoolReactor
I[05-08|08:57:18.459] Stopping BlockchainReactor                   module=blockchain impl=BlockchainReactor
I[05-08|08:57:18.459] Stopping ConsensusReactor                    module=consensus impl=ConsensusReactor
I[05-08|08:57:18.459] Stopping ConsensusState                      module=consensus impl=ConsensusState
I[05-08|08:57:18.459] Stopping TimeoutTicker                       module=consensus impl=TimeoutTicker
I[05-08|08:57:18.459] Stopping EvidenceReactor                     module=evidence impl=EvidenceReactor
I[05-08|08:57:18.459] Closing rpc listener                         module=main listener=&{fd:0xc420108f80}
I[05-08|08:57:18.459] Stopping EventBus                            module=events impl=EventBus

###Below are some authixory information
root@:~/tmdata/config# cat addrbook.json 
{
	"key": "11eb4a72362508469f13fc4f",
	"addrs": [
		{
			"addr": {
				"ID": "df8be27e5d6b7f4e774224f4815ce12418497b18",
				"IP": "47.75.188.184",
				"Port": 46656
			},
			"src": {
				"ID": "252626a28739100229361aa04bb8c0c305d0cbb3",
				"IP": "10.10.5.202",
				"Port": 46656
			},
			"attempts": 0,
			"last_attempt": "2018-05-08T15:03:53.731238651+08:00",
			"last_success": "0001-01-01T00:00:00Z",
			"bucket_type": 1,
			"buckets": [
				213
			]
		}
	]
}root@tendermint-node1:~/tmdata/config# cat priv_validator.json 
{"address":"7A494CED7A75A3F045F4FABE52280A16DED5A65D","pub_key":{"type":"AC26791624DE60","value":"X4f3FoMlkcP0i5rqrXNQTLYorTKcYfSL7n5xorQvT6s="},"last_height":41,"last_round":0,"last_step":3,"last_signature":{"type":"6BF5903DA1DB28","value":"1aUrJILxx0Ozn7UtdjpNtVkTB/xRm3xJ5uQEEW4ua6EGJHrDKNrpdI+ZrERDWwMIbJFBco0UJOlUiDVzzIdgDA=="},"last_signbytes":"7B2240636861696E5F6964223A22746573742D636861696E2D633339447456222C224074797065223A22766F7465222C22626C6F636B5F6964223A7B2268617368223A2233303338394546424132393141433441334332323238463239374639443446354330314644434233222C227061727473223A7B2268617368223A2233424446453633304539393233324544334230413439353544313031433544354132444443333136222C22746F74616C223A317D7D2C22686569676874223A34312C22726F756E64223A302C2274696D657374616D70223A22323031382D30352D30385430383A35373A31362E3732385A222C2274797065223A327D","priv_key":{"type":"954568A3288910","value":"H+Mo8PDx9zgCmfCpcTcAqtATksqaMoL+h7F3g50xqPlfh/cWgyWRw/SLmuqtc1BMtiitMpxh9IvufnGitC9Pqw=="}}
### The address filed can be used for identifying validator

