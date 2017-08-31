

关于比特币区块链，我们得搞明白以下这些概念和原理。
#比特币基础

##1、比特币网络
	
	。节点
	
	player
		miner
		user
##2、采矿
	。区块链
	。块
	。难度
##3、交易
	。脚本系统
	。输出
		。输出锁
##4、密钥对和地址
	。私钥
	。公钥
		。数字签名
			签名+验证
	。地址

##5、Merkle tree & SPV


##6、吞吐量 transaction per second(tps)
理论上，比特币系统能达到7tps，但实际上只有3tps。因为共识是需要发生时间的；验证是需要花时间的（帐户余额验证、双重支付判断等）；验证花的时间主要来自比特币对签名的验证，签名验证时基于栈的，验完一笔以后在验另一笔交易。


#比特币进阶

##1、sidechain（侧链）

目前侧链技术主要由Blockstream公司负责开发，该公司由Adam Back领衔。

##2、隔离见证

2017年8月24日，隔离见证正式在比特币主网激活，开启了一个比特币新未来。

##3、Schnorr签名算法

相较于ECDSA，Schnorr签名具有**更短的签名**（64字节，即512比特，而非71～72字节）、更快的签名/验证速度。

Schnorr的**优势**表现在：可实现多重数字签名与批验证，即多个用户对同一消息的签名可聚合成单个，且仅需要单词验证过程。
Schnorr算法是可证安全的，但Schnorr本人申请了专利的。

Q：为什么不选用BLS短签名算法呢？


##4、比特币闪电网络

闪电网络两个核心技术：1、序列到期可撤销合约（Recoverable sequence maturity contract）；2、杂凑时间锁定合约（Hash-time locked contract）。这两大技术共同构成了闪电网络。

目前，闪电网络正在开发中。主要有三个语言的实现，它们分别是C、Go、Scala。

项目地址分别是：

			  https://github.com/ElementsProject/lightning
			  https://github.com/lightningnetwork/lnd
			  https://github.com/acinq/eclair
				
闪电网络的详细理解见博客。

闪电网络的缺点：

#比特币协议有点乱：使用大端数，小端数，固定长度数，变长数，自定义编码（Base58Check），DER编码，各种各样的密码算法。

#如何理解比特币网络是“peer-to-peer 网络”？
1、每一个人（比特币客户端）互相连接，因此这是一个网络。

2、网络上的每个人（比特币客户端）是平等的，因此是同等地位的人（peers）。

#比特币节点（客户端）都要做哪些事？

一个节点要做三件事：遵守游戏规则；共享信息（典型的信息是交易）；保存确认交易的副本。

ps：节点需要共享两类交易：新鲜交易（即最近进入网络的交易）和已确认交易（交易已经被确认并写入文件中，交易块）

#交易数据格式初探


比特币交易分为三类

支付到比特币一般地址的交易Pay-to-PubKeyHash Tx.(P2PKH Tx)

大多数比特币交易都是这种一般类型。一般是从一个用户到另一个用户。

支付到比特币多钱地址的交易Pay-to-Script-Hash Tx.(P2SH Tx)

比特币挖矿生成的交易 coinbase Tx.(coinbase Tx)

##1、搭建比特币全球测试网络

我们以比特币测试网络的一笔交易（txid为b69c545b37321b3d64f288dbc14454656fa058d759c47460781343fd3f33684c）举例。我们通过点击“帮助->调试窗口->控制台”进入Bitcoin Core的RPC控制台，输入help命令可以浏览所有的RPC命令。

输入命令：getrawtransaction "b69c545b37321b3d64f288dbc14454656fa058d759c47460781343fd3f33684c"

显示：

	0100000001b4686d6187217f8983c9ce8afea8876127608c0c2508bdbee1699e0e5be35b790100000069463043021f58ca62ed3b358799977cf4dc4a01558774a1d6361fe1db237eb5ceacbfbfa802205fa52b07ecf17505988b8f46ae99120f5cb4ad3787e08207c52e5f440a6d7b820121036aa0ba6fe367bc7d64de5a34564640355ebf6a6fd7139a6143616e353e4069c0ffffffff0280778e06000000001976a914caaef32e64b2d6465d90a1c9af497066630992a788ac8c3ffc3d000000001976a914e091249ce2d5f43ebcafda20bfc71b3fb15763cd88ac00000000

