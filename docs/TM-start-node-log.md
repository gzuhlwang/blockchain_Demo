I[03-25|04:40:48.219] Starting multiAppConn                        module=proxy impl=multiAppConn

I[03-25|04:40:48.219] Starting localClient                         module=abci-client connection=query impl=localClient

I[03-25|04:40:48.219] Starting localClient                         module=abci-client connection=mempool impl=localClient

I[03-25|04:40:48.219] Starting localClient                         module=abci-client connection=consensus impl=localClient

I[03-25|04:40:48.219] ABCI Handshake                               module=consensus appHeight=0 appHash=

I[03-25|04:40:48.219] ABCI Replay Blocks                           module=consensus appHeight=0 storeHeight=0 stateHeight=0

I[03-25|04:40:48.219] Completed ABCI Handshake - Tendermint and App are synced module=consensus appHeight=0 appHash=

I[03-25|04:40:48.219] This node is a validator                     module=consensus addr=BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D pubKey={PubKeyInner:PubKeyEd25519{7A4BCE42785BF1B008E2B2B9117FB617153597E9E3BBE00BB93889DFA7885461}}

I[03-25|04:40:48.243] Starting Node                                module=main impl=Node

I[03-25|04:40:48.243] Starting EventBus                            module=events impl=EventBus

I[03-25|04:40:48.243] Starting RPC HTTP server on tcp socket 0.0.0.0:46657 module=rpc-server

I[03-25|04:40:48.244] Local listener                               module=p2p ip=:: port=46656

I[03-25|04:40:48.244] Getting UPNP external address                module=p2p

I[03-25|04:40:51.244] Could not perform UPNP discover              module=p2p err="read udp4 0.0.0.0:50863: i/o timeout"

I[03-25|04:40:51.244] Starting DefaultListener                     module=p2p impl=Listener(@172.31.22.212:46656)

I[03-25|04:40:51.244] P2P Node ID                                  module=main ID=6082741e5b3494908078fe5f473563f1c483d79e file=/opt/datadir/tendermint/config/node_key.json

I[03-25|04:40:51.244] Starting P2P Switch                          module=p2p impl="P2P Switch"

I[03-25|04:40:51.244] Starting EvidenceReactor                     module=evidence impl=EvidenceReactor

I[03-25|04:40:51.245] Starting PEXReactor                          module=p2p impl=PEXReactor

I[03-25|04:40:51.245] Starting AddrBook                            module=p2p book=/opt/datadir/tendermint/config/addrbook.json impl=AddrBook

I[03-25|04:40:51.245] Starting MempoolReactor                      module=mempool impl=MempoolReactor

I[03-25|04:40:51.245] Starting BlockchainReactor                   module=blockchain impl=BlockchainReactor

I[03-25|04:40:51.245] Starting ConsensusReactor                    module=consensus impl=ConsensusReactor

I[03-25|04:40:51.245] ConsensusReactor                             module=consensus fastSync=false

I[03-25|04:40:51.245] Starting ConsensusState                      module=consensus impl=ConsensusState

I[03-25|04:40:51.245] Starting baseWAL                             module=consensus wal=/opt/datadir/tendermint/data/cs.wal/wal impl=baseWAL

I[03-25|04:40:51.247] Starting TimeoutTicker                       module=consensus impl=TimeoutTicker

I[03-25|04:40:51.248] Catchup by replaying consensus messages      module=consensus height=1

I[03-25|04:40:51.248] Replay: Done                                 module=consensus

I[03-25|04:40:51.248] Timed out                                    module=consensus dur=-2.019172706s height=1 round=0 step=RoundStepNewHeight

I[03-25|04:40:51.248] Started node                                 module=main nodeInfo="NodeInfo{pk: {PubKeyEd25519{54E665EFA8EF7AD5763C421129F66FBD367B253788543C0E1B9CF047C45771D3}}, moniker: xxx, network: test-chain-MErM3n [listen 172.31.22.212:46656], version: 0.16.0 ([wire_version=0.7.2 p2p_version=0.5.0 consensus_version=v1/0.2.2 rpc_version=0.7.0/3 tx_index=on rpc_addr=tcp://0.0.0.0:46657])}"
##至此，节点启动成功，开始提供服务。
#进入第一轮竞选

I[03-25|04:40:51.250] enterNewRound(1/0). Current: 1/0/RoundStepNewHeight module=consensus

I[03-25|04:40:51.250] enterPropose(1/0). Current: 1/0/RoundStepNewRound module=consensus

I[03-25|04:40:51.250] enterPropose: Our turn to propose            module=consensus proposer=BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D privValidator="PrivValidator{BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D LH:0, LR:0, LS:0}"

I[03-25|04:40:51.253] Signed proposal                              module=consensus height=1 round=0 proposal="Proposal{1/0 1:57D9BC19067F (-1,:0:000000000000) {/3FB2AD239E88.../} @ 2018-03-25T04:40:51.250Z}"

