Other Technology Integration
Technologies
Complementing Technologies (Can stand on its own, but, enhance the business benefit of Blockchain if used in conjunction)

CAL ZEMELMAN:
1.	Machine Learning - artificial is the broad idea of teaching computers to think and act like an intelligent human. Machine learning is a subfield of artificial intelligence that deals with training computers to spot patterns and create predictive models for the future. Within machine learning, there are the ideas of supervised learning, unsupervised learning, and reinforcement learning. All of these might be useful for data. *Impact/Use Case:* 
Best Practices for ML:
* Start small.
* Use ML as Decision Support Systems, driven by simple rules (initially)

Use Cases: 
* Blockchains with a wide variety of data are fertile ground for training machine learning models. Imagine your blockchain stores financial transactions and whether they were found to be fraudulent. You could use a supervised learning technique on data from the blockchain to build a model for detecting fraudulent transactions.


2.	RPA - robotic process automation is the idea of using technology to have a program perform tasks that were previously done by a person. 

Best Practices
* RPA should be considered for a process that doesn't change that often. Otherwise, the maintanance of the code becomes a bottleneck.
* Choose the RPA tool appropriately. There are numerous tools out therre, understand the benefits of each before choosing the right one.

Use Cases:
* Imagine you have a legacy procurement system where purchase orders must be keyed in to a terminal application. You've also implemented a blockchain that stores procurement actions around your agency. You could create an RPA solution that read approved actions from the blockchain and automatically keyed them into the procurement system, reducing labor and increasing the accuracy of those POs.

3.	Big Data Management (including data storage) - big data can mean many things but the classic idea  is that new factors like data volume, velocity, and variability have proved difficult for traditional data processing solutions to handle and required new technology like Hadoop and Spark. 

Best Practices:
* It is best to store and manage any Big Data requirement 'outside' the blockchain (off chain) and provide a pointer to it on-chain.
* Access requirements to the data have to be resolved ahead of time.

Use Cases: 
* While blockchain is great for certain use cases, it is _not_ a great solution for high data volumes or complex analytical queries. In other words, if you need to do deep analysis on your transactions, to handle more than a couple transactions per second, or store more than 100GB of data, you may want to pivot from exploring blockchain to a complementary big data solution.

4.	Master Data Management (MDM) - a systematic way of handling important reference data for an organization that should be consistent to make it valuable. For example, if an organization does not have an standardized way of labeling customers but wants to do cross-cutting measures of customer service, they have a problem with MDM. If multiple parties or systems are participating in a blockchain, you must have good MDM in place or you will not be able to extract high quality information from your data. 

Best Practices:
* Make the MDM part of the Governance Model and structure.
* Define the MDM standards as part of the blokchain network design
* Use MDM to guide the structure of the data / asset to be stored in the Blockchain.

Use Cases:
* If you plan on analyzing the data on your blockchain or using metadata about it for other purposes, you should investigate an MDM strategy to make sure your data remains of a high quality. 


VENKAT KODUMUDI:
5.	Cybersecurity
    The work to address the controls described in and provided by the NIST 800.3, and FIPS 199 directives that govern Federal Government Systems and OWASP standards for commercial sector. Cybersecurity intersects with blockchain in a couple of areas. Design and development of the solution should follow best practices are built into the solution, not just to ensure compliance to the controls but to reduce risk. For example, public blockchains expose all transactions at a detail level so care must be taken with sensitive data. 
    
Best Practices:
* Consult the blockchain playbook to decide on the right type of blockchain (e.g. public, private).
* Conduct a standard audit of your solution design before implementation to ensure it is adequately secured. Blockchain does not remove security as a consideration from your IT system.

Use Cases:


6.	Archiving
    Archiving is *not* typically a feature of the Blockchain. As the number of blocks in the blockchain increases, the finite storage resources become dear to the success of the implementation. Archiving is normally one way to ensure enough storage is available for the operations of the system by moving a subset of data based on certain rules into an offline / somewhat difficult to access storage (also sometimes referred to as 'offline' storage). Archiving can get very complicated depending on the requirements. There can be tiers of archiving, such as semi-instantaneous access, and completely offline.

If not designed or implemented incorrectly, lack of archiving can break a solution. It is espcially acute with blockchain as the entire premise is generally based on the fact that 'a blockchain' holds the single source of truth of everything that happened. 

Best Practices:
* If you expect to have a lot of data (hundreds of GB or more), consider indexing or holding a _pointer_ to the large data in the blockchain. For example, if you wanted an immutable record of radiological images, your blockchain might store metadata about the image and a SHA256 hash of the file, while the actual images were kept elsewhere.
* If you do need to support archiving, you could perform a hard fork and modify the software running the blockchain to exclude old blocks.

Use Cases:


7.	Smart Contract (??)
    Please refer to the selection secion of the playbook for a definition of Smart Contract

8.	Messaging Protocols 
    Messaging is used as a mechanism to transfer and transport data between systems that perform specific functions. The systems can be anything from entire applications to a small microservice that perform a specific function. Most of these systems can't operate in a silo and need to interact with other systems either to get data from or to give data to. In some cases, the messaging is as simple as just transferring data from one location to another, while in other cases complex transformation is performed to map the data to suite the destination system. RESTful web services are an example of a common message protocol and integration method. There are many messaging platforms such as Dell Bhoomi, Mulesoft Anypoint, and RabbitMQ. 
    
    
    Best Practices:
    * Your blockchain system will likely not exist on a single node. Make sure you figure out how intra-process communications between the nodes will work to ensure the data is timely and accurate.
    * Your blockchain system will likely hold valuable data that others not participating in the blockchain will want to access. Make sure you figure out how inter-system and inter-organization communication will work. RESTful web service APIs are becoming ubiquituous for this purpose.