这就是一笔交易的原始数据，就是二进制数据，保存在区块链文件里面的。

下面我们来仔细解剖一下！

下面是交易原始(raw)数据：

<html>
<body>

	
<a title="The version in Little-Endian (reversed) format, four bytes" alt=" " >01000000</a>  &nbsp;&nbsp;version

<a title="The number of input(s)/UTXO(s)" alt="">01 
</a> &nbsp;&nbsp;inputcount

<a title="Previous transaction output hash, in Little-Endian. This can be found in the transaction input (txid) " alt="">b4686d6187217f8983c9ce8afea8876127608c0c2508bdbee1699e0e5be35b79</a> &nbsp;&nbsp;txid

<a title="Output index output_no of the previous transaction in Little-Endian format." alt="">01000000</a>&nbsp;&nbsp;vout

<a title="The size (bytes) of the scriptSig or Unlocking Script that immediately follows(包括sig+pubkey). This value is in HEX as are all similar numbers and need to convert HEX to DEC to be human readable." alt="">69</a>&nbsp;&nbsp;sigsize

<a title="PUSHDATA 46 - Size (in Bytes) to push to stack. This is also in HEX.">46</a>


<a title="script_asm" alt="">3043021f58ca62ed3b358799977cf4dc4a01558774a1d6361fe1db237eb5ceacbfbfa802205fa52b07ecf17505988b8f</a>


<a title="The signature (DER), first part of the scriptSig/Unlocking Script" alt="">46ae99120f5cb4ad3787e08207c52e5f440a6d7b820121036aa0ba6fe367bc7d64de5a34564640355ebf6a6fd7139a6143616e353e4069c0</a>

<a title="Sequence number, disabled for this transaction. However if non-zero locktime is used, then at least one input must have a seq number below 0xffffffff" alt="">ffffffff</a>&nbsp;&nbsp;sequence


<a title="Number of outputs followed in HEX" alt="">02</a>&nbsp;&nbsp;outputcount

<a title="Value to be transferred in Satoshi(my destination address)" alt="">80778e0600000000</a>&nbsp;&nbsp;amount

<a title="Size (in bytes) of the Locking Script (in this case, P2PKH) which follows. This is also in HEX." alt="">19</a>&nbsp;&nbsp;locksize
<a  title="OP_DUP,part of the scriptPubKey/Locking Script" alt=" ">76
</a>&nbsp;&nbsp;OP_DUP

<a title="OP_HASH160,part of the scriptPubKey/Locking Script" alt="">a9</a>&nbsp;&nbsp;OP_HASH160

<a title="PUSHDATA 14 - Size (in Bytes) to push to stack, part of the scriptPubKey/Locking Script. This is also in HEX." alt="">14</a>

<a title="Hash of the Destination Public Key" alt="">caaef32e64b2d6465d90a1c9af497066630992a7</a>&nbsp;&nbsp;pubKey

<a title="OP_EQUALVERIFY, part of the scriptPubKey/Locking Script." alt="" >88</a>&nbsp;&nbsp;OP_EQUALVERIFY

<a title="OP_CHECKSIG, part of the scriptPubKey/Locking Script." alt="">ac</a>&nbsp;&nbsp;OP_CHECKSIG


<a title="Value to be transferred in Satoshi(change address), in Little-Endian." alt="">8c3ffc3d00000000</a>

<a title="Size (in bytes) of the Locking Script (in this case, P2PKH) which follows. This is also in HEX." alt="">19</a>&nbsp;&nbsp;locksize

<a title="the whole scriptPubkey" alt="">76a914e091249ce2d5f43ebcafda20bfc71b3fb15763cd88ac</a>&nbsp;&nbsp;scriptPubKey

<a title="nLockTime, can be either UNIX time or Block Height depending on usage. Before this time, the transaction cannot be accepted into a block. In this example, nLockTime is 0, meaning that there is no nLockTime specified and thus the transaction is executed immediately.">00000000</a>&nbsp;&nbsp;Locktime
</body>
</html>

##2、 交易原始数据字段解读

###verson

	0100，0000 4个字节（小端）
