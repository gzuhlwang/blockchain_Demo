# node1：./geth --networkid 14  --nodiscover --datadir  ./data0  --port  61912 --rpcapi net,eth,web3,personal --rpc  --rpcport 8102 console
WARN [07-10|16:15:34] No etherbase set and no accounts found as default
INFO [07-10|16:15:34] Starting peer-to-peer node               instance=Geth/v1.6.7-stable-ab5646c5/linux-amd64/go1.9.1
INFO [07-10|16:15:34] Allocated cache and file handles         database=/root/go-ethereum/build/bin/data0/geth/chaindata cache=128 handles=1024
WARN [07-10|16:15:34] Upgrading chain database to use sequential keys
INFO [07-10|16:15:34] Initialised chain configuration          config="{ChainID: 15 Homestead: 0 DAO: <nil> DAOSupport: false EIP150: <nil> EIP155: 0 EIP158: 0 Metropolis: <nil> Engine: unknown}"
INFO [07-10|16:15:34] Disk storage enabled for ethash caches   dir=/root/go-ethereum/build/bin/data0/geth/ethash count=3
INFO [07-10|16:15:34] Disk storage enabled for ethash DAGs     dir=/root/.ethash                                 count=2
WARN [07-10|16:15:34] Upgrading db log bloom bins
INFO [07-10|16:15:34] Database conversion successful
INFO [07-10|16:15:34] Bloom-bin upgrade completed              elapsed=408.831µs
INFO [07-10|16:15:34] Initialising Ethereum protocol           versions="[63 62]" network=14
INFO [07-10|16:15:34] Loaded most recent local header          number=0 hash=272003…b62890 td=1024
INFO [07-10|16:15:34] Loaded most recent local full block      number=0 hash=272003…b62890 td=1024
INFO [07-10|16:15:34] Loaded most recent local fast block      number=0 hash=272003…b62890 td=1024
INFO [07-10|16:15:34] Starting P2P networking
INFO [07-10|16:15:34] RLPx listener up                         self="enode://182fff1f115bc8be4836b305f4394fddc5e9706a863e00bee22e38aba42e3d8e33f1d799db9c26a1b4e289ef60e3e6e4d935f94a0ecc61dc1bddc647c0335243@[::]:61912?discport=0"
INFO [07-10|16:15:34] HTTP endpoint opened: http://127.0.0.1:8102
INFO [07-10|16:15:35] IPC endpoint opened: /root/go-ethereum/build/bin/data0/geth.ipc
Welcome to the Geth JavaScript console!

instance: Geth/v1.6.7-stable-ab5646c5/linux-amd64/go1.9.1
 modules: admin:1.0 debug:1.0 eth:1.0 miner:1.0 net:1.0 personal:1.0 rpc:1.0 txpool:1.0 web3:1.0

