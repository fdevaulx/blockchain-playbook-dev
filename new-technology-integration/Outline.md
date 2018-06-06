Other Technology Integration
Technologies
Complementing Technologies (Can stand on its own, but, enhance the business benefit of Blockchain if used in conjunction)

CAL ZEMELMAN:
1.	Machine Learning - artificial is the broad idea of teaching computers to think and act like an intelligent human. Machine learning is a subfield of artificial intelligence that deals with training computers to spot patterns and create predictive models for the future. Within machine learning, there are the ideas of supervised learning, unsupervised learning, and reinforcement learning. All of these might be useful for data. *Impact/Use Case:* Blockchains with a wide variety of data are fertile ground for training machine learning models. Imagine your blockchain stores financial transactions and whether they were found to be fraudulent. You could use a supervised learning technique on data from the blockchain to build a model for detecting fraudulent transactions.

Best Practices:
1. Start small.
2. Use ML as Decision Support Systems, driven by simple rules (initially)

2.	RPA - robotic process automation is the idea of using technology to have a program perform tasks that were previously done by a person. *Impact/Use Case:* Imagine you have a legacy procurement system where purchase orders must be keyed in to a terminal application. You've also implemented a blockchain that stores procurement actions around your agency. You could create an RPA solution that read approved actions from the blockchain and automatically keyed them into the procurement system, reducing labor and increasing the accuracy of those POs.

Best Practices
1. RPA should be considered for a process that doesn't change that often. Otherwise, the maintanance of the code becomes a bottleneck.
2. Choose the RPA tool appropriately. There are numerous tools out therre, understand the benefits of each before choosing the right one.

3.	Big Data Management (including data storage) - big data can mean many things but the classic idea  is that new factors like data volume, velocity, and variability have proved difficult for traditional data processing solutions to handle and required new technology like Hadoop and Spark. *Impact/Use Case:* While blockchain is great for certain use cases, it is _not_ a great solution for high data volumes or complex analytical queries. In other words, if you need to do deep analysis on your transactions, to handle more than a couple transactions per second, or store more than 100GB of data, you may want to pivot from exploring blockchain to a complementary big data solution.

Best Practices:
1. It is best to store and manage any Big Data requirement 'outside' the blockchain (off chain) and provide a pointer to it on-chain.
2. It also means that access requirements to the data have to be resolved ahead of time.

4.	Master Data Management (MDM) - a systematic way of handling important reference data for an organization that should be consistent to make it valuable. For example, if an organization does not have an standardized way of labeling customers but wants to do cross-cutting measures of customer service, they have a problem with MDM. If multiple parties or systems are participating in a blockchain, you must have good MDM in place or you will not be able to extract high quality information from your data. *Impact/Use Case:* if you plan on analyzing the data on your blockchain or using metadata about it for other purposes, you should investigate an MDM strategy to make sure your data remains of a high quality. 

Best Practices:
1. Make the MDM part of the Governance Model and structure.
2. Define the MDM standards as part of the blokchain network design
3. Use MDM to guide the structure of the data / asset to be stored in the Blockchain.

VENKAT KODUMUDI:
5.	Cyber Security
    The term Cyber Security is used to collectively address the controls described in and provided by the NIST 800.3, and FIPS 199 directives that govern Federal Government Systems and OWASP standards for commercial sector. Cyber Security intersects with a Blockchain solution in a couple of areas:
    1. Design and Development of the solution should ensure secure practices are built into the solution, not just to ensure compliance to the standards, but also to ensure the solution is free from hacking, and other unsecure practices.
    2. Ensure compliance to the controls governed by the directives.

6.	Archiving
    Archiving is not a feature of the Blockchain. As the number of blocks in the blockchain increases, the finite storage resources become dear to the success of the implementation. Archiving is one way to ensure enough storage is available for the operations of the system by moving a subset of data based on certain rules into an offline / somewhat difficult to access storage (also sometimes referred to as 'offline' storage). Archiving can get very complicated depending on the requirements. There can be tiers of archiving, such as semi-instantaneous access, and completely offline.