###inputcount
	
	01  VarInt（大小可变，1～9字节）

	txid（transaction ID） 32字节
	
		b4686d6187217f8983c9ce8afea8876127608c0c2508bdbee1699e0e5be35b79
	
	vout 4字节（小端）

		01000000 （因为每笔交易可能有多个输出，在引用交易时我们得指定具体的输出）

	signaturesize 

	

	signature

	

	sequence  4字节（小端）

		ffff,ffff

###outputcount

	01 VarInt（大小可变，1～9字节）
	
	value  8字节（小端）
	
		80778e0600000000 

	lockingscriptsize

		19  VarInt（可变长度）

	lockingscript
		
		76a914caaef32e64b2d6465d90a1c9af497066630992a788ac

###locktime
	
	0000,0000 4字节（小端）

ps：字段长度
比特币网络上的节点期望每个字段有一定长度。这种结构化格式允许他们运行交易数据，并找出每个字段开始和结束的位置。
	
##3、原始数据对应的JSON格式（人类友好）
JSON中展示的就是大端格式（人类友好格式），能看懂！


	{
	  "txid": "b69c545b37321b3d64f288dbc14454656fa058d759c47460781343fd3f33684c",//大端
	  "hash": "b69c545b37321b3d64f288dbc14454656fa058d759c47460781343fd3f33684c",
	  "size": 224,
	  "vsize": 224,
	  "version": 1,
	  "locktime": 0,
	  "vin": [
	    {
	      "txid": "795be35b0e9e69e1bebd08250c8c60276187a8fe8acec983897f2187616d68b4", //大端
	      "vout": 1,  //
	      "scriptSig": {
	        "asm": "3043021f58ca62ed3b358799977cf4dc4a01558774a1d6361fe1db237eb5ceacbfbfa802205fa52b07ecf17505988b8f46ae99120f5cb4ad3787e08207c52e5f440a6d7b82[ALL] 036aa0ba6fe367bc7d64de5a34564640355ebf6a6fd7139a6143616e353e4069c0",
	        "hex": "463043021f58ca62ed3b358799977cf4dc4a01558774a1d6361fe1db237eb5ceacbfbfa802205fa52b07ecf17505988b8f46ae99120f5cb4ad3787e08207c52e5f440a6d7b820121036aa0ba6fe367bc7d64de5a34564640355ebf6a6fd7139a6143616e353e4069c0"
	      },
	      "sequence": 4294967295  //
	    }
	  ],
	  "vout": [
	    {
	      "value": 1.10000000,
	      "n": 0,
	      "scriptPubKey": {
	        "asm": "OP_DUP OP_HASH160 caaef32e64b2d6465d90a1c9af497066630992a7 OP_EQUALVERIFY OP_CHECKSIG",
	        "hex": "76a914caaef32e64b2d6465d90a1c9af497066630992a788ac",
	        "reqSigs": 1,
	        "type": "pubkeyhash",
	        "addresses": [
	          "myzeNY9Ks1eaJZDGePELhF7q5HrjMQqdgz"
	        ]
	      }
	    }, 
	    {
	      "value": 10.39941516,
	      "n": 1,
	      "scriptPubKey": {
	        "asm": "OP_DUP OP_HASH160 e091249ce2d5f43ebcafda20bfc71b3fb15763cd OP_EQUALVERIFY OP_CHECKSIG",
	        "hex": "76a914e091249ce2d5f43ebcafda20bfc71b3fb15763cd88ac",
	        "reqSigs": 1,
	        "type": "pubkeyhash",
	        "addresses": [
	          "n1zMXjkAGr9jkznTsqEiHY9YX5iKWi9V3K"
	        ]
	      }
	    }
	  ]
	}


从json数据格式不难看出，签名出现在交易的中部。

0100,0000 =version number(little-endian)

0000,0001 =version number(big-endian)


比特币软件和网站显示的时候，交易和块的摘要值都是（从小端转换）十六进制（大端模式），这是人类书写数字的方式。



##block 123，456的原始数据

    010000009500c43a25c624520b5100adf82cb9f9da72fd2447a496bc600b0000000000006cd862370395dedf1da2841ccda0fc489e3039de5f1ccddef0e834991a65600ea6c8cb4db3936a1ae3143991

对原始数据的分析：


<a title="version in liitle-endian format" alt="">01000000</a> 

<a title="previous Block Hash" alt="">9500c43a25c624520b5100adf82cb9f9da72fd2447a496bc600b000000000000</a>