> personal.newAccount("data")   //创建账户
"0x4ec01f28e27fee33b0d10dd882bcd8750035a5d3"
> INFO [07-10|16:15:59] New wallet appeared                      url=keystore:///root/go-ethereum/bu… status=Locked
> admin.nodeInfo                //获取节点信息
{
  enode: "enode://182fff1f115bc8be4836b305f4394fddc5e9706a863e00bee22e38aba42e3d8e33f1d799db9c26a1b4e289ef60e3e6e4d935f94a0ecc61dc1bddc647c0335243@[::]:61912?discport=0",
  id: "182fff1f115bc8be4836b305f4394fddc5e9706a863e00bee22e38aba42e3d8e33f1d799db9c26a1b4e289ef60e3e6e4d935f94a0ecc61dc1bddc647c0335243",
  ip: "::",
  listenAddr: "[::]:61912",
  name: "Geth/v1.6.7-stable-ab5646c5/linux-amd64/go1.9.1",
  ports: {
    discovery: 0,
    listener: 61912
  },
  protocols: {
    eth: {
      difficulty: 1024,
      genesis: "0x2720038ef46044a7a895296b85745294340ecfcedc32f8c9e9802129aeb62890",
      head: "0x2720038ef46044a7a895296b85745294340ecfcedc32f8c9e9802129aeb62890",
      network: 14
    }
  }
}
> INFO [07-10|16:17:41] Block synchronisation started
INFO [07-10|16:17:41] Imported new state entries               count=1 flushed=1 elapsed=114.776µs processed=1 pending=0 retry=0 duplicate=0 unexpected=0
INFO [07-10|16:17:42] Imported new block headers               count=2 elapsed=1.282s    number=2 hash=fdb247…698ce1 ignored=0
INFO [07-10|16:17:42] Imported new chain segment               blocks=2 txs=0 mgas=0.000 elapsed=1.364ms   mgasps=0.000 number=2 hash=fdb247…698ce1
WARN [07-10|16:17:42] Discarded bad propagated block           number=1 hash=7f827a…817398
INFO [07-10|16:17:42] Fast sync complete, auto disabling
INFO [07-10|16:17:42] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.497ms   mgasps=0.000 number=3 hash=32f053…55cfcd
INFO [07-10|16:17:45] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=5.727ms   mgasps=0.000 number=4 hash=27e1b1…3eb10d
> miner.start()                 //开始挖矿
INFO [07-10|16:17:49] Updated mining threads                   threads=0
INFO [07-10|16:17:49] Transaction pool price threshold updated price=18000000000
null
> INFO [07-10|16:17:49] Starting mining operation
INFO [07-10|16:17:49] Commit new mining work                   number=5 txs=0 uncles=0 elapsed=222.952µs
INFO [07-10|16:17:54] Successfully sealed new block            number=5 hash=89aac9…a8d74f
INFO [07-10|16:17:54] 🔨 mined potential block                  number=5 hash=89aac9…a8d74f
INFO [07-10|16:17:54] Commit new mining work                   number=6 txs=0 uncles=0 elapsed=188.804µs
INFO [07-10|16:18:01] Successfully sealed new block            number=6 hash=bba28f…c1bfa1
INFO [07-10|16:18:01] 🔨 mined potential block                  number=6 hash=bba28f…c1bfa1
INFO [07-10|16:18:01] Commit new mining work                   number=7 txs=0 uncles=0 elapsed=193.141µs
INFO [07-10|16:18:03] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.919ms  mgasps=0.000 number=7 hash=a76e32…157218
INFO [07-10|16:18:03] Commit new mining work                   number=8 txs=0 uncles=0 elapsed=220.731µs
INFO [07-10|16:18:04] Successfully sealed new block            number=8 hash=0efa56…f79d0d
INFO [07-10|16:18:04] 🔨 mined potential block                  number=8 hash=0efa56…f79d0d
INFO [07-10|16:18:04] Commit new mining work                   number=9 txs=0 uncles=0 elapsed=205.354µs
INFO [07-10|16:18:05] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=51.051ms  mgasps=0.000 number=9 hash=7d5468…a96e58
INFO [07-10|16:18:05] Commit new mining work                   number=10 txs=0 uncles=0 elapsed=204.347µs
INFO [07-10|16:18:06] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=5.717ms   mgasps=0.000 number=10 hash=d1e4df…3eee60
INFO [07-10|16:18:06] Commit new mining work                   number=11 txs=0 uncles=0 elapsed=139.709µs
INFO [07-10|16:18:06] 🔗 block reached canonical chain          number=5  hash=89aac9…a8d74f
INFO [07-10|16:18:07] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=43.422ms  mgasps=0.000 number=11 hash=6e38a7…466d9e
INFO [07-10|16:18:07] Commit new mining work                   number=12 txs=0 uncles=0 elapsed=137.309µs
INFO [07-10|16:18:07] 🔗 block reached canonical chain          number=6  hash=bba28f…c1bfa1
INFO [07-10|16:18:07] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=31.060ms  mgasps=0.000 number=12 hash=383ef1…471bc4
INFO [07-10|16:18:07] Commit new mining work                   number=13 txs=0 uncles=0 elapsed=214.302µs
INFO [07-10|16:18:10] Successfully sealed new block            number=13 hash=96957a…7ec856
INFO [07-10|16:18:10] 🔗 block reached canonical chain          number=8  hash=0efa56…f79d0d
INFO [07-10|16:18:10] 🔨 mined potential block                  number=13 hash=96957a…7ec856
INFO [07-10|16:18:10] Commit new mining work                   number=14 txs=0 uncles=0 elapsed=192.709µs
INFO [07-10|16:18:11] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=35.398ms  mgasps=0.000 number=14 hash=1f3501…d1c2eb
INFO [07-10|16:18:11] Commit new mining work                   number=15 txs=0 uncles=0 elapsed=165.878µs
INFO [07-10|16:18:16] Successfully sealed new block            number=15 hash=91e27c…384c15
INFO [07-10|16:18:16] 🔨 mined potential block                  number=15 hash=91e27c…384c15
INFO [07-10|16:18:16] Commit new mining work                   number=16 txs=0 uncles=0 elapsed=208.407µs
INFO [07-10|16:18:19] Successfully sealed new block            number=16 hash=3702aa…1c137d
INFO [07-10|16:18:19] 🔨 mined potential block                  number=16 hash=3702aa…1c137d
INFO [07-10|16:18:19] Commit new mining work                   number=17 txs=0 uncles=0 elapsed=193.788µs
INFO [07-10|16:18:19] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=33.253ms  mgasps=0.000 number=17 hash=d1f107…808bc1
INFO [07-10|16:18:19] Commit new mining work                   number=18 txs=0 uncles=0 elapsed=203.359µs
INFO [07-10|16:18:21] Successfully sealed new block            number=18 hash=39f251…82552c
INFO [07-10|16:18:21] 🔗 block reached canonical chain          number=13 hash=96957a…7ec856
INFO [07-10|16:18:21] 🔨 mined potential block                  number=18 hash=39f251…82552c
INFO [07-10|16:18:21] Commit new mining work                   number=19 txs=0 uncles=0 elapsed=178.145µs
INFO [07-10|16:18:29] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=189.761ms mgasps=0.000 number=19 hash=224266…2454e3
INFO [07-10|16:18:29] Commit new mining work                   number=20 txs=0 uncles=0 elapsed=236.111µs
INFO [07-10|16:18:29] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=10.490ms  mgasps=0.000 number=20 hash=0a2eee…e96c12
INFO [07-10|16:18:29] Commit new mining work                   number=21 txs=0 uncles=0 elapsed=170.437µs
INFO [07-10|16:18:29] 🔗 block reached canonical chain          number=15 hash=91e27c…384c15
INFO [07-10|16:18:35] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.701ms  mgasps=0.000 number=21 hash=5d04d1…937b96
INFO [07-10|16:18:35] Commit new mining work                   number=22 txs=0 uncles=0 elapsed=163.041µs
INFO [07-10|16:18:35] 🔗 block reached canonical chain          number=16 hash=3702aa…1c137d
INFO [07-10|16:18:39] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=12.666ms  mgasps=0.000 number=22 hash=02dd21…1234c9
INFO [07-10|16:18:39] Commit new mining work                   number=23 txs=0 uncles=0 elapsed=221.557µs
INFO [07-10|16:18:44] Successfully sealed new block            number=23 hash=ae15cc…99b678
INFO [07-10|16:18:44] 🔗 block reached canonical chain          number=18 hash=39f251…82552c
INFO [07-10|16:18:44] 🔨 mined potential block                  number=23 hash=ae15cc…99b678
INFO [07-10|16:18:44] Commit new mining work                   number=24 txs=0 uncles=0 elapsed=173.636µs
INFO [07-10|16:18:49] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.639ms  mgasps=0.000 number=24 hash=cedfb1…3a7ab8
INFO [07-10|16:18:49] Commit new mining work                   number=25 txs=0 uncles=0 elapsed=215.974µs
INFO [07-10|16:19:00] Successfully sealed new block            number=25 hash=d9aa40…7cafbb
INFO [07-10|16:19:00] 🔨 mined potential block                  number=25 hash=d9aa40…7cafbb
INFO [07-10|16:19:00] Commit new mining work                   number=26 txs=0 uncles=0 elapsed=178.11µs
INFO [07-10|16:19:02] Successfully sealed new block            number=26 hash=6bc773…3fe9c2
INFO [07-10|16:19:02] 🔨 mined potential block                  number=26 hash=6bc773…3fe9c2
INFO [07-10|16:19:02] Commit new mining work                   number=27 txs=0 uncles=0 elapsed=243.434µs
INFO [07-10|16:19:03] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=31.723ms  mgasps=0.000 number=27 hash=701ed0…b2c0d6
INFO [07-10|16:19:03] Commit new mining work                   number=28 txs=0 uncles=0 elapsed=228.32µs
INFO [07-10|16:19:06] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.797ms  mgasps=0.000 number=28 hash=5648b4…10dfc6
INFO [07-10|16:19:06] Commit new mining work                   number=29 txs=0 uncles=0 elapsed=178.085µs
INFO [07-10|16:19:06] 🔗 block reached canonical chain          number=23 hash=ae15cc…99b678
INFO [07-10|16:19:06] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.227ms  mgasps=0.000 number=29 hash=677fe0…f0928c
INFO [07-10|16:19:06] Commit new mining work                   number=30 txs=0 uncles=0 elapsed=169.548µs
INFO [07-10|16:19:08] Successfully sealed new block            number=30 hash=ddc6b7…c61dde
INFO [07-10|16:19:08] 🔗 block reached canonical chain          number=25 hash=d9aa40…7cafbb
INFO [07-10|16:19:08] 🔨 mined potential block                  number=30 hash=ddc6b7…c61dde
INFO [07-10|16:19:08] Commit new mining work                   number=31 txs=0 uncles=0 elapsed=197.239µs
INFO [07-10|16:19:09] Successfully sealed new block            number=31 hash=3cbd22…b887bd
INFO [07-10|16:19:09] 🔗 block reached canonical chain          number=26 hash=6bc773…3fe9c2
INFO [07-10|16:19:09] 🔨 mined potential block                  number=31 hash=3cbd22…b887bd
INFO [07-10|16:19:09] Commit new mining work                   number=32 txs=0 uncles=0 elapsed=200.332µs
INFO [07-10|16:19:10] Successfully sealed new block            number=32 hash=1587b3…246e72
INFO [07-10|16:19:10] 🔨 mined potential block                  number=32 hash=1587b3…246e72
INFO [07-10|16:19:10] Commit new mining work                   number=33 txs=0 uncles=0 elapsed=187.676µs
INFO [07-10|16:19:13] Successfully sealed new block            number=33 hash=f9f1c9…ab7420
INFO [07-10|16:19:13] 🔨 mined potential block                  number=33 hash=f9f1c9…ab7420
INFO [07-10|16:19:13] Commit new mining work                   number=34 txs=0 uncles=0 elapsed=199.668µs
INFO [07-10|16:19:23] Successfully sealed new block            number=34 hash=d1071f…cba281
INFO [07-10|16:19:23] 🔨 mined potential block                  number=34 hash=d1071f…cba281
INFO [07-10|16:19:23] Commit new mining work                   number=35 txs=0 uncles=0 elapsed=209.857µs
INFO [07-10|16:19:24] Successfully sealed new block            number=35 hash=0a809f…5197ea
INFO [07-10|16:19:24] 🔗 block reached canonical chain          number=30 hash=ddc6b7…c61dde
INFO [07-10|16:19:24] 🔨 mined potential block                  number=35 hash=0a809f…5197ea
INFO [07-10|16:19:24] Commit new mining work                   number=36 txs=0 uncles=0 elapsed=182.535µs
INFO [07-10|16:19:25] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.340ms  mgasps=0.000 number=36 hash=5d5b36…e713ce
INFO [07-10|16:19:25] Commit new mining work                   number=37 txs=0 uncles=0 elapsed=161.749µs
INFO [07-10|16:19:25] 🔗 block reached canonical chain          number=31 hash=3cbd22…b887bd
INFO [07-10|16:19:25] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=45.270ms  mgasps=0.000 number=37 hash=afe37e…30bc0e
INFO [07-10|16:19:25] Commit new mining work                   number=38 txs=0 uncles=0 elapsed=186.576µs
INFO [07-10|16:19:25] 🔗 block reached canonical chain          number=32 hash=1587b3…246e72
INFO [07-10|16:19:27] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=5.954ms   mgasps=0.000 number=38 hash=bf33e2…f3753d
INFO [07-10|16:19:27] Commit new mining work                   number=39 txs=0 uncles=0 elapsed=163.79µs
INFO [07-10|16:19:27] 🔗 block reached canonical chain          number=33 hash=f9f1c9…ab7420
INFO [07-10|16:19:29] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=10.451ms  mgasps=0.000 number=39 hash=4d1a32…00932d
INFO [07-10|16:19:29] Commit new mining work                   number=40 txs=0 uncles=0 elapsed=157.565µs
INFO [07-10|16:19:29] 🔗 block reached canonical chain          number=34 hash=d1071f…cba281
INFO [07-10|16:19:30] Successfully sealed new block            number=40 hash=efaf6a…b34923
INFO [07-10|16:19:30] 🔗 block reached canonical chain          number=35 hash=0a809f…5197ea
INFO [07-10|16:19:30] 🔨 mined potential block                  number=40 hash=efaf6a…b34923
INFO [07-10|16:19:30] Commit new mining work                   number=41 txs=0 uncles=0 elapsed=173.754µs
INFO [07-10|16:19:37] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.379ms  mgasps=0.000 number=41 hash=5a192e…713c7d
INFO [07-10|16:19:37] Commit new mining work                   number=42 txs=0 uncles=0 elapsed=193.018µs
INFO [07-10|16:19:39] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=17.653ms  mgasps=0.000 number=42 hash=ca1acf…44033f
INFO [07-10|16:19:39] Commit new mining work                   number=43 txs=0 uncles=0 elapsed=205.128µs
INFO [07-10|16:19:40] Successfully sealed new block            number=43 hash=025d91…206c55
INFO [07-10|16:19:40] 🔨 mined potential block                  number=43 hash=025d91…206c55
INFO [07-10|16:19:40] Commit new mining work                   number=44 txs=0 uncles=0 elapsed=179.333µs
INFO [07-10|16:19:40] Successfully sealed new block            number=44 hash=59dfd5…1fe8b2
INFO [07-10|16:19:40] 🔨 mined potential block                  number=44 hash=59dfd5…1fe8b2
INFO [07-10|16:19:40] Commit new mining work                   number=45 txs=0 uncles=0 elapsed=173.89µs
INFO [07-10|16:19:41] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=12.526ms  mgasps=0.000 number=45 hash=02d013…969d28
INFO [07-10|16:19:41] Commit new mining work                   number=46 txs=0 uncles=0 elapsed=205.418µs
INFO [07-10|16:19:41] 🔗 block reached canonical chain          number=40 hash=efaf6a…b34923
INFO [07-10|16:19:45] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.957ms  mgasps=0.000 number=46 hash=bfd138…e23e84
INFO [07-10|16:19:45] Commit new mining work                   number=47 txs=0 uncles=0 elapsed=171.429µs
INFO [07-10|16:19:50] Successfully sealed new block            number=47 hash=ebf08b…9fba42
INFO [07-10|16:19:50] 🔨 mined potential block                  number=47 hash=ebf08b…9fba42
INFO [07-10|16:19:50] Commit new mining work                   number=48 txs=0 uncles=0 elapsed=177.808µs
INFO [07-10|16:19:53] Successfully sealed new block            number=48 hash=d284d4…54eb55
INFO [07-10|16:19:53] 🔗 block reached canonical chain          number=43 hash=025d91…206c55
INFO [07-10|16:19:53] 🔨 mined potential block                  number=48 hash=d284d4…54eb55
INFO [07-10|16:19:53] Commit new mining work                   number=49 txs=0 uncles=0 elapsed=187.312µs
INFO [07-10|16:19:54] Successfully sealed new block            number=49 hash=167474…e98b52
INFO [07-10|16:19:54] 🔗 block reached canonical chain          number=44 hash=59dfd5…1fe8b2
INFO [07-10|16:19:54] 🔨 mined potential block                  number=49 hash=167474…e98b52
INFO [07-10|16:19:54] Commit new mining work                   number=50 txs=0 uncles=0 elapsed=195.133µs
INFO [07-10|16:19:56] Successfully sealed new block            number=50 hash=1386c8…cc0e9a
INFO [07-10|16:19:56] 🔨 mined potential block                  number=50 hash=1386c8…cc0e9a
INFO [07-10|16:19:56] Commit new mining work                   number=51 txs=0 uncles=0 elapsed=186.415µs
INFO [07-10|16:19:56] Successfully sealed new block            number=51 hash=d5a444…a75bae
INFO [07-10|16:19:56] 🔨 mined potential block                  number=51 hash=d5a444…a75bae
INFO [07-10|16:19:56] Commit new mining work                   number=52 txs=0 uncles=0 elapsed=182.232µs
INFO [07-10|16:19:57] Successfully sealed new block            number=52 hash=0e69bb…31dbc2
INFO [07-10|16:19:57] 🔗 block reached canonical chain          number=47 hash=ebf08b…9fba42
INFO [07-10|16:19:57] Commit new mining work                   number=53 txs=0 uncles=0 elapsed=177.587µs
INFO [07-10|16:19:57] 🔨 mined potential block                  number=52 hash=0e69bb…31dbc2
INFO [07-10|16:19:58] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=11.440ms  mgasps=0.000 number=53 hash=4cba89…ab7b91
INFO [07-10|16:19:58] Commit new mining work                   number=54 txs=0 uncles=0 elapsed=168.047µs
INFO [07-10|16:19:58] 🔗 block reached canonical chain          number=48 hash=d284d4…54eb55
INFO [07-10|16:19:59] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.458ms   mgasps=0.000 number=54 hash=32a641…4517bd
INFO [07-10|16:19:59] Commit new mining work                   number=55 txs=0 uncles=0 elapsed=188.587µs
INFO [07-10|16:19:59] 🔗 block reached canonical chain          number=49 hash=167474…e98b52
INFO [07-10|16:20:04] Successfully sealed new block            number=55 hash=94d9e1…e05702
INFO [07-10|16:20:04] 🔗 block reached canonical chain          number=50 hash=1386c8…cc0e9a
INFO [07-10|16:20:04] 🔨 mined potential block                  number=55 hash=94d9e1…e05702
INFO [07-10|16:20:04] Commit new mining work                   number=56 txs=0 uncles=0 elapsed=188.541µs
INFO [07-10|16:20:07] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=53.490ms  mgasps=0.000 number=56 hash=7e4656…9c057e
INFO [07-10|16:20:07] Commit new mining work                   number=57 txs=0 uncles=0 elapsed=197.936µs
INFO [07-10|16:20:07] 🔗 block reached canonical chain          number=51 hash=d5a444…a75bae
INFO [07-10|16:20:08] Successfully sealed new block            number=57 hash=23c012…75a525
INFO [07-10|16:20:08] 🔗 block reached canonical chain          number=52 hash=0e69bb…31dbc2
INFO [07-10|16:20:08] 🔨 mined potential block                  number=57 hash=23c012…75a525
INFO [07-10|16:20:08] Commit new mining work                   number=58 txs=0 uncles=0 elapsed=199.091µs
INFO [07-10|16:20:10] Successfully sealed new block            number=58 hash=6f0e7d…87085b
INFO [07-10|16:20:10] 🔨 mined potential block                  number=58 hash=6f0e7d…87085b
INFO [07-10|16:20:10] Commit new mining work                   number=59 txs=0 uncles=0 elapsed=185.359µs
INFO [07-10|16:20:13] Successfully sealed new block            number=59 hash=4b943a…d4278b
INFO [07-10|16:20:13] 🔨 mined potential block                  number=59 hash=4b943a…d4278b
INFO [07-10|16:20:13] Commit new mining work                   number=60 txs=0 uncles=0 elapsed=189.343µs
INFO [07-10|16:20:16] Successfully sealed new block            number=60 hash=2da19e…5580ba
INFO [07-10|16:20:16] 🔗 block reached canonical chain          number=55 hash=94d9e1…e05702
INFO [07-10|16:20:16] 🔨 mined potential block                  number=60 hash=2da19e…5580ba
INFO [07-10|16:20:16] Commit new mining work                   number=61 txs=0 uncles=0 elapsed=214.345µs
INFO [07-10|16:20:17] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=18.441ms  mgasps=0.000 number=61 hash=31c409…10bafa
INFO [07-10|16:20:17] Commit new mining work                   number=62 txs=0 uncles=0 elapsed=177.137µs
INFO [07-10|16:20:17] Successfully sealed new block            number=62 hash=233323…082958
INFO [07-10|16:20:17] 🔗 block reached canonical chain          number=57 hash=23c012…75a525
INFO [07-10|16:20:17] 🔨 mined potential block                  number=62 hash=233323…082958
INFO [07-10|16:20:17] Commit new mining work                   number=63 txs=0 uncles=0 elapsed=184.42µs
INFO [07-10|16:20:18] Successfully sealed new block            number=63 hash=39ab8d…42c9df
INFO [07-10|16:20:18] 🔗 block reached canonical chain          number=58 hash=6f0e7d…87085b
INFO [07-10|16:20:18] 🔨 mined potential block                  number=63 hash=39ab8d…42c9df
INFO [07-10|16:20:18] Commit new mining work                   number=64 txs=0 uncles=0 elapsed=183.939µs
INFO [07-10|16:20:21] Successfully sealed new block            number=64 hash=e039e0…6281a1
INFO [07-10|16:20:21] 🔗 block reached canonical chain          number=59 hash=4b943a…d4278b
INFO [07-10|16:20:21] 🔨 mined potential block                  number=64 hash=e039e0…6281a1
INFO [07-10|16:20:21] Commit new mining work                   number=65 txs=0 uncles=0 elapsed=170.39µs
INFO [07-10|16:20:22] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.736ms  mgasps=0.000 number=65 hash=a055d8…7fd40b
INFO [07-10|16:20:22] Commit new mining work                   number=66 txs=0 uncles=0 elapsed=242.46µs
INFO [07-10|16:20:22] 🔗 block reached canonical chain          number=60 hash=2da19e…5580ba
INFO [07-10|16:20:23] Successfully sealed new block            number=66 hash=d24b37…f39941
INFO [07-10|16:20:23] 🔨 mined potential block                  number=66 hash=d24b37…f39941
INFO [07-10|16:20:23] Commit new mining work                   number=67 txs=0 uncles=0 elapsed=214.411µs
INFO [07-10|16:20:27] Successfully sealed new block            number=67 hash=e09735…0afc51
INFO [07-10|16:20:27] 🔗 block reached canonical chain          number=62 hash=233323…082958
INFO [07-10|16:20:27] 🔨 mined potential block                  number=67 hash=e09735…0afc51
INFO [07-10|16:20:27] Commit new mining work                   number=68 txs=0 uncles=0 elapsed=258.643µs
INFO [07-10|16:20:29] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=51.970ms  mgasps=0.000 number=68 hash=79d385…1c07cf
INFO [07-10|16:20:29] Commit new mining work                   number=69 txs=0 uncles=0 elapsed=161.829µs
INFO [07-10|16:20:29] 🔗 block reached canonical chain          number=63 hash=39ab8d…42c9df
INFO [07-10|16:20:33] Successfully sealed new block            number=69 hash=5c0996…8ee78f
INFO [07-10|16:20:33] 🔗 block reached canonical chain          number=64 hash=e039e0…6281a1
INFO [07-10|16:20:33] 🔨 mined potential block                  number=69 hash=5c0996…8ee78f
INFO [07-10|16:20:33] Commit new mining work                   number=70 txs=0 uncles=0 elapsed=226.962µs
INFO [07-10|16:20:33] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=32.524ms  mgasps=0.000 number=70 hash=002ce9…46a345
INFO [07-10|16:20:33] Commit new mining work                   number=71 txs=0 uncles=0 elapsed=160.098µs
INFO [07-10|16:20:34] Successfully sealed new block            number=71 hash=60835a…1b69b2
INFO [07-10|16:20:34] 🔗 block reached canonical chain          number=66 hash=d24b37…f39941
INFO [07-10|16:20:34] 🔨 mined potential block                  number=71 hash=60835a…1b69b2
INFO [07-10|16:20:34] Commit new mining work                   number=72 txs=0 uncles=0 elapsed=176.24µs
INFO [07-10|16:20:35] Successfully sealed new block            number=72 hash=8640a3…f6f36b
INFO [07-10|16:20:35] 🔗 block reached canonical chain          number=67 hash=e09735…0afc51
INFO [07-10|16:20:35] 🔨 mined potential block                  number=72 hash=8640a3…f6f36b
INFO [07-10|16:20:35] Commit new mining work                   number=73 txs=0 uncles=0 elapsed=203.144µs
INFO [07-10|16:20:36] Successfully sealed new block            number=73 hash=cd7549…81a389
INFO [07-10|16:20:36] 🔨 mined potential block                  number=73 hash=cd7549…81a389
INFO [07-10|16:20:36] Commit new mining work                   number=74 txs=0 uncles=0 elapsed=221.052µs
INFO [07-10|16:20:40] Successfully sealed new block            number=74 hash=5cbca9…b36fe4
INFO [07-10|16:20:40] 🔗 block reached canonical chain          number=69 hash=5c0996…8ee78f
INFO [07-10|16:20:40] 🔨 mined potential block                  number=74 hash=5cbca9…b36fe4
INFO [07-10|16:20:40] Commit new mining work                   number=75 txs=0 uncles=0 elapsed=208.127µs
INFO [07-10|16:20:40] Successfully sealed new block            number=75 hash=c2c7f9…a70ad2
INFO [07-10|16:20:40] 🔨 mined potential block                  number=75 hash=c2c7f9…a70ad2
INFO [07-10|16:20:40] Commit new mining work                   number=76 txs=0 uncles=0 elapsed=216.551µs
INFO [07-10|16:20:42] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=49.425ms  mgasps=0.000 number=76 hash=98935c…4f7112
INFO [07-10|16:20:42] Commit new mining work                   number=77 txs=0 uncles=0 elapsed=265.712µs
INFO [07-10|16:20:42] 🔗 block reached canonical chain          number=71 hash=60835a…1b69b2
INFO [07-10|16:20:44] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.014ms   mgasps=0.000 number=77 hash=9b2475…8f70d9
INFO [07-10|16:20:44] Commit new mining work                   number=78 txs=0 uncles=0 elapsed=165.118µs
INFO [07-10|16:20:44] 🔗 block reached canonical chain          number=72 hash=8640a3…f6f36b
INFO [07-10|16:20:44] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=21.562ms  mgasps=0.000 number=78 hash=127d0a…5a0d65
INFO [07-10|16:20:44] Commit new mining work                   number=79 txs=0 uncles=0 elapsed=214.815µs
INFO [07-10|16:20:44] 🔗 block reached canonical chain          number=73 hash=cd7549…81a389
INFO [07-10|16:20:46] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=40.251ms  mgasps=0.000 number=79 hash=da6267…0fe8d4
INFO [07-10|16:20:46] Commit new mining work                   number=80 txs=0 uncles=0 elapsed=175.646µs
INFO [07-10|16:20:46] 🔗 block reached canonical chain          number=74 hash=5cbca9…b36fe4
INFO [07-10|16:20:48] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=15.409ms  mgasps=0.000 number=80 hash=112732…27a567
INFO [07-10|16:20:48] Commit new mining work                   number=81 txs=0 uncles=0 elapsed=167.732µs
INFO [07-10|16:20:48] 🔗 block reached canonical chain          number=75 hash=c2c7f9…a70ad2
INFO [07-10|16:20:49] Successfully sealed new block            number=81 hash=768f9a…cb5c3d
INFO [07-10|16:20:49] 🔨 mined potential block                  number=81 hash=768f9a…cb5c3d
INFO [07-10|16:20:49] Commit new mining work                   number=82 txs=0 uncles=0 elapsed=186.806µs
INFO [07-10|16:20:50] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=10.484ms  mgasps=0.000 number=82 hash=3702ea…547ba7
INFO [07-10|16:20:50] Commit new mining work                   number=83 txs=0 uncles=0 elapsed=222.528µs
INFO [07-10|16:20:52] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=18.748ms  mgasps=0.000 number=83 hash=cc5e1a…7d6440
INFO [07-10|16:20:52] Commit new mining work                   number=84 txs=0 uncles=0 elapsed=166.633µs
INFO [07-10|16:20:53] Successfully sealed new block            number=84 hash=49188b…0d5a14
INFO [07-10|16:20:53] 🔨 mined potential block                  number=84 hash=49188b…0d5a14
INFO [07-10|16:20:53] Commit new mining work                   number=85 txs=0 uncles=0 elapsed=232.399µs
INFO [07-10|16:20:56] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=10.671ms  mgasps=0.000 number=85 hash=e0df03…20b44a
INFO [07-10|16:20:56] Commit new mining work                   number=86 txs=0 uncles=0 elapsed=225.833µs
INFO [07-10|16:20:59] Successfully sealed new block            number=86 hash=1f47ea…b85523
INFO [07-10|16:20:59] 🔗 block reached canonical chain          number=81 hash=768f9a…cb5c3d
INFO [07-10|16:20:59] 🔨 mined potential block                  number=86 hash=1f47ea…b85523
INFO [07-10|16:20:59] Commit new mining work                   number=87 txs=0 uncles=0 elapsed=184.627µs
INFO [07-10|16:21:07] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=17.188ms  mgasps=0.000 number=87 hash=032d6d…b37e17
INFO [07-10|16:21:07] Commit new mining work                   number=88 txs=0 uncles=0 elapsed=240.844µs
INFO [07-10|16:21:08] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=39.987ms  mgasps=0.000 number=88 hash=50e65c…f4bd19
INFO [07-10|16:21:08] Commit new mining work                   number=89 txs=0 uncles=0 elapsed=183.685µs
INFO [07-10|16:21:11] Successfully sealed new block            number=89 hash=4b2fdc…6834ed
INFO [07-10|16:21:11] 🔗 block reached canonical chain          number=84 hash=49188b…0d5a14
INFO [07-10|16:21:11] 🔨 mined potential block                  number=89 hash=4b2fdc…6834ed
INFO [07-10|16:21:11] Commit new mining work                   number=90 txs=0 uncles=0 elapsed=192.015µs
INFO [07-10|16:21:12] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=22.016ms  mgasps=0.000 number=90 hash=a2ff61…14fe02
INFO [07-10|16:21:12] Commit new mining work                   number=91 txs=0 uncles=0 elapsed=6.019ms
INFO [07-10|16:21:13] Successfully sealed new block            number=91 hash=7c62e0…2c9241
INFO [07-10|16:21:13] 🔗 block reached canonical chain          number=86 hash=1f47ea…b85523
INFO [07-10|16:21:13] 🔨 mined potential block                  number=91 hash=7c62e0…2c9241
INFO [07-10|16:21:13] Commit new mining work                   number=92 txs=0 uncles=0 elapsed=195.991µs
INFO [07-10|16:21:15] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=57.104ms  mgasps=0.000 number=92 hash=4b8341…3326b9
INFO [07-10|16:21:15] Commit new mining work                   number=93 txs=0 uncles=0 elapsed=209.706µs
INFO [07-10|16:21:16] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.111ms   mgasps=0.000 number=93 hash=b347fb…9dbc80
INFO [07-10|16:21:16] Commit new mining work                   number=94 txs=0 uncles=0 elapsed=211.068µs
INFO [07-10|16:21:16] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.378ms  mgasps=0.000 number=94 hash=2f6ec9…995b64
INFO [07-10|16:21:16] Commit new mining work                   number=95 txs=0 uncles=0 elapsed=149.142µs
INFO [07-10|16:21:16] 🔗 block reached canonical chain          number=89 hash=4b2fdc…6834ed
INFO [07-10|16:21:21] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.190ms   mgasps=0.000 number=95 hash=034389…2e3297
INFO [07-10|16:21:21] Commit new mining work                   number=96 txs=0 uncles=0 elapsed=172.4µs
INFO [07-10|16:21:24] Successfully sealed new block            number=96 hash=7b9d04…df572c
INFO [07-10|16:21:24] 🔗 block reached canonical chain          number=91 hash=7c62e0…2c9241
INFO [07-10|16:21:24] 🔨 mined potential block                  number=96 hash=7b9d04…df572c
INFO [07-10|16:21:24] Commit new mining work                   number=97 txs=0 uncles=0 elapsed=172.25µs
INFO [07-10|16:21:26] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=10.498ms  mgasps=0.000 number=97 hash=9f0e1f…f7d90f
INFO [07-10|16:21:26] Commit new mining work                   number=98 txs=0 uncles=0 elapsed=202.303µs
INFO [07-10|16:21:30] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=5.299ms   mgasps=0.000 number=98 hash=e59b59…63094d
INFO [07-10|16:21:30] Commit new mining work                   number=99 txs=0 uncles=0 elapsed=157.147µs
INFO [07-10|16:21:30] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=59.259ms  mgasps=0.000 number=99 hash=d2721e…f8df74
INFO [07-10|16:21:30] Commit new mining work                   number=100 txs=0 uncles=0 elapsed=168.525µs
INFO [07-10|16:21:35] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=18.919ms  mgasps=0.000 number=100 hash=503e3f…a50bc2
INFO [07-10|16:21:35] Commit new mining work                   number=101 txs=0 uncles=0 elapsed=176.886µs
INFO [07-10|16:21:37] Successfully sealed new block            number=101 hash=12de28…825f1a
INFO [07-10|16:21:37] 🔗 block reached canonical chain          number=96  hash=7b9d04…df572c
INFO [07-10|16:21:37] 🔨 mined potential block                  number=101 hash=12de28…825f1a
INFO [07-10|16:21:37] Commit new mining work                   number=102 txs=0 uncles=0 elapsed=196.364µs
INFO [07-10|16:21:37] Successfully sealed new block            number=102 hash=817f93…4fc54a
INFO [07-10|16:21:37] 🔨 mined potential block                  number=102 hash=817f93…4fc54a
INFO [07-10|16:21:37] Commit new mining work                   number=103 txs=0 uncles=0 elapsed=203.365µs
INFO [07-10|16:21:40] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=27.212ms  mgasps=0.000 number=103 hash=9a48de…a7d504
INFO [07-10|16:21:40] Commit new mining work                   number=104 txs=0 uncles=0 elapsed=181.086µs
INFO [07-10|16:21:40] Successfully sealed new block            number=104 hash=7a3f55…b8bad5
INFO [07-10|16:21:40] 🔨 mined potential block                  number=104 hash=7a3f55…b8bad5
INFO [07-10|16:21:40] Commit new mining work                   number=105 txs=0 uncles=0 elapsed=212.031µs
INFO [07-10|16:21:40] Successfully sealed new block            number=105 hash=a4677c…a58c8d
INFO [07-10|16:21:40] 🔨 mined potential block                  number=105 hash=a4677c…a58c8d
INFO [07-10|16:21:40] Mining too far in the future             wait=2s
> miner.stINFO [07-10|16:21:42] Commit new mining work                   number=106 txs=0 uncles=0 elapsed=2.000s
> miner.stop()INFO [07-10|16:21:44] Successfully sealed new block            number=106 hash=a7ce29…7dfa4d
INFO [07-10|16:21:44] 🔗 block reached canonical chain          number=101 hash=12de28…825f1a
INFO [07-10|16:21:44] 🔨 mined potential block                  number=106 hash=a7ce29…7dfa4d
INFO [07-10|16:21:44] Commit new mining work                   number=107 txs=0 uncles=0 elapsed=3.382ms