Use Cases:
* You may want to setup a blockchain for tracking supply chain movements of goods to guarantee certain requirements are met from initial sourcing. Some of the data is sensitive, so you cannot grant the general public access to the data which may contain sensitive technical specifications or pricing. Consider setting up an API with RESTful web services to allow the public to view a subset of the information or redacted information.
    
9. Identity and Access Management
Identity and Access Management is the core 'entry' point into any application. It also serves as the gate keeper of user roles and responsibilities.

Besides serving similar responsibiities for a blockchain solution, Identity Management can play additional role - in permissioned networks, it can serve as the gate keeper for on-ramping and off-ramping network participants. For permissionless networks, it can simply act as the keeper of the members wanting to connect. It can also serve as the algorithm and mechanism for assigning and tracking the nodes that validate, and write the blocks into the chain, and also those who want to serve as a 'decentralized node'.

Best Practice:
* Decide how your system is going to handle identity and access management. Is this a public blockchain anyone can join? If not, how will you confirm identity? Look into the mutual exchange of TLS certificates for system-to-system communications so that both parties can confirm the other party holds a private key matching the public key that they identify themselves with.

Use Cases:


10. Geospatial or GEOINT - Geospatial, location-based application, and GEOINT, Geospatial Intelligence, are becoming more prevalent across all industries and allows for seamless sharing of constantly updated locational data.  Integrating with Blockchain provides updated status of each asset and each contract along with verification and history for each.  Geospatial and Blockchain integration improves a longstanding issue with the accuracy and currency of all geospatial source data.  There are many use cases for Public and Private Blockchain integration with GEOINT.

Best Practices:

    * Consider validation processes for open-source and public location assets versus proprietary, sensitive or classified location assets.  In a public blockchain the validation process can take time.  In the private blockchain the number of users can be restricted by invitation only and the rules of governing can be more easily changed by the administrators.  Backtracking (correcting) transactions may be permitted by them quickly as malfunctioning nodes can be quickly spotted and repaired in a private blockchain.
    * Decide and assign roles along with identity and access management processes up front for public or private blockchains.
    * In the private blockchain space, identify a liaison to gain consensus with your mission partners on processes for validation for proprietary, sensitive and classified assets at the start.

Use Cases:

Law enforcement evidence can be tracked, fraud and abuse are more easily identified and trafficking of humans, weapons, drugs, wildlife and more can be affected by integrating GEOINT and Blockchain.  When integrating Artificial Intelligence with GEOINT and Blockchain you can also manage your Internet-Of-Things and Facilities Management seamlessly.  Validation and automation for the identification of persons, vehicles, structures, etc. from all types of location-based imagery is already underway.  Some public and private geospatial blockchain use cases can include advertising and marketing, land transactions, street networks, terrain models, aerial or satellite imagery, LiDAR, UAVs like drones negotiating use of air space and geotagged blockchain election ballots.


##Adjacent Technologies 
(They can potentially replace Blockchain technology for specific uses)
1.	Cryptography - the practice of obfuscating or encrypting information so it is no longer intelligible without a key. You can use cryptography to secure distributed pieces of information with much less overhead than blockchain. For example, imagine you have a compilation of text from different parties that changes over time, much like a GitHub repository. If each participant enables _signed commits_, GitHub uses public/private key pairs to verify that each contribution is from the party that the commit is contributed to. From a technical standpoint, this is much simpler than blockchain and is a service GitHub (and others) can offer as a free service.


Best Practices:
* As with any password / key, ensure the private key can't be stolen
* Use the highest form of encryption available for the keys - for example SHA-256
* A proper place to use this in lieu of Blockchain would be when you don't need a validation flow for the source of truth, and you are just storing the data securely.


2.	Hashgraph
Hashgraph is a new consensus alternative to the blockchain. It uses a gossip protocol that works in the following manner: Every node in Hashgraph can spread signed information (called events) on newly-created transactions and transactions received from others, to its randomly chosen neighbors. These neighbors will aggregate received events with information received from other nodes into a new event, and then send it on to other randomly chosen neighbors. This process continues until all the nodes are aware of the information created or received at the beginning. Due to the rapid convergence property of the gossip protocol, every piece of new information can reach each node in the network in a fast manner.

Best Practices:
* Consider the pros and cons of hashgraph vs blockchain as compared to your requirements. Do you expect the data to be widely distributed across the globe with intermittent connectivity? Do you need immutable blocks of transactions to support a business process? If so, that may cause you to trial one or the other.

3.	Distributed Ledger (IPFS) / Distributed Databases  - blockchain is built on top of a technology called distributed ledgers. The "block chaining" feature ensures groups of transactions are immutability linked to one another and is important in an adversarial environment. If you are looking into a system that only needs to exchange data with trusted parties or within an organization, blockchain is likely overkill for your situation. Look into services like Google Cloud Spanner which offers a globally distributed, highly redundant distributed database as a service.

Best Practices:
* A proper place to use this in lieu of Blockchain would be when you don't need a ordering / validation flow for the source of truth, and you are just storing the data in a distributed fashion. For example, when we talk about distribution of information such as the investment reports, where you aren't transferring an asset, a Distributed Ledger maybe worth investigating.

##Outline
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