<a title="Merkle Root" alt="">6cd862370395dedf1da2841ccda0fc489e3039de5f1ccddef0e834991a65600ea</a>

<a title="Time" alt="">a6c8cb4d </a>


<a title="Bits" alt="">b3936a1a </a>

<a title="Nonce" alt="">e3143991</a>


##区块头数据结构

字段       				大小        数据

Version    				4字节      little-endian

Previous Block ID		23字节		
	
#创始区块数据格式
##json格式

    {
    
    "hash":"000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f",
    
    "ver":1,
    
    "prev_block":"0000000000000000000000000000000000000000000000000000000000000000",
    
    "mrkl_root":"4a5e1e4baab89f3a32518a88c31bc87f618f76673e2cc77ab2127b7afdeda33b",
    
    "time":1231006505,
    
    "bits":486604799,
    
    "fee":0,
    
    "nonce":2083236893,
    
    "n_tx":1,
    
    "size":285,
    
    "block_index":14849,
    
    "main_chain":true,
    
    "height":0,
    
    "tx":[
    
    {
    
       "lock_time":0,
    
       "ver":1,
    
       "size":204,
    
       "inputs":[
    
      {
    
     "sequence":4294967295,
    
     "script":"04ffff001d0104455468652054696d65732030332f4a616e2f32303039204368616e63656c6c6f72206f6e206272696e6b206f66207365636f6e64206261696c6f757420666f722062616e6b73"
    
      }
       ],
    
       "time":1231006505,
    
       "tx_index":14849,
    
       "vin_sz":1,
    
       "hash":"4a5e1e4baab89f3a32518a88c31bc87f618f76673e2cc77ab2127b7afdeda33b",
    
       "vout_sz":1,
    
       "relayed_by":"0.0.0.0",
    
       "out":[
      {
    
     "addr_tag_link":"https:\/\/en.bitcoin.it\/wiki\/Genesis_block",
    
     "addr_tag":"Genesis of Bitcoin",
    
     "spent":false,
    
     "tx_index":14849,
    
     "type":0,
    
     "addr":"1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa",
    
     "value":5000000000,
    
     "n":0,
     "script":"4104678afdb0fe5548271967f1a67130b7105cd6a828e03909a67962e0ea1f61deb649f6bc3f4cef38c4f35504e51ec112de5c384df7ba0b8d578a4c702b6bf11d5fac"
      }
    
       ]
    }]
     }


##私钥、公钥、地址

**钱包**生成私钥->私钥生成公钥->公钥生成哈希->公钥哈希生成地址->地址用来接收比特币。

ps：注意是钱包帮你生成私钥。不是书上讲的自己选一串256bit的随机数。那个是为了讲原理。**钱包的核心就是私钥的保存与使用。**

在比特币中，私钥是长度为256bit的无符号整数（32字节）。形如：

    108165236279178312660610114131826512483935470542850824183737259708197206310322 【10进制】

    1110111100100011010110101010110011111001000011011001111101001010101011011101100011001001001011100100101100100101011000101110000111011001111010111001011111110000110111111001101110100011101101010000100000100101100001110011100111001011000000010011110110110010 【二进制】

    ef235aacf90d9f4aadd8c92e4b2562e1d9eb97f0df9ba3b508258739cb013db2 【十六进制】

上面的10进制和二进制表示本质上都是一个数。但在计算中处理的数都是二进制形式。比特币毕竟还是一段程序。

原始的私钥一般采用16进制表示。

    

签名长度有三种：73字节（25%）、72字节（50%）或者71字节（25%）。

公钥分为压缩和非压缩两种。压缩公钥以0x02或0x03开头，占33字节；非压缩公钥以0x04、0x06、0x07开头，占65字节。现在常见的是压缩公钥。

私钥、公钥以及公钥的摘要值在外表上都是经过base58check编码的ASCII码.

参考资料：https://en.bitcoin.it/wiki/Elliptic_Curve_Digital_Signature_Algorithm




the Bitcoin Protocol （true）
Bicoin （true）
the Bitcoin （x）

##further reading

http://learnmeabitcoin.com/browser/node/ （强烈推荐）

http://www.righto.com/2014/02/bitcoins-hard-way-using-raw-bitcoin.html#ref7