I[03-25|04:40:51.259] Received complete proposal block             module=consensus height=1 hash=2CFA5BC56A2E5D0BB94B84EB35AD05CC8F47CC49

I[03-25|04:40:51.259] enterPrevote(1/0). Current: 1/0/RoundStepPropose module=consensus

I[03-25|04:40:51.259] enterPrevote: ProposalBlock is valid         module=consensus height=1 round=0

I[03-25|04:40:51.261] Signed and pushed vote                       module=consensus height=1 round=0 vote="Vote{0:BD8F0160796A 1/00/1(Prevote) 2CFA5BC56A2E {/347B4DC16274.../} @ 2018-03-25T04:40:51.259Z}" err=null

I[03-25|04:40:51.265] Added to prevote                             module=consensus vote="Vote{0:BD8F0160796A 1/00/1(Prevote) 2CFA5BC56A2E {/347B4DC16274.../} @ 2018-03-25T04:40:51.259Z}" prevotes="VoteSet{H:1 R:0 T:1 +2/3:2CFA5BC56A2E5D0BB94B84EB35AD05CC8F47CC49:1:57D9BC19067F BA{1:X} map[]}"

I[03-25|04:40:51.265] enterPrecommit(1/0). Current: 1/0/RoundStepPrevote module=consensus

I[03-25|04:40:51.265] enterPrecommit: +2/3 prevoted proposal block. Locking module=consensus hash=2CFA5BC56A2E5D0BB94B84EB35AD05CC8F47CC49

I[03-25|04:40:51.267] Signed and pushed vote                       module=consensus height=1 round=0 vote="Vote{0:BD8F0160796A 1/00/2(Precommit) 2CFA5BC56A2E {/1AB356C41018.../} @ 2018-03-25T04:40:51.265Z}" err=null

I[03-25|04:40:51.271] Added to precommit                           module=consensus vote="Vote{0:BD8F0160796A 1/00/2(Precommit) 2CFA5BC56A2E {/1AB356C41018.../} @ 2018-03-25T04:40:51.265Z}" precommits="VoteSet{H:1 R:0 T:2 +2/3:2CFA5BC56A2E5D0BB94B84EB35AD05CC8F47CC49:1:57D9BC19067F BA{1:X} map[]}"

I[03-25|04:40:51.271] enterCommit(1/0). Current: 1/0/RoundStepPrecommit module=consensus

I[03-25|04:40:51.274] Finalizing commit of block with 0 txs        module=consensus height=1 
hash=2CFA5BC56A2E5D0BB94B84EB35AD05CC8F47CC49 root=

I[03-25|04:40:51.274] Block{

  Header{

    ChainID:        test-chain-MErM3n
    Height:         1
    Time:           2018-03-25 12:40:51.25 +0800 CST
    NumTxs:         0
    TotalTxs:       0
    LastBlockID:    :0:000000000000
    LastCommit:
    Data:
    Validators:     7DBC0AC152D72CA2DA37CAB8D6D5A73B8DA9DC43
    App:
    Conensus:       0B8CEF95EC57AC2D96038FD0AE3901C14FAE8E73
    Results:
    Evidence:
  }#2CFA5BC56A2E5D0BB94B84EB35AD05CC8F47CC49
  Data{

  }#
  Data{

  }#

  Commit{

    BlockID:    :0:000000000000
    Precommits:
  }#

}#2CFA5BC56A2E5D0BB94B84EB35AD05CC8F47CC49 module=consensus

I[03-25|04:40:51.279] Executed block                               module=state height=1 validTxs=0 invalidTxs=0

I[03-25|04:40:51.281] Committed state                              module=state height=1 txs=0 appHash=0000000000000000

I[03-25|04:40:51.281] Recheck txs                                  module=mempool numtxs=0 height=1

I[03-25|04:40:52.272] Timed out                                    module=consensus dur=983.293563ms height=2 round=0 step=RoundStepNewHeight
#进入第二轮竞选
I[03-25|04:40:52.274] enterNewRound(2/0). Current: 2/0/RoundStepNewHeight module=consensus

I[03-25|04:40:52.274] enterPropose(2/0). Current: 2/0/RoundStepNewRound module=consensus