true
>


# node2：./geth --networkid 14  --nodiscover --datadir  ./data1  --port  61911 --rpcapi net,eth,web3,personal --rpc  --rpcport 8101 console
WARN [07-10|16:15:08] No etherbase set and no accounts found as default
INFO [07-10|16:15:08] Starting peer-to-peer node               instance=Geth/v1.6.7-stable-ab5646c5/linux-amd64/go1.9.1
INFO [07-10|16:15:08] Allocated cache and file handles         database=/root/go-ethereum/build/bin/data1/geth/chaindata cache=128 handles=1024
WARN [07-10|16:15:08] Upgrading chain database to use sequential keys
INFO [07-10|16:15:08] Initialised chain configuration          config="{ChainID: 15 Homestead: 0 DAO: <nil> DAOSupport: false EIP150: <nil> EIP155: 0 EIP158: 0 Metropolis: <nil> Engine: unknown}"
INFO [07-10|16:15:08] Disk storage enabled for ethash caches   dir=/root/go-ethereum/build/bin/data1/geth/ethash count=3
INFO [07-10|16:15:08] Disk storage enabled for ethash DAGs     dir=/root/.ethash                                 count=2
WARN [07-10|16:15:08] Upgrading db log bloom bins
INFO [07-10|16:15:08] Bloom-bin upgrade completed              elapsed=240.918µs
INFO [07-10|16:15:08] Initialising Ethereum protocol           versions="[63 62]" network=14
INFO [07-10|16:15:08] Database conversion successful
INFO [07-10|16:15:08] Loaded most recent local header          number=0 hash=272003…b62890 td=1024
INFO [07-10|16:15:08] Loaded most recent local full block      number=0 hash=272003…b62890 td=1024
INFO [07-10|16:15:08] Loaded most recent local fast block      number=0 hash=272003…b62890 td=1024
INFO [07-10|16:15:08] Starting P2P networking
INFO [07-10|16:15:08] RLPx listener up                         self="enode://c2cc1ac0a09b1e2d27afa1b6ffc29b3b57a5cc79914db10cd9b2af407c90c7276b2f3d2393ad7a62cb88dea6ebf385c382f5c257de490a6a3e963c4d0a9a8fdb@[::]:61911?discport=0"
INFO [07-10|16:15:08] IPC endpoint opened: /root/go-ethereum/build/bin/data1/geth.ipc
INFO [07-10|16:15:08] HTTP endpoint opened: http://127.0.0.1:8101
Welcome to the Geth JavaScript console!

