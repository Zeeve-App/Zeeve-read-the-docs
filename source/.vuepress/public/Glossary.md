# Glossary

#### Access Key



> Access Key ID helps in accessing and controlling the cloud account and services like EC2, S3, SimpleDB, CloudFront, SQS, EMR, RDS, etc. In case of [AWS](https://aws.amazon.com/) its length is 20 alphanumeric characters long like ABCDGHJK1234CBDG123C . It can be shared with others as well.

* * *

#### Bitcoin

> ![img](./images/bitcoin.jpg) Bitcoin is an open source public blockchain in which anyone can participate. Currency exchange in this is termed as Bitcoin, which is having value in stock exchange as well. It is a peer-to-peer technology to operate with no central authority or banks; managing transactions and the issuing of bitcoins is carried out collectively by the network. [Ref.](https://bitcoin.org/en/)

* * *

#### Blockchain

> Blockchain is considered as a chain of blocks. Blocks are nothing but collection of data. Blockchain is an immutable time-stamped series of data that is maintained within a distributed network of peer nodes. These nodes each maintain a copy of the ledger by applying transactions that have been validated by a consensus protocol, grouped into blocks that include a hash that bind each block to the preceding block.

* * *

#### Certificate Authority

> Certificate Authority accorss this documentation refers to HyperLedger Fabric's key component. This component is responsible for issuing identification material like certificates and keys for an organization. 

* * *

#### Cloud

* * *

<!-- #### Credits
>![img](./images/credits.png) Credits is a decentralized blockchain platform built over peer-to-peer principles in order to develop smart contracts and decentralized applications. Smart contracts are aiming to create high-performance applications. [Ref.](https://credits.com/)

* * * -->

#### Distributed Ledger Technology (DLT)
> ![img](./images/dlt.png) Distributed Ledger is a backbone of Blockchain. Literal meaning of Ledger says that a book contains different records, which in turn is distributed in nature. DLT is a digital system which is recording the transactions and their details in distributed manner. Distributed ledger don't have any central data store.
* * *

<!--#### Ethereum

> ![img](./images/ethereum.png) Ethereum is an open-source, public, blockchain based distributed computing platform and operating system which involves smart contract (business logic coded script) functionality. Ether is a token whose blockchain is generated by the Ethereum platform. Ether is a currency used for the transactions between accounts and also used to compensate participating mining nodes for computations performed. [Ref.](https://www.ethereum.org/)

 * * *

 #### Hyperledger Fabric

> ![img](./images/fabric.png) Hyperledger Fabric is an open source enterprise-grade permissioned distributed ledger technology (DLT) platform, designed for use in enterprise contexts, that delivers some key differentiating capabilities over other popular distributed ledger or blockchain platforms. [Ref.](https://hyperledger-fabric.readthedocs.io/en/release-1.4/whatis.html)

* * * -->

#### Inode

* * *

#### Instance Type

> In cloud instance is considered as a node termed as EC2 (Elastic Compute Cloud). Instance type is a term given which varies based upon the hardware configuration of instance created. In Zeeve we have various instance type both in AWS as well as in Azure. For more information click for [AWS Instance Type](https://aws.amazon.com/ec2/instance-types/) and [Azure Instance Type](https://azure.microsoft.com/en-in/pricing/details/virtual-machines/linux/).

* * *

#### IOT

> Internet of Things

* * *


#### Kafka

> Kafka is a message handling system which uses Publish-Subscribe model. Consumers subscribe to the topic to receive new messages, that are published by a Producer. Topics are nothing but messages, so when they become huge in number, then they are split into partitions, and Kafka guarantees that all messages inside a partition are sequentially ordered. Hyperledger Fabric ordering service nodes (OSNs) use the Kafka cluster and provide an ordering service to your blockchain network. Kafka is permissioned voting based consensus type, here leader does the ordering, only in-sync can be voted as leader. 

* * *


#### Node

> Node is an instance of a network. It basically a connection point which is helping in receiving, creating, storing and sending data.

* * *

#### Network

> Network is a collection of nodes/instances. In Zeeve, when you create a network over the cloud then it asks you for providing the number of nodes and other configuration details. Once all the installation and configuration gets over, it results in [[How_to_create_my_first_network|creating]] your Blockchain network.

* * *


#### Orderer

> Orderers are considered as the special nodes, which are helping each peer nodes to have consistent ledger by enabling the interaction of peer nodes and applications participating in the network.


* * *

#### Raft

> Raft based Ordering service in fabric.


* * *

<!-- #### Sawtooth

> ![img](./images/sawtooth.png) Hyperledger Sawtooth is an enterprise blockchain platform for building distributed ledger applications and networks. The design philosophy targets keeping ledgers distributed and making smart contracts safe, particularly for enterprise use. [Ref.](https://sawtooth.hyperledger.org/docs/core/releases/1.0/introduction.html)
> 
> * * * -->


#### Secret Key

> Secret key is used along with Access key in order to access and control the cloud account and services like EC2, S3, SimpleDB, CloudFront, SQS, EMR, RDS, etc. In case of [AWS](https://aws.amazon.com/) its length is 40 alphanumeric-slash-plus characters long like \*\*\*\*\*\*KOsJW/\*\*\*\*\*\*/c\*\*\*\*\*\*\*\*\*+\*\*\*wy . It can't be shared with others.
>
> * * *

#### Smart Contract

> Smart Contract is a piece of code that contains the business logic. It's execution is done in a secured environment. This is the part of the blockchain that ensures validity of data going into it.  
>
> * * *

#### Zookeeper

> Zookeeper is a distributed key-value store, most commonly used to store metadata and handle the mechanics of clustering. It allows clients of the service (the Kafka brokers) to subscribe and have changes sent to them once they happen. This is how brokers know when to switch partition leaders. Zookeeper is also extremely fault-tolerant as it ought to be, since Kafka heavily depends on it.
> * * *