I[03-25|04:40:52.274] enterPropose: Our turn to propose            module=consensus 
proposer=BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D privValidator="PrivValidator{BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D LH:1, LR:0, LS:3}"
I[03-25|04:40:52.276] Signed proposal                              module=consensus height=2 round=0 proposal="Proposal{2/0 1:FB8EA6CB4E08 (-1,:0:000000000000) {/46D0DF8DB329.../} @ 2018-03-25T04:40:52.274Z}"
I[03-25|04:40:52.282] Received complete proposal block             module=consensus height=2 hash=C42136D825614DAFDB7BB0E1FAA6C2A2EE2B2516
I[03-25|04:40:52.282] enterPrevote(2/0). Current: 2/0/RoundStepPropose module=consensus
I[03-25|04:40:52.282] enterPrevote: ProposalBlock is valid         module=consensus height=2 round=0
I[03-25|04:40:52.284] Signed and pushed vote                       module=consensus height=2 round=0 vote="Vote{0:BD8F0160796A 2/00/1(Prevote) C42136D82561 {/E96466717A1F.../} @ 2018-03-25T04:40:52.282Z}" err=null
I[03-25|04:40:52.288] Added to prevote                             module=consensus vote="Vote{0:BD8F0160796A 2/00/1(Prevote) C42136D82561 {/E96466717A1F.../} @ 2018-03-25T04:40:52.282Z}" prevotes="VoteSet{H:2 R:0 T:1 +2/3:C42136D825614DAFDB7BB0E1FAA6C2A2EE2B2516:1:FB8EA6CB4E08 BA{1:X} map[]}"
I[03-25|04:40:52.288] enterPrecommit(2/0). Current: 2/0/RoundStepPrevote module=consensus
I[03-25|04:40:52.288] enterPrecommit: +2/3 prevoted proposal block. Locking module=consensus hash=C42136D825614DAFDB7BB0E1FAA6C2A2EE2B2516
I[03-25|04:40:52.291] Signed and pushed vote                       module=consensus height=2 round=0 vote="Vote{0:BD8F0160796A 2/00/2(Precommit) C42136D82561 {/2C0E36816AC1.../} @ 2018-03-25T04:40:52.289Z}" err=null
I[03-25|04:40:52.295] Added to precommit                           module=consensus vote="Vote{0:BD8F0160796A 2/00/2(Precommit) C42136D82561 {/2C0E36816AC1.../} @ 2018-03-25T04:40:52.289Z}" precommits="VoteSet{H:2 R:0 T:2 +2/3:C42136D825614DAFDB7BB0E1FAA6C2A2EE2B2516:1:FB8EA6CB4E08 BA{1:X} map[]}"
I[03-25|04:40:52.295] enterCommit(2/0). Current: 2/0/RoundStepPrecommit module=consensus
I[03-25|04:40:52.298] Finalizing commit of block with 0 txs        module=consensus height=2 hash=C42136D825614DAFDB7BB0E1FAA6C2A2EE2B2516 root=0000000000000000
I[03-25|04:40:52.298] Block{
  Header{
    ChainID:        test-chain-MErM3n
    Height:         2
    Time:           2018-03-25 12:40:52.274 +0800 CST
    NumTxs:         0
    TotalTxs:       0
    LastBlockID:    2CFA5BC56A2E5D0BB94B84EB35AD05CC8F47CC49:1:57D9BC19067F
    LastCommit:     4023F7463FA70B62354FE6C38813675E58311ACD
    Data:
    Validators:     7DBC0AC152D72CA2DA37CAB8D6D5A73B8DA9DC43
    App:            0000000000000000
    Conensus:       0B8CEF95EC57AC2D96038FD0AE3901C14FAE8E73
    Results:
    Evidence:
  }#C42136D825614DAFDB7BB0E1FAA6C2A2EE2B2516
  Data{

  }#
  Data{

  }#
  Commit{
    BlockID:    2CFA5BC56A2E5D0BB94B84EB35AD05CC8F47CC49:1:57D9BC19067F
    Precommits: Vote{0:BD8F0160796A 1/00/2(Precommit) 2CFA5BC56A2E {/1AB356C41018.../} @ 2018-03-25T04:40:51.265Z}
  }#4023F7463FA70B62354FE6C38813675E58311ACD
}#C42136D825614DAFDB7BB0E1FAA6C2A2EE2B2516 module=consensus
I[03-25|04:40:52.303] Executed block                               module=state height=2 validTxs=0 invalidTxs=0
I[03-25|04:40:52.305] Committed state                              module=state height=2 txs=0 appHash=0000000000000000
I[03-25|04:40:52.305] Recheck txs                                  module=mempool numtxs=0 height=2
I[03-25|04:40:53.295] Timed out                                    module=consensus dur=983.417207ms height=3 round=0 step=RoundStepNewHeight
#进入第三轮竞选
I[03-25|04:40:53.297] enterNewRound(3/0). Current: 3/0/RoundStepNewHeight module=consensus
I[03-25|04:40:53.297] enterPropose(3/0). Current: 3/0/RoundStepNewRound module=consensus
I[03-25|04:40:53.297] enterPropose: Our turn to propose            module=consensus proposer=BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D privValidator="PrivValidator{BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D LH:2, LR:0, LS:3}"
I[03-25|04:40:53.300] Signed proposal                              module=consensus height=3 round=0 proposal="Proposal{3/0 1:A4C0397361F7 (-1,:0:000000000000) {/3A452D01E01A.../} @ 2018-03-25T04:40:53.298Z}"
I[03-25|04:40:53.306] Received complete proposal block             module=consensus height=3 hash=29CB0877F667A6441A1CE2AE88047E362E02A2E6
I[03-25|04:40:53.306] enterPrevote(3/0). Current: 3/0/RoundStepPropose module=consensus
I[03-25|04:40:53.306] enterPrevote: ProposalBlock is valid         module=consensus height=3 round=0
I[03-25|04:40:53.308] Signed and pushed vote                       module=consensus height=3 round=0 vote="Vote{0:BD8F0160796A 3/00/1(Prevote) 29CB0877F667 {/1E4EF5DE4C60.../} @ 2018-03-25T04:40:53.306Z}" err=null
I[03-25|04:40:53.312] Added to prevote                             module=consensus vote="Vote{0:BD8F0160796A 3/00/1(Prevote) 29CB0877F667 {/1E4EF5DE4C60.../} @ 2018-03-25T04:40:53.306Z}" prevotes="VoteSet{H:3 R:0 T:1 +2/3:29CB0877F667A6441A1CE2AE88047E362E02A2E6:1:A4C0397361F7 BA{1:X} map[]}"
I[03-25|04:40:53.312] enterPrecommit(3/0). Current: 3/0/RoundStepPrevote module=consensus
I[03-25|04:40:53.312] enterPrecommit: +2/3 prevoted proposal block. Locking module=consensus hash=29CB0877F667A6441A1CE2AE88047E362E02A2E6
I[03-25|04:40:53.315] Signed and pushed vote                       module=consensus height=3 round=0 vote="Vote{0:BD8F0160796A 3/00/2(Precommit) 29CB0877F667 {/CC14DE861AB9.../} @ 2018-03-25T04:40:53.313Z}" err=null
I[03-25|04:40:53.319] Added to precommit                           module=consensus vote="Vote{0:BD8F0160796A 3/00/2(Precommit) 29CB0877F667 {/CC14DE861AB9.../} @ 2018-03-25T04:40:53.313Z}" precommits="VoteSet{H:3 R:0 T:2 +2/3:29CB0877F667A6441A1CE2AE88047E362E02A2E6:1:A4C0397361F7 BA{1:X} map[]}"
I[03-25|04:40:53.319] enterCommit(3/0). Current: 3/0/RoundStepPrecommit module=consensus
I[03-25|04:40:53.321] Finalizing commit of block with 0 txs        module=consensus height=3 hash=29CB0877F667A6441A1CE2AE88047E362E02A2E6 root=0000000000000000
I[03-25|04:40:53.321] Block{
  Header{
    ChainID:        test-chain-MErM3n
    Height:         3
    Time:           2018-03-25 12:40:53.297 +0800 CST
    NumTxs:         0
    TotalTxs:       0
    LastBlockID:    C42136D825614DAFDB7BB0E1FAA6C2A2EE2B2516:1:FB8EA6CB4E08
    LastCommit:     8DC1265FDDD7BA9B0E4FB13FB0E90EBD3ADEE0C4
    Data:
    Validators:     7DBC0AC152D72CA2DA37CAB8D6D5A73B8DA9DC43
    App:            0000000000000000
    Conensus:       0B8CEF95EC57AC2D96038FD0AE3901C14FAE8E73
    Results:
    Evidence:
  }#29CB0877F667A6441A1CE2AE88047E362E02A2E6
  Data{

  }#
  Data{

  }#
  Commit{
    BlockID:    C42136D825614DAFDB7BB0E1FAA6C2A2EE2B2516:1:FB8EA6CB4E08
    Precommits: Vote{0:BD8F0160796A 2/00/2(Precommit) C42136D82561 {/2C0E36816AC1.../} @ 2018-03-25T04:40:52.289Z}
  }#8DC1265FDDD7BA9B0E4FB13FB0E90EBD3ADEE0C4
}#29CB0877F667A6441A1CE2AE88047E362E02A2E6 module=consensus
I[03-25|04:40:53.327] Executed block                               module=state height=3 validTxs=0 invalidTxs=0
I[03-25|04:40:53.329] Committed state                              module=state height=3 txs=0 appHash=0000000000000000
I[03-25|04:40:53.329] Recheck txs                                  module=mempool numtxs=0 height=3
I[03-25|04:40:54.319] Timed out                                    module=consensus dur=983.977228ms height=4 round=0 step=RoundStepNewHeight
#进入第四轮竞选
I[03-25|04:40:54.321] enterNewRound(4/0). Current: 4/0/RoundStepNewHeight module=consensus
I[03-25|04:40:54.321] enterPropose(4/0). Current: 4/0/RoundStepNewRound module=consensus
I[03-25|04:40:54.321] enterPropose: Our turn to propose            module=consensus proposer=BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D privValidator="PrivValidator{BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D LH:3, LR:0, LS:3}"
I[03-25|04:40:54.324] Signed proposal                              module=consensus height=4 round=0 proposal="Proposal{4/0 1:249551F52468 (-1,:0:000000000000) {/82DC6F309BF2.../} @ 2018-03-25T04:40:54.322Z}"
I[03-25|04:40:54.330] Received complete proposal block             module=consensus height=4 hash=E3CF29F971473CA698122F89084D187FC5E0E64E
I[03-25|04:40:54.330] enterPrevote(4/0). Current: 4/0/RoundStepPropose module=consensus
I[03-25|04:40:54.330] enterPrevote: ProposalBlock is valid         module=consensus height=4 round=0
I[03-25|04:40:54.332] Signed and pushed vote                       module=consensus height=4 round=0 vote="Vote{0:BD8F0160796A 4/00/1(Prevote) E3CF29F97147 {/88556BD626EB.../} @ 2018-03-25T04:40:54.330Z}" err=null
I[03-25|04:40:54.337] Added to prevote                             module=consensus vote="Vote{0:BD8F0160796A 4/00/1(Prevote) E3CF29F97147 {/88556BD626EB.../} @ 2018-03-25T04:40:54.330Z}" prevotes="VoteSet{H:4 R:0 T:1 +2/3:E3CF29F971473CA698122F89084D187FC5E0E64E:1:249551F52468 BA{1:X} map[]}"
I[03-25|04:40:54.337] enterPrecommit(4/0). Current: 4/0/RoundStepPrevote module=consensus
I[03-25|04:40:54.337] enterPrecommit: +2/3 prevoted proposal block. Locking module=consensus hash=E3CF29F971473CA698122F89084D187FC5E0E64E
I[03-25|04:40:54.339] Signed and pushed vote                       module=consensus height=4 round=0 vote="Vote{0:BD8F0160796A 4/00/2(Precommit) E3CF29F97147 {/780513CA099E.../} @ 2018-03-25T04:40:54.337Z}" err=null
I[03-25|04:40:54.343] Added to precommit                           module=consensus vote="Vote{0:BD8F0160796A 4/00/2(Precommit) E3CF29F97147 {/780513CA099E.../} @ 2018-03-25T04:40:54.337Z}" precommits="VoteSet{H:4 R:0 T:2 +2/3:E3CF29F971473CA698122F89084D187FC5E0E64E:1:249551F52468 BA{1:X} map[]}"
I[03-25|04:40:54.343] enterCommit(4/0). Current: 4/0/RoundStepPrecommit module=consensus
I[03-25|04:40:54.346] Finalizing commit of block with 0 txs        module=consensus height=4 hash=E3CF29F971473CA698122F89084D187FC5E0E64E root=0000000000000000
I[03-25|04:40:54.346] Block{
  Header{
    ChainID:        test-chain-MErM3n
    Height:         4
    Time:           2018-03-25 12:40:54.321 +0800 CST
    NumTxs:         0
    TotalTxs:       0
    LastBlockID:    29CB0877F667A6441A1CE2AE88047E362E02A2E6:1:A4C0397361F7
    LastCommit:     B80329D682E9645245D42AADCAFFAFA8B8D1CEBE
    Data:
    Validators:     7DBC0AC152D72CA2DA37CAB8D6D5A73B8DA9DC43
    App:            0000000000000000
    Conensus:       0B8CEF95EC57AC2D96038FD0AE3901C14FAE8E73
    Results:
    Evidence:
  }#E3CF29F971473CA698122F89084D187FC5E0E64E
  Data{

  }#
  Data{

  }#
  Commit{
    BlockID:    29CB0877F667A6441A1CE2AE88047E362E02A2E6:1:A4C0397361F7
    Precommits: Vote{0:BD8F0160796A 3/00/2(Precommit) 29CB0877F667 {/CC14DE861AB9.../} @ 2018-03-25T04:40:53.313Z}
  }#B80329D682E9645245D42AADCAFFAFA8B8D1CEBE
}#E3CF29F971473CA698122F89084D187FC5E0E64E module=consensus
I[03-25|04:40:54.352] Executed block                               module=state height=4 validTxs=0 invalidTxs=0
I[03-25|04:40:54.354] Committed state                              module=state height=4 txs=0 appHash=0000000000000000
I[03-25|04:40:54.354] Recheck txs                                  module=mempool numtxs=0 height=4
I[03-25|04:40:55.344] Timed out                                    module=consensus dur=982.612404ms height=5 round=0 step=RoundStepNewHeight
I[03-25|04:40:55.346] enterNewRound(5/0). Current: 5/0/RoundStepNewHeight module=consensus
I[03-25|04:40:55.346] enterPropose(5/0). Current: 5/0/RoundStepNewRound module=consensus
I[03-25|04:40:55.346] enterPropose: Our turn to propose            module=consensus proposer=BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D privValidator="PrivValidator{BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D LH:4, LR:0, LS:3}"
I[03-25|04:40:55.348] Signed proposal                              module=consensus height=5 round=0 proposal="Proposal{5/0 1:71408F28B339 (-1,:0:000000000000) {/B21CD4AB1928.../} @ 2018-03-25T04:40:55.346Z}"
I[03-25|04:40:55.354] Received complete proposal block             module=consensus height=5 hash=3C9418E7F89C7438A0E45F594CF124003C747860
I[03-25|04:40:55.354] enterPrevote(5/0). Current: 5/0/RoundStepPropose module=consensus
I[03-25|04:40:55.354] enterPrevote: ProposalBlock is valid         module=consensus height=5 round=0
I[03-25|04:40:55.357] Signed and pushed vote                       module=consensus height=5 round=0 vote="Vote{0:BD8F0160796A 5/00/1(Prevote) 3C9418E7F89C {/9C35BEA84BA6.../} @ 2018-03-25T04:40:55.354Z}" err=null
I[03-25|04:40:55.361] Added to prevote                             module=consensus vote="Vote{0:BD8F0160796A 5/00/1(Prevote) 3C9418E7F89C {/9C35BEA84BA6.../} @ 2018-03-25T04:40:55.354Z}" prevotes="VoteSet{H:5 R:0 T:1 +2/3:3C9418E7F89C7438A0E45F594CF124003C747860:1:71408F28B339 BA{1:X} map[]}"
I[03-25|04:40:55.361] enterPrecommit(5/0). Current: 5/0/RoundStepPrevote module=consensus
I[03-25|04:40:55.361] enterPrecommit: +2/3 prevoted proposal block. Locking module=consensus hash=3C9418E7F89C7438A0E45F594CF124003C747860
I[03-25|04:40:55.363] Signed and pushed vote                       module=consensus height=5 round=0 vote="Vote{0:BD8F0160796A 5/00/2(Precommit) 3C9418E7F89C {/1423D8A4054C.../} @ 2018-03-25T04:40:55.361Z}" err=null
I[03-25|04:40:55.367] Added to precommit                           module=consensus vote="Vote{0:BD8F0160796A 5/00/2(Precommit) 3C9418E7F89C {/1423D8A4054C.../} @ 2018-03-25T04:40:55.361Z}" precommits="VoteSet{H:5 R:0 T:2 +2/3:3C9418E7F89C7438A0E45F594CF124003C747860:1:71408F28B339 BA{1:X} map[]}"
I[03-25|04:40:55.367] enterCommit(5/0). Current: 5/0/RoundStepPrecommit module=consensus
I[03-25|04:40:55.370] Finalizing commit of block with 0 txs        module=consensus height=5 hash=3C9418E7F89C7438A0E45F594CF124003C747860 root=0000000000000000
I[03-25|04:40:55.370] Block{
  Header{
    ChainID:        test-chain-MErM3n
    Height:         5
    Time:           2018-03-25 12:40:55.346 +0800 CST
    NumTxs:         0
    TotalTxs:       0
    LastBlockID:    E3CF29F971473CA698122F89084D187FC5E0E64E:1:249551F52468
    LastCommit:     7E92F8CC0866717C13CEFA943B01D3507379325C
    Data:
    Validators:     7DBC0AC152D72CA2DA37CAB8D6D5A73B8DA9DC43
    App:            0000000000000000
    Conensus:       0B8CEF95EC57AC2D96038FD0AE3901C14FAE8E73
    Results:
    Evidence:
  }#3C9418E7F89C7438A0E45F594CF124003C747860
  Data{

  }#
  Data{

  }#
  Commit{
    BlockID:    E3CF29F971473CA698122F89084D187FC5E0E64E:1:249551F52468
    Precommits: Vote{0:BD8F0160796A 4/00/2(Precommit) E3CF29F97147 {/780513CA099E.../} @ 2018-03-25T04:40:54.337Z}
  }#7E92F8CC0866717C13CEFA943B01D3507379325C
}#3C9418E7F89C7438A0E45F594CF124003C747860 module=consensus
I[03-25|04:40:55.375] Executed block                               module=state height=5 validTxs=0 invalidTxs=0
I[03-25|04:40:55.377] Committed state                              module=state height=5 txs=0 appHash=0000000000000000
I[03-25|04:40:55.377] Recheck txs                                  module=mempool numtxs=0 height=5
I[03-25|04:40:56.367] Timed out                                    module=consensus dur=982.995126ms height=6 round=0 step=RoundStepNewHeight
#进入第六轮竞选
I[03-25|04:40:56.369] enterNewRound(6/0). Current: 6/0/RoundStepNewHeight module=consensus
I[03-25|04:40:56.369] enterPropose(6/0). Current: 6/0/RoundStepNewRound module=consensus
I[03-25|04:40:56.369] enterPropose: Our turn to propose            module=consensus proposer=BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D privValidator="PrivValidator{BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D LH:5, LR:0, LS:3}"
I[03-25|04:40:56.372] Signed proposal                              module=consensus height=6 round=0 proposal="Proposal{6/0 1:1494FCA8EDE2 (-1,:0:000000000000) {/B2BEE47880D4.../} @ 2018-03-25T04:40:56.370Z}"
I[03-25|04:40:56.378] Received complete proposal block             module=consensus height=6 hash=8AD379E85954B22FB1300F58D6A73FB31442B4D1
I[03-25|04:40:56.378] enterPrevote(6/0). Current: 6/0/RoundStepPropose module=consensus
I[03-25|04:40:56.379] enterPrevote: ProposalBlock is valid         module=consensus height=6 round=0
I[03-25|04:40:56.381] Signed and pushed vote                       module=consensus height=6 round=0 vote="Vote{0:BD8F0160796A 6/00/1(Prevote) 8AD379E85954 {/408D2AB5E60B.../} @ 2018-03-25T04:40:56.379Z}" err=null
I[03-25|04:40:56.386] Added to prevote                             module=consensus vote="Vote{0:BD8F0160796A 6/00/1(Prevote) 8AD379E85954 {/408D2AB5E60B.../} @ 2018-03-25T04:40:56.379Z}" prevotes="VoteSet{H:6 R:0 T:1 +2/3:8AD379E85954B22FB1300F58D6A73FB31442B4D1:1:1494FCA8EDE2 BA{1:X} map[]}"
I[03-25|04:40:56.386] enterPrecommit(6/0). Current: 6/0/RoundStepPrevote module=consensus
I[03-25|04:40:56.386] enterPrecommit: +2/3 prevoted proposal block. Locking module=consensus hash=8AD379E85954B22FB1300F58D6A73FB31442B4D1
I[03-25|04:40:56.388] Signed and pushed vote                       module=consensus height=6 round=0 vote="Vote{0:BD8F0160796A 6/00/2(Precommit) 8AD379E85954 {/A02E870B5F1E.../} @ 2018-03-25T04:40:56.386Z}" err=null
I[03-25|04:40:56.393] Added to precommit                           module=consensus vote="Vote{0:BD8F0160796A 6/00/2(Precommit) 8AD379E85954 {/A02E870B5F1E.../} @ 2018-03-25T04:40:56.386Z}" precommits="VoteSet{H:6 R:0 T:2 +2/3:8AD379E85954B22FB1300F58D6A73FB31442B4D1:1:1494FCA8EDE2 BA{1:X} map[]}"
I[03-25|04:40:56.393] enterCommit(6/0). Current: 6/0/RoundStepPrecommit module=consensus
I[03-25|04:40:56.395] Finalizing commit of block with 0 txs        module=consensus height=6 hash=8AD379E85954B22FB1300F58D6A73FB31442B4D1 root=0000000000000000
I[03-25|04:40:56.395] Block{
  Header{
    ChainID:        test-chain-MErM3n
    Height:         6
    Time:           2018-03-25 12:40:56.369 +0800 CST
    NumTxs:         0
    TotalTxs:       0
    LastBlockID:    3C9418E7F89C7438A0E45F594CF124003C747860:1:71408F28B339
    LastCommit:     15F28C7294FB3052744869FEFECE42E3AEEFE302
    Data:
    Validators:     7DBC0AC152D72CA2DA37CAB8D6D5A73B8DA9DC43
    App:            0000000000000000
    Conensus:       0B8CEF95EC57AC2D96038FD0AE3901C14FAE8E73
    Results:
    Evidence:
  }#8AD379E85954B22FB1300F58D6A73FB31442B4D1
  Data{

  }#
  Data{

  }#
  Commit{
    BlockID:    3C9418E7F89C7438A0E45F594CF124003C747860:1:71408F28B339
    Precommits: Vote{0:BD8F0160796A 5/00/2(Precommit) 3C9418E7F89C {/1423D8A4054C.../} @ 2018-03-25T04:40:55.361Z}
  }#15F28C7294FB3052744869FEFECE42E3AEEFE302
}#8AD379E85954B22FB1300F58D6A73FB31442B4D1 module=consensus
I[03-25|04:40:56.401] Executed block                               module=state height=6 validTxs=0 invalidTxs=0
I[03-25|04:40:56.403] Committed state                              module=state height=6 txs=0 appHash=0000000000000000
I[03-25|04:40:56.403] Recheck txs                                  module=mempool numtxs=0 height=6
I[03-25|04:40:57.393] Timed out                                    module=consensus dur=982.79493ms height=7 round=0 step=RoundStepNewHeight
I[03-25|04:40:57.395] enterNewRound(7/0). Current: 7/0/RoundStepNewHeight module=consensus
I[03-25|04:40:57.395] enterPropose(7/0). Current: 7/0/RoundStepNewRound module=consensus
I[03-25|04:40:57.395] enterPropose: Our turn to propose            module=consensus proposer=BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D privValidator="PrivValidator{BD8F0160796AEC1E6454C55CCA6AF15EACF94A2D LH:6, LR:0, LS:3}"
I[03-25|04:40:57.397] Signed proposal                              module=consensus height=7 round=0 proposal="Proposal{7/0 1:38862324613F (-1,:0:000000000000) {/E7C317A6025E.../} @ 2018-03-25T04:40:57.395Z}"
I[03-25|04:40:57.404] Received complete proposal block             module=consensus height=7 hash=37DBE3EE8D355DEDD7B1858307A0683957FD58E6
I[03-25|04:40:57.404] enterPrevote(7/0). Current: 7/0/RoundStepPropose module=consensus
I[03-25|04:40:57.404] enterPrevote: ProposalBlock is valid         module=consensus height=7 round=0
I[03-25|04:40:57.407] Signed and pushed vote                       module=consensus height=7 round=0 vote="Vote{0:BD8F0160796A 7/00/1(Prevote) 37DBE3EE8D35 {/C39325ED6F8B.../} @ 2018-03-25T04:40:57.405Z}" err=null
I[03-25|04:40:57.411] Added to prevote                             module=consensus vote="Vote{0:BD8F0160796A 7/00/1(Prevote) 37DBE3EE8D35 {/C39325ED6F8B.../} @ 2018-03-25T04:40:57.405Z}" prevotes="VoteSet{H:7 R:0 T:1 +2/3:37DBE3EE8D355DEDD7B1858307A0683957FD58E6:1:38862324613F BA{1:X} map[]}"
I[03-25|04:40:57.411] enterPrecommit(7/0). Current: 7/0/RoundStepPrevote module=consensus
I[03-25|04:40:57.411] enterPrecommit: +2/3 prevoted proposal block. Locking module=consensus hash=37DBE3EE8D355DEDD7B1858307A0683957FD58E6
I[03-25|04:40:57.413] Signed and pushed vote                       module=consensus height=7 round=0 vote="Vote{0:BD8F0160796A 7/00/2(Precommit) 37DBE3EE8D35 {/9ADE116E7D07.../} @ 2018-03-25T04:40:57.411Z}" err=null
I[03-25|04:40:57.417] Added to precommit                           module=consensus vote="Vote{0:BD8F0160796A 7/00/2(Precommit) 37DBE3EE8D35 {/9ADE116E7D07.../} @ 2018-03-25T04:40:57.411Z}" precommits="VoteSet{H:7 R:0 T:2 +2/3:37DBE3EE8D355DEDD7B1858307A0683957FD58E6:1:38862324613F BA{1:X} map[]}"
I[03-25|04:40:57.417] enterCommit(7/0). Current: 7/0/RoundStepPrecommit module=consensus
I[03-25|04:40:57.420] Finalizing commit of block with 0 txs        module=consensus height=7 hash=37DBE3EE8D355DEDD7B1858307A0683957FD58E6 root=0000000000000000
I[03-25|04:40:57.420] Block{
  Header{
    ChainID:        test-chain-MErM3n
    Height:         7
    Time:           2018-03-25 12:40:57.395 +0800 CST
    NumTxs:         0
    TotalTxs:       0
    LastBlockID:    8AD379E85954B22FB1300F58D6A73FB31442B4D1:1:1494FCA8EDE2
    LastCommit:     21C22ADBAE49E9E157CD1B4E4C60C6C020BE12FD
    Data:
    Validators:     7DBC0AC152D72CA2DA37CAB8D6D5A73B8DA9DC43
    App:            0000000000000000
    Conensus:       0B8CEF95EC57AC2D96038FD0AE3901C14FAE8E73
    Results:
    Evidence:
  }#37DBE3EE8D355DEDD7B1858307A0683957FD58E6
  Data{

  }#
  Data{

  }#
  Commit{
    BlockID:    8AD379E85954B22FB1300F58D6A73FB31442B4D1:1:1494FCA8EDE2
    Precommits: Vote{0:BD8F0160796A 6/00/2(Precommit) 8AD379E85954 {/A02E870B5F1E.../} @ 2018-03-25T04:40:56.386Z}
  }#21C22ADBAE49E9E157CD1B4E4C60C6C020BE12FD
}#37DBE3EE8D355DEDD7B1858307A0683957FD58E6 module=consensus
I[03-25|04:40:57.425] Executed block                               module=state height=7 validTxs=0 invalidTxs=0
I[03-25|04:40:57.427] Committed state                              module=state height=7 txs=0 appHash=0000000000000000
I[03-25|04:40:57.427] Recheck txs                                  module=mempool numtxs=0 height=7
I[03-25|04:40:58.417] Timed out                                    module=consensus dur=984.479107ms height=8 round=0 step=RoundStepNewHeight