instance: Geth/v1.6.7-stable-ab5646c5/linux-amd64/go1.9.1
 modules: admin:1.0 debug:1.0 eth:1.0 miner:1.0 net:1.0 personal:1.0 rpc:1.0 txpool:1.0 web3:1.0

> personal.newAccount("data")
"0x127a9c16eb2f1a373d4e390342e68676454db383"
> INFO [07-10|16:16:10] New wallet appeared                      url=keystore:///root/go-ethereum/bu… status=Locked
> admin.nodeInfo
{
  enode: "enode://c2cc1ac0a09b1e2d27afa1b6ffc29b3b57a5cc79914db10cd9b2af407c90c7276b2f3d2393ad7a62cb88dea6ebf385c382f5c257de490a6a3e963c4d0a9a8fdb@[::]:61911?discport=0",
  id: "c2cc1ac0a09b1e2d27afa1b6ffc29b3b57a5cc79914db10cd9b2af407c90c7276b2f3d2393ad7a62cb88dea6ebf385c382f5c257de490a6a3e963c4d0a9a8fdb",
  ip: "::",
  listenAddr: "[::]:61911",
  name: "Geth/v1.6.7-stable-ab5646c5/linux-amd64/go1.9.1",
  ports: {
    discovery: 0,
    listener: 61911
  },
  protocols: {
    eth: {
      difficulty: 1024,
      genesis: "0x2720038ef46044a7a895296b85745294340ecfcedc32f8c9e9802129aeb62890",
      head: "0x2720038ef46044a7a895296b85745294340ecfcedc32f8c9e9802129aeb62890",
      network: 14
    }
  }
}
> admin.addPeer("enode://182fff1f115bc8be4836b305f4394fddc5e9706a863e00bee22e38aba42e3d8e33f1d799db9c26a1b4e289ef60e3e6e4d935f94a0ecc61dc1bddc647c0335243@127.0.0.1:61912?discport=0)
... ^C
> admin.addPeer("enode://182fff1f115bc8be4836b305f4394fddc5e9706a863e00bee22e38aba42e3d8e33f1d799db9c26a1b4e289ef60e3e6e4d935f94a0ecc61dc1bddc647c0335243@[::]:61912?discport=0")
true
> miner.start()
INFO [07-10|16:17:40] Updated mining threads                   threads=0
INFO [07-10|16:17:40] Transaction pool price threshold updated price=18000000000
null
> INFO [07-10|16:17:40] Starting mining operation
INFO [07-10|16:17:40] Commit new mining work                   number=1 txs=0 uncles=0 elapsed=173.727µs
INFO [07-10|16:17:40] Successfully sealed new block            number=1 hash=7f827a…817398
INFO [07-10|16:17:40] 🔨 mined potential block                  number=1 hash=7f827a…817398
INFO [07-10|16:17:40] Commit new mining work                   number=2 txs=0 uncles=0 elapsed=200.405µs
INFO [07-10|16:17:41] Successfully sealed new block            number=2 hash=fdb247…698ce1
INFO [07-10|16:17:41] 🔨 mined potential block                  number=2 hash=fdb247…698ce1
INFO [07-10|16:17:41] Commit new mining work                   number=3 txs=0 uncles=0 elapsed=173.434µs
INFO [07-10|16:17:41] Successfully sealed new block            number=3 hash=32f053…55cfcd
INFO [07-10|16:17:41] 🔨 mined potential block                  number=3 hash=32f053…55cfcd
INFO [07-10|16:17:41] Mining too far in the future             wait=2s
INFO [07-10|16:17:43] Commit new mining work                   number=4 txs=0 uncles=0 elapsed=2.000s
INFO [07-10|16:17:45] Successfully sealed new block            number=4 hash=27e1b1…3eb10d
INFO [07-10|16:17:45] 🔨 mined potential block                  number=4 hash=27e1b1…3eb10d
INFO [07-10|16:17:45] Commit new mining work                   number=5 txs=0 uncles=0 elapsed=183.459µs
INFO [07-10|16:17:57] Generating ethash verification cache     epoch=0 percentage=56 elapsed=3.026s
INFO [07-10|16:17:59] Generated ethash verification cache      epoch=0 elapsed=5.172s
WARN [07-10|16:17:59] Discarded bad propagated block           number=5 hash=89aac9…a8d74f
INFO [07-10|16:18:01] Block synchronisation started
INFO [07-10|16:18:01] Mining aborted due to sync
INFO [07-10|16:18:01] Imported new state entries               count=1 flushed=0 elapsed=84.279µs  processed=1 pending=3 retry=0 duplicate=0 unexpected=0
INFO [07-10|16:18:01] Imported new state entries               count=2 flushed=3 elapsed=116.202µs processed=3 pending=0 retry=0 duplicate=0 unexpected=0
INFO [07-10|16:18:01] Imported new block headers               count=2 elapsed=41.190ms  number=6 hash=bba28f…c1bfa1 ignored=4
INFO [07-10|16:18:01] Imported new chain segment               blocks=2 txs=0 mgas=0.000 elapsed=1.066ms   mgasps=0.000 number=6 hash=bba28f…c1bfa1 ignored=4
INFO [07-10|16:18:01] Fast sync complete, auto disabling
INFO [07-10|16:18:01] Starting mining operation
INFO [07-10|16:18:01] Commit new mining work                   number=7 txs=0 uncles=0 elapsed=193.516µs
INFO [07-10|16:18:01] 🔗 block reached canonical chain          number=1 hash=7f827a…817398
INFO [07-10|16:18:02] Generating ethash verification cache     epoch=1 percentage=63 elapsed=3.012s
INFO [07-10|16:18:03] Successfully sealed new block            number=7 hash=a76e32…157218
INFO [07-10|16:18:03] 🔗 block reached canonical chain          number=2 hash=fdb247…698ce1
INFO [07-10|16:18:03] 🔨 mined potential block                  number=7 hash=a76e32…157218
INFO [07-10|16:18:03] Commit new mining work                   number=8 txs=0 uncles=0 elapsed=170.363µs
INFO [07-10|16:18:04] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=8.654ms   mgasps=0.000 number=8 hash=0efa56…f79d0d
INFO [07-10|16:18:04] Commit new mining work                   number=9 txs=0 uncles=0 elapsed=182.671µs
INFO [07-10|16:18:04] 🔗 block reached canonical chain          number=3 hash=32f053…55cfcd
INFO [07-10|16:18:04] Generated ethash verification cache      epoch=1 elapsed=4.943s
INFO [07-10|16:18:05] Successfully sealed new block            number=9 hash=7d5468…a96e58
INFO [07-10|16:18:05] 🔗 block reached canonical chain          number=4 hash=27e1b1…3eb10d
INFO [07-10|16:18:05] 🔨 mined potential block                  number=9 hash=7d5468…a96e58
INFO [07-10|16:18:05] Commit new mining work                   number=10 txs=0 uncles=0 elapsed=172.215µs
INFO [07-10|16:18:06] Successfully sealed new block            number=10 hash=d1e4df…3eee60
INFO [07-10|16:18:06] 🔨 mined potential block                  number=10 hash=d1e4df…3eee60
INFO [07-10|16:18:06] Commit new mining work                   number=11 txs=0 uncles=0 elapsed=184.358µs
INFO [07-10|16:18:07] Successfully sealed new block            number=11 hash=6e38a7…466d9e
INFO [07-10|16:18:07] 🔨 mined potential block                  number=11 hash=6e38a7…466d9e
INFO [07-10|16:18:07] Commit new mining work                   number=12 txs=0 uncles=0 elapsed=192.474µs
INFO [07-10|16:18:07] Successfully sealed new block            number=12 hash=383ef1…471bc4
INFO [07-10|16:18:07] 🔗 block reached canonical chain          number=7  hash=a76e32…157218
INFO [07-10|16:18:07] 🔨 mined potential block                  number=12 hash=383ef1…471bc4
INFO [07-10|16:18:07] Commit new mining work                   number=13 txs=0 uncles=0 elapsed=157.37µs
INFO [07-10|16:18:10] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=21.188ms  mgasps=0.000 number=13 hash=96957a…7ec856
INFO [07-10|16:18:10] Commit new mining work                   number=14 txs=0 uncles=0 elapsed=235.963µs
INFO [07-10|16:18:11] Successfully sealed new block            number=14 hash=1f3501…d1c2eb
INFO [07-10|16:18:11] 🔗 block reached canonical chain          number=9  hash=7d5468…a96e58
INFO [07-10|16:18:11] 🔨 mined potential block                  number=14 hash=1f3501…d1c2eb
INFO [07-10|16:18:11] Commit new mining work                   number=15 txs=0 uncles=0 elapsed=195.065µs
INFO [07-10|16:18:16] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=58.810ms  mgasps=0.000 number=15 hash=91e27c…384c15
INFO [07-10|16:18:16] Commit new mining work                   number=16 txs=0 uncles=0 elapsed=157.772µs
INFO [07-10|16:18:16] 🔗 block reached canonical chain          number=10 hash=d1e4df…3eee60
INFO [07-10|16:18:19] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=5.666ms   mgasps=0.000 number=16 hash=3702aa…1c137d
INFO [07-10|16:18:19] Commit new mining work                   number=17 txs=0 uncles=0 elapsed=161.663µs
INFO [07-10|16:18:19] 🔗 block reached canonical chain          number=11 hash=6e38a7…466d9e
INFO [07-10|16:18:19] Successfully sealed new block            number=17 hash=d1f107…808bc1
INFO [07-10|16:18:19] 🔗 block reached canonical chain          number=12 hash=383ef1…471bc4
INFO [07-10|16:18:19] 🔨 mined potential block                  number=17 hash=d1f107…808bc1
INFO [07-10|16:18:19] Commit new mining work                   number=18 txs=0 uncles=0 elapsed=192.213µs
INFO [07-10|16:18:21] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=8.742ms   mgasps=0.000 number=18 hash=39f251…82552c
INFO [07-10|16:18:21] Commit new mining work                   number=19 txs=0 uncles=0 elapsed=168.461µs
INFO [07-10|16:18:29] Successfully sealed new block            number=19 hash=224266…2454e3
INFO [07-10|16:18:29] 🔗 block reached canonical chain          number=14 hash=1f3501…d1c2eb
INFO [07-10|16:18:29] Commit new mining work                   number=20 txs=0 uncles=0 elapsed=199.766µs
INFO [07-10|16:18:29] 🔨 mined potential block                  number=19 hash=224266…2454e3
INFO [07-10|16:18:29] Successfully sealed new block            number=20 hash=0a2eee…e96c12
INFO [07-10|16:18:29] 🔨 mined potential block                  number=20 hash=0a2eee…e96c12
INFO [07-10|16:18:29] Commit new mining work                   number=21 txs=0 uncles=0 elapsed=182.412µs
INFO [07-10|16:18:35] Successfully sealed new block            number=21 hash=5d04d1…937b96
INFO [07-10|16:18:35] 🔨 mined potential block                  number=21 hash=5d04d1…937b96
INFO [07-10|16:18:35] Commit new mining work                   number=22 txs=0 uncles=0 elapsed=197.846µs
INFO [07-10|16:18:39] Successfully sealed new block            number=22 hash=02dd21…1234c9
INFO [07-10|16:18:39] 🔗 block reached canonical chain          number=17 hash=d1f107…808bc1
INFO [07-10|16:18:39] 🔨 mined potential block                  number=22 hash=02dd21…1234c9
INFO [07-10|16:18:39] Commit new mining work                   number=23 txs=0 uncles=0 elapsed=168.784µs
INFO [07-10|16:18:44] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=40.540ms  mgasps=0.000 number=23 hash=ae15cc…99b678
INFO [07-10|16:18:44] Commit new mining work                   number=24 txs=0 uncles=0 elapsed=157.231µs
INFO [07-10|16:18:49] Successfully sealed new block            number=24 hash=cedfb1…3a7ab8
INFO [07-10|16:18:49] 🔗 block reached canonical chain          number=19 hash=224266…2454e3
INFO [07-10|16:18:49] 🔨 mined potential block                  number=24 hash=cedfb1…3a7ab8
INFO [07-10|16:18:49] Commit new mining work                   number=25 txs=0 uncles=0 elapsed=187.022µs
INFO [07-10|16:19:00] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=39.070ms  mgasps=0.000 number=25 hash=d9aa40…7cafbb
INFO [07-10|16:19:00] Commit new mining work                   number=26 txs=0 uncles=0 elapsed=165.956µs
INFO [07-10|16:19:00] 🔗 block reached canonical chain          number=20 hash=0a2eee…e96c12
INFO [07-10|16:19:02] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.850ms  mgasps=0.000 number=26 hash=6bc773…3fe9c2
INFO [07-10|16:19:02] Commit new mining work                   number=27 txs=0 uncles=0 elapsed=260.875µs
INFO [07-10|16:19:02] 🔗 block reached canonical chain          number=21 hash=5d04d1…937b96
INFO [07-10|16:19:02] Successfully sealed new block            number=27 hash=701ed0…b2c0d6
INFO [07-10|16:19:02] 🔗 block reached canonical chain          number=22 hash=02dd21…1234c9
INFO [07-10|16:19:02] 🔨 mined potential block                  number=27 hash=701ed0…b2c0d6
INFO [07-10|16:19:02] Commit new mining work                   number=28 txs=0 uncles=0 elapsed=194.204µs
INFO [07-10|16:19:06] Successfully sealed new block            number=28 hash=5648b4…10dfc6
INFO [07-10|16:19:06] 🔨 mined potential block                  number=28 hash=5648b4…10dfc6
INFO [07-10|16:19:06] Commit new mining work                   number=29 txs=0 uncles=0 elapsed=202.546µs
INFO [07-10|16:19:06] Successfully sealed new block            number=29 hash=677fe0…f0928c
INFO [07-10|16:19:06] 🔗 block reached canonical chain          number=24 hash=cedfb1…3a7ab8
INFO [07-10|16:19:06] 🔨 mined potential block                  number=29 hash=677fe0…f0928c
INFO [07-10|16:19:06] Commit new mining work                   number=30 txs=0 uncles=0 elapsed=246.041µs
INFO [07-10|16:19:08] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.979ms  mgasps=0.000 number=30 hash=ddc6b7…c61dde
INFO [07-10|16:19:08] Commit new mining work                   number=31 txs=0 uncles=0 elapsed=161.878µs
INFO [07-10|16:19:09] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.729ms  mgasps=0.000 number=31 hash=3cbd22…b887bd
INFO [07-10|16:19:09] Commit new mining work                   number=32 txs=0 uncles=0 elapsed=221.372µs
INFO [07-10|16:19:10] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.680ms  mgasps=0.000 number=32 hash=1587b3…246e72
INFO [07-10|16:19:10] Commit new mining work                   number=33 txs=0 uncles=0 elapsed=209.075µs
INFO [07-10|16:19:10] 🔗 block reached canonical chain          number=27 hash=701ed0…b2c0d6
INFO [07-10|16:19:13] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=32.681ms  mgasps=0.000 number=33 hash=f9f1c9…ab7420
INFO [07-10|16:19:13] Commit new mining work                   number=34 txs=0 uncles=0 elapsed=161.839µs
INFO [07-10|16:19:13] 🔗 block reached canonical chain          number=28 hash=5648b4…10dfc6
INFO [07-10|16:19:23] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=5.511ms   mgasps=0.000 number=34 hash=d1071f…cba281
INFO [07-10|16:19:23] Commit new mining work                   number=35 txs=0 uncles=0 elapsed=165.66µs
INFO [07-10|16:19:23] 🔗 block reached canonical chain          number=29 hash=677fe0…f0928c
INFO [07-10|16:19:24] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=10.936ms  mgasps=0.000 number=35 hash=0a809f…5197ea
INFO [07-10|16:19:24] Commit new mining work                   number=36 txs=0 uncles=0 elapsed=208.568µs
INFO [07-10|16:19:25] Successfully sealed new block            number=36 hash=5d5b36…e713ce
INFO [07-10|16:19:25] 🔨 mined potential block                  number=36 hash=5d5b36…e713ce
INFO [07-10|16:19:25] Commit new mining work                   number=37 txs=0 uncles=0 elapsed=174.244µs
INFO [07-10|16:19:25] Successfully sealed new block            number=37 hash=afe37e…30bc0e
INFO [07-10|16:19:25] 🔨 mined potential block                  number=37 hash=afe37e…30bc0e
INFO [07-10|16:19:25] Commit new mining work                   number=38 txs=0 uncles=0 elapsed=185.813µs
INFO [07-10|16:19:27] Successfully sealed new block            number=38 hash=bf33e2…f3753d
INFO [07-10|16:19:27] 🔨 mined potential block                  number=38 hash=bf33e2…f3753d
INFO [07-10|16:19:27] Commit new mining work                   number=39 txs=0 uncles=0 elapsed=203.026µs
INFO [07-10|16:19:29] Successfully sealed new block            number=39 hash=4d1a32…00932d
INFO [07-10|16:19:29] 🔨 mined potential block                  number=39 hash=4d1a32…00932d
INFO [07-10|16:19:29] Commit new mining work                   number=40 txs=0 uncles=0 elapsed=185.158µs
INFO [07-10|16:19:30] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=19.954ms  mgasps=0.000 number=40 hash=efaf6a…b34923
INFO [07-10|16:19:30] Commit new mining work                   number=41 txs=0 uncles=0 elapsed=166.485µs
INFO [07-10|16:19:37] Successfully sealed new block            number=41 hash=5a192e…713c7d
INFO [07-10|16:19:37] 🔗 block reached canonical chain          number=36 hash=5d5b36…e713ce
INFO [07-10|16:19:37] 🔨 mined potential block                  number=41 hash=5a192e…713c7d
INFO [07-10|16:19:37] Commit new mining work                   number=42 txs=0 uncles=0 elapsed=214.455µs
INFO [07-10|16:19:39] Successfully sealed new block            number=42 hash=ca1acf…44033f
INFO [07-10|16:19:39] 🔗 block reached canonical chain          number=37 hash=afe37e…30bc0e
INFO [07-10|16:19:39] 🔨 mined potential block                  number=42 hash=ca1acf…44033f
INFO [07-10|16:19:39] Commit new mining work                   number=43 txs=0 uncles=0 elapsed=188.42µs
INFO [07-10|16:19:40] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=13.964ms  mgasps=0.000 number=43 hash=025d91…206c55
INFO [07-10|16:19:40] Commit new mining work                   number=44 txs=0 uncles=0 elapsed=192.406µs
INFO [07-10|16:19:40] 🔗 block reached canonical chain          number=38 hash=bf33e2…f3753d
INFO [07-10|16:19:40] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.053ms   mgasps=0.000 number=44 hash=59dfd5…1fe8b2
INFO [07-10|16:19:40] Commit new mining work                   number=45 txs=0 uncles=0 elapsed=148.364µs
INFO [07-10|16:19:40] 🔗 block reached canonical chain          number=39 hash=4d1a32…00932d
INFO [07-10|16:19:41] Successfully sealed new block            number=45 hash=02d013…969d28
INFO [07-10|16:19:41] 🔨 mined potential block                  number=45 hash=02d013…969d28
INFO [07-10|16:19:41] Commit new mining work                   number=46 txs=0 uncles=0 elapsed=172.843µs
INFO [07-10|16:19:45] Successfully sealed new block            number=46 hash=bfd138…e23e84
INFO [07-10|16:19:45] 🔗 block reached canonical chain          number=41 hash=5a192e…713c7d
INFO [07-10|16:19:45] 🔨 mined potential block                  number=46 hash=bfd138…e23e84
INFO [07-10|16:19:45] Commit new mining work                   number=47 txs=0 uncles=0 elapsed=182.541µs
INFO [07-10|16:19:50] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.450ms   mgasps=0.000 number=47 hash=ebf08b…9fba42
INFO [07-10|16:19:50] Commit new mining work                   number=48 txs=0 uncles=0 elapsed=182.578µs
INFO [07-10|16:19:50] 🔗 block reached canonical chain          number=42 hash=ca1acf…44033f
INFO [07-10|16:19:53] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=13.942ms  mgasps=0.000 number=48 hash=d284d4…54eb55
INFO [07-10|16:19:53] Commit new mining work                   number=49 txs=0 uncles=0 elapsed=174.713µs
INFO [07-10|16:19:54] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=20.408ms  mgasps=0.000 number=49 hash=167474…e98b52
INFO [07-10|16:19:54] Commit new mining work                   number=50 txs=0 uncles=0 elapsed=174.961µs
INFO [07-10|16:19:56] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=8.241ms   mgasps=0.000 number=50 hash=1386c8…cc0e9a
INFO [07-10|16:19:56] Commit new mining work                   number=51 txs=0 uncles=0 elapsed=157.609µs
INFO [07-10|16:19:56] 🔗 block reached canonical chain          number=45 hash=02d013…969d28
INFO [07-10|16:19:57] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=16.963ms  mgasps=0.000 number=51 hash=d5a444…a75bae
INFO [07-10|16:19:57] Commit new mining work                   number=52 txs=0 uncles=0 elapsed=191.212µs
INFO [07-10|16:19:57] 🔗 block reached canonical chain          number=46 hash=bfd138…e23e84
INFO [07-10|16:19:57] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=5.413ms   mgasps=0.000 number=52 hash=0e69bb…31dbc2
INFO [07-10|16:19:57] Commit new mining work                   number=53 txs=0 uncles=0 elapsed=166.973µs
INFO [07-10|16:19:58] Successfully sealed new block            number=53 hash=4cba89…ab7b91
INFO [07-10|16:19:58] 🔨 mined potential block                  number=53 hash=4cba89…ab7b91
INFO [07-10|16:19:58] Commit new mining work                   number=54 txs=0 uncles=0 elapsed=209.067µs
INFO [07-10|16:19:59] Successfully sealed new block            number=54 hash=32a641…4517bd
INFO [07-10|16:19:59] 🔨 mined potential block                  number=54 hash=32a641…4517bd
INFO [07-10|16:19:59] Commit new mining work                   number=55 txs=0 uncles=0 elapsed=173.44µs
INFO [07-10|16:20:04] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=13.919ms  mgasps=0.000 number=55 hash=94d9e1…e05702
INFO [07-10|16:20:04] Commit new mining work                   number=56 txs=0 uncles=0 elapsed=186.499µs
INFO [07-10|16:20:07] Successfully sealed new block            number=56 hash=7e4656…9c057e
INFO [07-10|16:20:07] 🔨 mined potential block                  number=56 hash=7e4656…9c057e
INFO [07-10|16:20:07] Commit new mining work                   number=57 txs=0 uncles=0 elapsed=204.905µs
INFO [07-10|16:20:08] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.341ms   mgasps=0.000 number=57 hash=23c012…75a525
INFO [07-10|16:20:08] Commit new mining work                   number=58 txs=0 uncles=0 elapsed=163.719µs
INFO [07-10|16:20:10] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.094ms   mgasps=0.000 number=58 hash=6f0e7d…87085b
INFO [07-10|16:20:10] Commit new mining work                   number=59 txs=0 uncles=0 elapsed=176.604µs
INFO [07-10|16:20:10] 🔗 block reached canonical chain          number=53 hash=4cba89…ab7b91
INFO [07-10|16:20:13] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=43.031ms  mgasps=0.000 number=59 hash=4b943a…d4278b
INFO [07-10|16:20:13] Commit new mining work                   number=60 txs=0 uncles=0 elapsed=157.742µs
INFO [07-10|16:20:13] 🔗 block reached canonical chain          number=54 hash=32a641…4517bd
INFO [07-10|16:20:16] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=5.846ms   mgasps=0.000 number=60 hash=2da19e…5580ba
INFO [07-10|16:20:16] Commit new mining work                   number=61 txs=0 uncles=0 elapsed=165.459µs
INFO [07-10|16:20:16] Successfully sealed new block            number=61 hash=31c409…10bafa
INFO [07-10|16:20:16] 🔗 block reached canonical chain          number=56 hash=7e4656…9c057e
INFO [07-10|16:20:16] 🔨 mined potential block                  number=61 hash=31c409…10bafa
INFO [07-10|16:20:16] Commit new mining work                   number=62 txs=0 uncles=0 elapsed=201.151µs
INFO [07-10|16:20:17] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=22.483ms  mgasps=0.000 number=62 hash=233323…082958
INFO [07-10|16:20:17] Commit new mining work                   number=63 txs=0 uncles=0 elapsed=190.704µs
INFO [07-10|16:20:18] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=18.873ms  mgasps=0.000 number=63 hash=39ab8d…42c9df
INFO [07-10|16:20:18] Commit new mining work                   number=64 txs=0 uncles=0 elapsed=180.401µs
INFO [07-10|16:20:21] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=10.333ms  mgasps=0.000 number=64 hash=e039e0…6281a1
INFO [07-10|16:20:21] Commit new mining work                   number=65 txs=0 uncles=0 elapsed=157.554µs
INFO [07-10|16:20:22] Successfully sealed new block            number=65 hash=a055d8…7fd40b
INFO [07-10|16:20:22] 🔨 mined potential block                  number=65 hash=a055d8…7fd40b
INFO [07-10|16:20:22] Commit new mining work                   number=66 txs=0 uncles=0 elapsed=194.471µs
INFO [07-10|16:20:23] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=10.897ms  mgasps=0.000 number=66 hash=d24b37…f39941
INFO [07-10|16:20:23] Commit new mining work                   number=67 txs=0 uncles=0 elapsed=224.251µs
INFO [07-10|16:20:23] 🔗 block reached canonical chain          number=61 hash=31c409…10bafa
INFO [07-10|16:20:27] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=29.885ms  mgasps=0.000 number=67 hash=e09735…0afc51
INFO [07-10|16:20:27] Commit new mining work                   number=68 txs=0 uncles=0 elapsed=177.656µs
INFO [07-10|16:20:29] Successfully sealed new block            number=68 hash=79d385…1c07cf
INFO [07-10|16:20:29] 🔨 mined potential block                  number=68 hash=79d385…1c07cf
INFO [07-10|16:20:29] Commit new mining work                   number=69 txs=0 uncles=0 elapsed=177.973µs
INFO [07-10|16:20:33] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.409ms   mgasps=0.000 number=69 hash=5c0996…8ee78f
INFO [07-10|16:20:33] Commit new mining work                   number=70 txs=0 uncles=0 elapsed=219.878µs
INFO [07-10|16:20:33] Successfully sealed new block            number=70 hash=002ce9…46a345
INFO [07-10|16:20:33] 🔗 block reached canonical chain          number=65 hash=a055d8…7fd40b
INFO [07-10|16:20:33] 🔨 mined potential block                  number=70 hash=002ce9…46a345
INFO [07-10|16:20:33] Commit new mining work                   number=71 txs=0 uncles=0 elapsed=174.118µs
INFO [07-10|16:20:34] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=61.707ms  mgasps=0.000 number=71 hash=60835a…1b69b2
INFO [07-10|16:20:34] Commit new mining work                   number=72 txs=0 uncles=0 elapsed=160.709µs
INFO [07-10|16:20:35] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=42.239ms  mgasps=0.000 number=72 hash=8640a3…f6f36b
INFO [07-10|16:20:35] Commit new mining work                   number=73 txs=0 uncles=0 elapsed=168.755µs
INFO [07-10|16:20:36] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.199ms   mgasps=0.000 number=73 hash=cd7549…81a389
INFO [07-10|16:20:36] Commit new mining work                   number=74 txs=0 uncles=0 elapsed=170.187µs
INFO [07-10|16:20:36] 🔗 block reached canonical chain          number=68 hash=79d385…1c07cf
INFO [07-10|16:20:40] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=18.747ms  mgasps=0.000 number=74 hash=5cbca9…b36fe4
INFO [07-10|16:20:40] Commit new mining work                   number=75 txs=0 uncles=0 elapsed=166.383µs
INFO [07-10|16:20:40] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=5.953ms   mgasps=0.000 number=75 hash=c2c7f9…a70ad2
INFO [07-10|16:20:40] Commit new mining work                   number=76 txs=0 uncles=0 elapsed=158.058µs
INFO [07-10|16:20:40] 🔗 block reached canonical chain          number=70 hash=002ce9…46a345
INFO [07-10|16:20:42] Successfully sealed new block            number=76 hash=98935c…4f7112
INFO [07-10|16:20:42] 🔨 mined potential block                  number=76 hash=98935c…4f7112
INFO [07-10|16:20:42] Commit new mining work                   number=77 txs=0 uncles=0 elapsed=225.994µs
INFO [07-10|16:20:44] Successfully sealed new block            number=77 hash=9b2475…8f70d9
INFO [07-10|16:20:44] 🔨 mined potential block                  number=77 hash=9b2475…8f70d9
INFO [07-10|16:20:44] Commit new mining work                   number=78 txs=0 uncles=0 elapsed=182.523µs
INFO [07-10|16:20:44] Successfully sealed new block            number=78 hash=127d0a…5a0d65
INFO [07-10|16:20:44] 🔨 mined potential block                  number=78 hash=127d0a…5a0d65
INFO [07-10|16:20:44] Commit new mining work                   number=79 txs=0 uncles=0 elapsed=179.187µs
INFO [07-10|16:20:46] Successfully sealed new block            number=79 hash=da6267…0fe8d4
INFO [07-10|16:20:46] 🔨 mined potential block                  number=79 hash=da6267…0fe8d4
INFO [07-10|16:20:46] Commit new mining work                   number=80 txs=0 uncles=0 elapsed=194.459µs
INFO [07-10|16:20:48] Successfully sealed new block            number=80 hash=112732…27a567
INFO [07-10|16:20:48] 🔨 mined potential block                  number=80 hash=112732…27a567
INFO [07-10|16:20:48] Commit new mining work                   number=81 txs=0 uncles=0 elapsed=197.489µs
INFO [07-10|16:20:49] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=21.300ms  mgasps=0.000 number=81 hash=768f9a…cb5c3d
INFO [07-10|16:20:49] Commit new mining work                   number=82 txs=0 uncles=0 elapsed=165.004µs
INFO [07-10|16:20:49] 🔗 block reached canonical chain          number=76 hash=98935c…4f7112
INFO [07-10|16:20:50] Successfully sealed new block            number=82 hash=3702ea…547ba7
INFO [07-10|16:20:50] 🔗 block reached canonical chain          number=77 hash=9b2475…8f70d9
INFO [07-10|16:20:50] 🔨 mined potential block                  number=82 hash=3702ea…547ba7
INFO [07-10|16:20:50] Commit new mining work                   number=83 txs=0 uncles=0 elapsed=195.099µs
INFO [07-10|16:20:52] Successfully sealed new block            number=83 hash=cc5e1a…7d6440
INFO [07-10|16:20:52] 🔗 block reached canonical chain          number=78 hash=127d0a…5a0d65
INFO [07-10|16:20:52] 🔨 mined potential block                  number=83 hash=cc5e1a…7d6440
INFO [07-10|16:20:52] Commit new mining work                   number=84 txs=0 uncles=0 elapsed=193.616µs
INFO [07-10|16:20:53] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.790ms   mgasps=0.000 number=84 hash=49188b…0d5a14
INFO [07-10|16:20:53] Commit new mining work                   number=85 txs=0 uncles=0 elapsed=215.581µs
INFO [07-10|16:20:53] 🔗 block reached canonical chain          number=79 hash=da6267…0fe8d4
INFO [07-10|16:20:56] Successfully sealed new block            number=85 hash=e0df03…20b44a
INFO [07-10|16:20:56] 🔗 block reached canonical chain          number=80 hash=112732…27a567
INFO [07-10|16:20:56] 🔨 mined potential block                  number=85 hash=e0df03…20b44a
INFO [07-10|16:20:56] Commit new mining work                   number=86 txs=0 uncles=0 elapsed=189.677µs
INFO [07-10|16:20:59] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.578ms  mgasps=0.000 number=86 hash=1f47ea…b85523
INFO [07-10|16:20:59] Commit new mining work                   number=87 txs=0 uncles=0 elapsed=165.617µs
INFO [07-10|16:21:07] Successfully sealed new block            number=87 hash=032d6d…b37e17
INFO [07-10|16:21:07] 🔗 block reached canonical chain          number=82 hash=3702ea…547ba7
INFO [07-10|16:21:07] 🔨 mined potential block                  number=87 hash=032d6d…b37e17
INFO [07-10|16:21:07] Commit new mining work                   number=88 txs=0 uncles=0 elapsed=199.605µs
INFO [07-10|16:21:08] Successfully sealed new block            number=88 hash=50e65c…f4bd19
INFO [07-10|16:21:08] 🔗 block reached canonical chain          number=83 hash=cc5e1a…7d6440
INFO [07-10|16:21:08] 🔨 mined potential block                  number=88 hash=50e65c…f4bd19
INFO [07-10|16:21:08] Commit new mining work                   number=89 txs=0 uncles=0 elapsed=217.921µs
INFO [07-10|16:21:11] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=26.847ms  mgasps=0.000 number=89 hash=4b2fdc…6834ed
INFO [07-10|16:21:11] Commit new mining work                   number=90 txs=0 uncles=0 elapsed=188.346µs
INFO [07-10|16:21:12] Successfully sealed new block            number=90 hash=a2ff61…14fe02
INFO [07-10|16:21:12] 🔗 block reached canonical chain          number=85 hash=e0df03…20b44a
INFO [07-10|16:21:12] 🔨 mined potential block                  number=90 hash=a2ff61…14fe02
INFO [07-10|16:21:12] Commit new mining work                   number=91 txs=0 uncles=0 elapsed=209.489µs
INFO [07-10|16:21:13] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=23.812ms  mgasps=0.000 number=91 hash=7c62e0…2c9241
INFO [07-10|16:21:13] Commit new mining work                   number=92 txs=0 uncles=0 elapsed=168.478µs
INFO [07-10|16:21:15] Successfully sealed new block            number=92 hash=4b8341…3326b9
INFO [07-10|16:21:15] 🔗 block reached canonical chain          number=87 hash=032d6d…b37e17
INFO [07-10|16:21:15] 🔨 mined potential block                  number=92 hash=4b8341…3326b9
INFO [07-10|16:21:15] Commit new mining work                   number=93 txs=0 uncles=0 elapsed=186.5µs
INFO [07-10|16:21:16] Successfully sealed new block            number=93 hash=b347fb…9dbc80
INFO [07-10|16:21:16] 🔗 block reached canonical chain          number=88 hash=50e65c…f4bd19
INFO [07-10|16:21:16] 🔨 mined potential block                  number=93 hash=b347fb…9dbc80
INFO [07-10|16:21:16] Commit new mining work                   number=94 txs=0 uncles=0 elapsed=189.715µs
INFO [07-10|16:21:16] Successfully sealed new block            number=94 hash=2f6ec9…995b64
INFO [07-10|16:21:16] 🔨 mined potential block                  number=94 hash=2f6ec9…995b64
INFO [07-10|16:21:16] Commit new mining work                   number=95 txs=0 uncles=0 elapsed=147.479µs
INFO [07-10|16:21:21] Successfully sealed new block            number=95 hash=034389…2e3297
INFO [07-10|16:21:21] 🔗 block reached canonical chain          number=90 hash=a2ff61…14fe02
INFO [07-10|16:21:21] 🔨 mined potential block                  number=95 hash=034389…2e3297
INFO [07-10|16:21:21] Commit new mining work                   number=96 txs=0 uncles=0 elapsed=204.681µs
INFO [07-10|16:21:24] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=28.092ms  mgasps=0.000 number=96 hash=7b9d04…df572c
INFO [07-10|16:21:24] Commit new mining work                   number=97 txs=0 uncles=0 elapsed=214.124µs
INFO [07-10|16:21:26] Successfully sealed new block            number=97 hash=9f0e1f…f7d90f
INFO [07-10|16:21:26] 🔗 block reached canonical chain          number=92 hash=4b8341…3326b9
INFO [07-10|16:21:26] 🔨 mined potential block                  number=97 hash=9f0e1f…f7d90f
INFO [07-10|16:21:26] Commit new mining work                   number=98 txs=0 uncles=0 elapsed=212.054µs
INFO [07-10|16:21:30] Successfully sealed new block            number=98 hash=e59b59…63094d
INFO [07-10|16:21:30] 🔗 block reached canonical chain          number=93 hash=b347fb…9dbc80
INFO [07-10|16:21:30] 🔨 mined potential block                  number=98 hash=e59b59…63094d
INFO [07-10|16:21:30] Commit new mining work                   number=99 txs=0 uncles=0 elapsed=184.566µs
INFO [07-10|16:21:30] Successfully sealed new block            number=99 hash=d2721e…f8df74
INFO [07-10|16:21:30] 🔗 block reached canonical chain          number=94 hash=2f6ec9…995b64
INFO [07-10|16:21:30] 🔨 mined potential block                  number=99 hash=d2721e…f8df74
INFO [07-10|16:21:30] Commit new mining work                   number=100 txs=0 uncles=0 elapsed=199.428µs
> minerINFO [07-10|16:21:35] Successfully sealed new block            number=100 hash=503e3f…a50bc2
INFO [07-10|16:21:35] 🔗 block reached canonical chain          number=95  hash=034389…2e3297
INFO [07-10|16:21:35] 🔨 mined potential block                  number=100 hash=503e3f…a50bc2
INFO [07-10|16:21:35] Commit new mining work                   number=101 txs=0 uncles=0 elapsed=182.95µs
> miner.stoINFO [07-10|16:21:37] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=14.353ms  mgasps=0.000 number=101 hash=12de28…825f1a
INFO [07-10|16:21:37] Commit new mining work                   number=102 txs=0 uncles=0 elapsed=154.447µs
> miner.stopINFO [07-10|16:21:37] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=13.939ms  mgasps=0.000 number=102 hash=817f93…4fc54a
INFO [07-10|16:21:37] Commit new mining work                   number=103 txs=0 uncles=0 elapsed=199.462µs
INFO [07-10|16:21:37] 🔗 block reached canonical chain          number=97  hash=9f0e1f…f7d90f
> miner.stop()INFO [07-10|16:21:37] Successfully sealed new block            number=103 hash=9a48de…a7d504
INFO [07-10|16:21:37] 🔗 block reached canonical chain          number=98  hash=e59b59…63094d
INFO [07-10|16:21:37] 🔨 mined potential block                  number=103 hash=9a48de…a7d504
INFO [07-10|16:21:37] Mining too far in the future             wait=2s

INFO [07-10|16:21:39] Commit new mining work                   number=104 txs=0 uncles=0 elapsed=2.000s
true
> INFO [07-10|16:21:40] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=10.439ms  mgasps=0.000 number=104 hash=7a3f55…b8bad5
INFO [07-10|16:21:44] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=7.261ms   mgasps=0.000 number=105 hash=a4677c…a58c8d
INFO [07-10|16:21:44] Imported new chain segment               blocks=1 txs=0 mgas=0.000 elapsed=6.051ms   mgasps=0.000 number=106 hash=a7ce29…7dfa4d
> miner.stop()
true
>