#Hyperledger Fabric


谢林币：一种最小信任的通用数据供给


原文作者：Vitalik Buterin
时间：2014年3月28日

人们一直感兴趣的以太坊的主要应用之一是金融合约和衍生品。虽然金融衍生品已经获得了这样一种声誉：作为高度风险和破坏稳定的设备，且具有丰富投机者的唯一功能，但是其基本概念实际上具有许多合法用途，一些确实帮助人们保护自己免受金融市场的波动。
Fabric文档

#Fabric 》=1.0节点类型（四类）
目前网络中存在以下4种不同类型的服务节点，彼此协作完成整个区块链系统的功能。对网络中节点（peer）角色进行解耦是Fabric设计中的一大创新，这也是联盟链场景下的特殊需求和环境所决定的。

	证书节点（CA）：负责对网络中的所有证书进行管理，提供标准的PKI服务。
	Endorser（背书节点）：负责对交易的提案（proposal）进行检查和背书，模拟交易执行结果；
	Orderer（排序节点）：对所有发往网络中的交易进行排序，将排序后的交易按照配置中的约定整理为区块，之后提交给确认节点进行处理。
	Committer（确认节点）：负责在接受交易结果前再次检查合法性，接受合法交易对账本的修改，并写入区块链结构；
	
v0.6需要每一个节点执行每一笔交易，维护了一个账本和运行共识。但是不能支持隐私交易和机密合约。因此Hyperledger社区想将Fabric打造成为真正模块化的、可扩展的和安全的适用于企业区块链解决方案的基础。对节点来说，最显著的改变是将节点划分为两种peers（endorser和committer）和Consenters。
youtube：building a blockchain for business with the Hyperledger.
从数据结构讲：
State：
——由Peer维护
Ledger：
——由Orderer创建
——由Oderer交付给每一个Peer，每个Peer上维护一个ledger的副本。
Orderer：
——提供原子的广播服务
——Order service类型：
	——Solo（一个）
	——Kafka
	——PBFT
——OrderLedger类型
	——RAM Ledger
	——File Ledger
	——Other
Channel：
——Orderer支持channel
——Client/Peer连接至Orderer的某个（某些）channel
——channel之间不可见
——可同时连接多个channel
——增强了保密性


#Fabric

Fabric包括Fabric、Fabric CA、Fabric SDK（包括Node.js、Python和Java等语言）和fabric-api等，目前是区块链的基础核心平台。











#docker

docker官网：https://www.docker.com

docker的安装包及周边高速镜像：https://get.daocloud.io/

阿里云开源镜像站点：https://mirrors.aliyun.com/

DaoCloud：http://www.daocloud.io/

博客：http://www.widuu.com/docker/index.html




#资源

MLG Blockchain[官网LEARN菜单](https://www.mlgblockchain.com/index.html)cover了Bitcoin、Ethereum、Hyperledger、Ripple、Factom和Eris的教程。

#寻求帮助
https://stackoverflow.com/questions/tagged/hyperledger-fabric