Archiving is a prominent concept, if designed or implemented incorrectly can break a solution. It is espcially acute with Blockchain as the entire premise of Blockchain is based on the fact that 'a blockchain' holds the single source of truth of everything that happened. Some of the things to consider at design time of a Blockchain implementation is to index. Another design concept to consider is to fork the chain when we archive.

7.	Smart Contract (??)
    Please refer to the selection secion of the playbook for a definition of Smart Contract

8.	Messaging Protocols 
    Messaging is used as a mechanism to transfer and transport data between systems that perform specific functions. The systems can be anywhere from entire applications to a small microservice that perform a specific function. Most of these systems can't operate in a silo and need to interact with other systems either to get data from or to give data to. In some cases, the messaging is as simple as just transferring data from one location to another, while in other cases complex transformation is performed to map the data to suite the destination system. Some example of messaging protocols are Web Services, REST services, RPC etc. There are many messaging platforms such as Dell Bhoomi, Mulesoft, Rabbit MQ, IBM MQ Series, Apache Kafka etc.
    
    The importance of messaging in a Blockchain environment is multi fold.
    1. Intra network participant communication
    2. Inter network communication
    3. Communication between the blockchain and the participants
  Typically, the blockchain framework handles all the internal communication within the network. For the communication mechanisms between clients and client and the node, we should consider any one of the concepts listed above. For inter network communication, in speaking between 2 self contained networks, there are tools like Wanchain (wanchain.io) focuses on this technology.

    
9. Identity and Access Management
Identity and Access Management is the core 'entry' point into any application. It also serves as the gate keeper of user roles and responsibilities.

Besides serving similar responsibiities for a blockchain solution, Identity Management can play additional role - in permissioned networks, it can serve as the gate keeper for on-ramping and off-ramping network participants. For permissionless networks, it can simply act as the keeper of the members wanting to connect. It can also serve as the algorithm and mechanism for assigning and tracking the nodes that validate, and write the blocks into the chain, and also those who want to serve as a 'decentralized node'.



BRIAN RODRIGUE:
Adjacent Technologies (They can potentially replace Blockchain technology for specific uses)
1.	Cryptography - the practice of obfuscating or encrypting information so it is no longer intelligible without a key. You can use cryptography to secure distributed pieces of information with much less overhead than blockchain. For example, imagine you have a compilation of text from different parties that changes over time, much like a GitHub repository. If each participant enables _signed commits_, GitHub uses public/private key pairs to verify that each contribution is from the party that the commit is contributed to. From a technical standpoint, this is much simpler than blockchain and is a service GitHub (and others) can offer as a free service.
2.	Hashgraph
Hashgraph is a new consensus alternative to the blockchain. It uses a gossip protocol that works in the following manner: Every node in Hashgraph can spread signed information (called events) on newly-created transactions and transactions received from others, to its randomly chosen neighbors. These neighbors will aggregate received events with information received from other nodes into a new event, and then send it on to other randomly chosen neighbors. This process continues until all the nodes are aware of the information created or received at the beginning. Due to the rapid convergence property of the gossip protocol, every piece of new information can reach each node in the network in a fast manner.
3.	Distributed Ledger (IPFS) / Distributed Databases  - blockchain is built on top of a technology called distributed ledgers. The "block chaining" feature ensures groups of transactions are immutability linked to one another and is important in an adversarial environment. If you are looking into a system that only needs to exchange data with trusted parties or within an organization, blockchain is likely overkill for your situation. Look into services like Google Cloud Spanner which offers a globally distributed, highly redundant distributed database as a service.

Outline
1.	Intro
2.	Definition of the different technologies and categories
3.	How does each technology integrate / interface with Blockchain
4.	Impact / Benefit / Best Practices
5.	Usecases and examples (one hypothetical usecase, with other examples)
a.	ConOps
b.	Reference Architecture????? – Nice to have
6.	Conclusion / Takeaway
High Level Timeline
ETC – End of August (including review and approval)
