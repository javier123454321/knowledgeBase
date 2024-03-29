- Type:: [[Book]]
- Source:: https://github.com/sherminvo/TokenEconomyBook/wiki
- Author:: [[Shermin Voshmgir]]
- Subject:: [[cryptocurrency]] [[web3]] [[Ethereum]]
- Status:: [[In Progress]]
- Abstract::
    - 
- Summary::
    - [introduction](https://github.com/sherminvo/TokenEconomyBook/wiki/Introduction)
        - Tokens wil be to web3 what websites are for web2. Standards have not emerged from it yet.
    - [Tokenized Networks: Web3, the Stateful Web](https://github.com/sherminvo/TokenEconomyBook/wiki/Tokenized-Networks%3A-Web3%2C-the-Stateful-Web)
        - After 30 years, we still use data in the internet based on the model of a standalone computer. One server has read/write access to the data.
        - This mimics the age when data had to be stored in drives and mailed to share access to it. IP cleared some of the hiccups, but the underlying model did not evolve.
            - The Web2 allowed us to enjoy peer-to-peer (P2P) interactions on a global scale, but always with a middleman: a platform acting as a trusted intermediary between two people who do not know or trust each other.
        - While web2 changes frontend, web3 changes backend
        - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2FJavier-knowledge-graph%2FN-3APkuIo1.png?alt=media&token=8949b95e-cd8b-480b-af7b-a76168c89bf6)
    - [Keeping Track of the Tokens: Bitcoin, Blockchain, & Other Distributed Ledgers](https://github.com/sherminvo/TokenEconomyBook/wiki/Keeping-Track-of-the-Tokens%3A-Bitcoin%2C-Blockchain%2C-%26-Other-Distributed-Ledgers)
        - Distributed control of the network
        - Byzantine Generals Problem, what to do when a system which relies on all the actors gets infiltrated by a bad actor
            - The cost of hcanging the history of the network (introducing a double spend) is prohibitively high. To change the past, you need to go back to rearange the previous blocks, hash them all, find.a nonce which gives you the correct hashed state, do the computation for every node, and do it faster than new nodes are being produced. You need to maintain over 51% of the hashrate of bitcoin for a long period of time for that to be effective.
            - A bad actor could ONLY double spend, because any information put into a node has to be valid as per the protocol rules and sending from an address requires access to the private keys. 
        - Proof of work, proof of stake, delegated proof of stake, and directed graph protocols are all mechanisms which allow for the arrival at a shared consensus. They both weigh the risk of engaging as a bad actor in the system compared to being rewarded for securing the system. 
    - [Token Security: Cryptography](https://github.com/sherminvo/TokenEconomyBook/wiki/Token-Security%3A-Cryptography)
        - Process of converting plaintext to cyphertext
        - Three relevant cryptographic building blocks are used in the context of public blockchain networks and other Web3 technologies: 
            - Hash Functions 
                - Convert arbitrarily complex data to fixed length array
                    - (i) easy to compute; 
                    - (ii) deterministic, meaning that the same message always results in the same hash
                    - (iii) time consuming and expensive to generate a message from its hash value with sheer brute force - need to try all possible compinations
                    - (iv) small changes to the original input value should change the hash value. - it should preferably change it completely as to avoid gaining information about the content of the message from the hash
                    - (v) infeasible to find two different messages (input) with the same hash value (output).
            - Symmetric Systems:
                - Cryptography carried out by first establishing communication on an unencrypted system. inpractical for computers The same key is used for encrypting and decrypting.
            - Asymmetric Systems
                - public/private key pair. The public key can be broadcast and it proves only the owner of the private key can sign messages with it.
                    - Anyone can verify that the public key and any message broadcast with it belongs to that user
                - Send an open lock which only you have the key to, I will write a message and lock it with that lock, and know that only you can open it.
        - Wallets
            - Bitcoin wallets either generate a private key or accept one as input.
            - In a first step, the private key is a randomly generated 256-bit integer. The public key is then mathematically derived, using elliptic-key cryptography, from the private key. In a second step, the blockchain address is derived from the public key, using a different type of cryptographic function from the one that was used to derive the public key, adding metadata like checksums and prefixes.
                - The public key is not the address!
            - An address does not store the token, if someone sends any cryto to that wallet, the entry is stored on the ledger, which maps the tokens to that specific address. An address is a key, not a wallet
    - [Who Controls The Tokens? User Centric Identities](https://github.com/sherminvo/TokenEconomyBook/wiki/Who-Controls-The-Tokens%3F-User-Centric-Identities)
        - Identity management
            - The process in which an entity can be correctly identified
            - Identifiers
                - ideally unique and persistent. Can be signaled to by a third party to point towards that entity.
            - Authentication
                - Proof someone is who they say they are. Has to be initiated by the identity holder.
            - Claims & Credentials
                - Information related to the identity
        - [Server Centric Identities](https://github.com/sherminvo/TokenEconomyBook/wiki/Who-Controls-The-Tokens%3F-User-Centric-Identities#server-centric-identities)
            - in the internet, identity verification, authentication are done in a private hosted database subject to the rules and regulations of the central authority
            - Issues:
                - Password chaos: 
                    - Too many passwords, not aligned, hard to keep track of
                - Protection against bad actors
                    - Fake actors with malicious intent
                - Data protection & custodial costs
                    - Trust that your data will be persisted, trust that it will not be used against you or your will
                - Data portability
                    - Massive friction in exporting, shaping, re-inporting and making your data interoperable
                - Lack of Control & Sovereignty
                    - Control is handed to the company, and wherever the jurisdiction for the company is
                - Re-centralization of the Internet
                    - Vendor lock in through network effects of a single service. You are more likely to stay within one system because the value of the system is tied to how many people use it. It is hard to port to a different system, and it is hard to leave. 
        - [History of digital identity management](https://github.com/sherminvo/TokenEconomyBook/wiki/Who-Controls-The-Tokens%3F-User-Centric-Identities#history-of-digital-identity-management)
            - Microsoft Passport -> Liberty Alliance -> OpenId
                - OpenId is “server-centric model” to “user-centric model” but failed to provide a user friendly solution
            - Facebook Connect
                - Won for usability, interoperability and adoption -> Google, Amazon, Twitter followed
                - user-centric to server-centric again
            - Christopher Allen and initiatives such as Rebooting-the-Web-of-Trust
                - proposed the use of public-key cryptography for pseudo-anonymous identification without linking identities to an email address
                - Access & Control
                    - Users are the ultimate authority and choose the level of access others can have
                - Transparency & Interoperability
                    - Algorithms are built and audited in the open
                - Portability
                    - Can transfer between services
                - Consent & Minimization
                    - Users must concent, and when they do, it is only for the minimal access to identity information.
            - [W3c group for Decentralized Identifiers](https://www.w3.org/TR/did-core/[[introduction]])
                - latest initiative to provide an open standard for identifying users
        - [User-Centric Identities using DIDs](https://github.com/sherminvo/TokenEconomyBook/wiki/Who-Controls-The-Tokens%3F-User-Centric-Identities#user-centric-identities-using-dids)
            - A DID is a pseudonymous identifier of an entity in the network without the need for institutional management of that identity
                - To be useable as DID and decentralized they need 3 properties
                    - They need to be permanent so they cannot be reassigned to other entities by whomever is in control. 
                    - They need to be resolvable so everyone understands how to interact with the subject identified by the DID
                    - they need to be cryptographically verifiable.
            - There still needs to be a centralized identity provider which validates characteristics of the person with the DID, address, legal age, etc.
                - Identity issuers vs Identity owners
                - Issuers are the trusted entities - [[oracle problem]] which provide data about the owner. They provide credentials which the owner can sign off on to signal the minimum data needed for the task at hand
            - The identity owners can choose which data about their identity to reveal in the process, the ledger is the process which allows for the validity of the claim and the person making the claim. 
                - DIDs can be used for the person attesting to the validity of a credential associated with a person, and they can be used by the person to identify themselves by a person looking for proof about that person
                    - This scheme of the separation of the issuing of credentials, verifying of credentials, and making a claim about those credentials is the basis for a decentralized identity mechanism in the blockchain
                        - This doesn't have to be plain text data from a database, it can be as simple as signaling that you have enough qualifying information to do a certain task (passed the bar for example) without having to generate more context around that number. Same thing with Age, are you old enough vs what year where you born?
                    - KERI (Key Event Receipt Infrastructure) is the latest on how this would work
        - [Outlook](https://github.com/sherminvo/TokenEconomyBook/wiki/Who-Controls-The-Tokens%3F-User-Centric-Identities#outlook)
            - This really revolutionized the Know Your Customer process for companies looking to onboard new clients into a network.
            - > One of the most interesting future use cases will be the digital identification of objects. Currently, most Internet-of-Things (IoT) devices have no secure digital identity and access management capabilities. A DID-powered serial number can make any object in the Web3 addressable. Once we start tagging objects with mini computers (crypto accelerators) that come with a DID-powered serial number and communicate with a distributed ledger network, any object along the supply chain can prove ownership and credentials to others in the network using cryptographic proofs. Objects that have their own unique Web3 identity and Web3 wallet can become autonomous and trustable economic entities. Such a “cyber-physical link” between objects and DID allows for effective product tracking and data sharing on the provenance of goods and services between producers and consumers.
    - [Smart Contracts](https://github.com/sherminvo/TokenEconomyBook/wiki/Smart-Contracts)
        - An executable trustless piece of logic that guarantees the same results for outputs given some inputs
        - [Self Enforcing Agreements](https://github.com/sherminvo/TokenEconomyBook/wiki/Smart-Contracts#self-enforcing-agreements)
            - A smart contract is a self-enforcing agreement, formalized as a software.
            - Parties agree on the terms of the code, and sometimes the code itself runs as the other party in the process. Since the agreement guarantees open access to whoever wants to participate in it (if the rules allow it) it provides higher security and guarantees than a traditional verbally bound agreement. 
            - Smart contracts neither enforce legal agreements, nor do they care about the legality of it. Smart contracts are pieces of logic that will run given a particular state of the blockchain which they are a part of, and the inputs given to them. The particular issues for contracts are along the axis of vulnerability for external attackers, the lack of context to anything outside the blockchain which they belong to (the oracle problem), and the human fallability that plagues software development. 
        - [Industry Use Cases](https://github.com/sherminvo/TokenEconomyBook/wiki/Smart-Contracts#industry-use-cases)
            - > Smart contracts can provide a native settlement layer for the sharing economy, currently brokered and processed by Internet platform operators.
            - > Smart contracts can furthermore be used to create and manage cryptographic tokens that can represent any asset or access rights, and even incentivize behavior. Tokens might emerge to be one of the most important applications of smart contracts, potentially revolutionizing asset management as we know it. This is why the last two parts of this book are dedicated entirely to the topic of tokens.
        - [Oracles](https://github.com/sherminvo/TokenEconomyBook/wiki/Smart-Contracts#oracles)
            - Oracles are not reliant on the security that the network provides, thus succeptible to attacks.
            - They add latency and points of failure to a smart contract. 
        - [History of Smart Contracts](https://github.com/sherminvo/TokenEconomyBook/wiki/Smart-Contracts#history-of-smart-contracts)
            - Nick Szabo in 1996
            - Formalized it by saying a piece of code that defines, verifies and executes the terms of an agreement. 
- Grokked::
    - Cryptocurrencies are more than a system for exchanging value, they are a protocol for communicating the exchange of value through distributed networks. By creating a network which generates a token of value, it align the incentives of the particular nodes in the network to execute computation which can be verified. Crypto networks are therefore super computers that can execute arbitrarily complex computations for a fee, creating a singular (yet still decentralized) point of reference which can serve as the infrastructure of a new internet - a stateful internet. 

Whereas the internet is a stateless protocol (at least http is), blockchain provides incentives for a decentralized state management system which can add a stateful layer to the internet itself. 
- [[roam/comments]]
    - [[July 9th, 2021]]
        - Parties agree on the terms of the code, and sometimes the code itself runs as the other party in the process. Since the agreement guarantees open access to whoever wants to participate in it (if the rules allow it) it provides higher security and guarantees than a traditional verbally bound agreement. 
            - Of course that [[smart contracts]] are exceptional at financial instruments that are a mathematically guarantee. hen all the simple terms of the transactions are just a matter of mathematically enforceable agreement, then they shine. Think the [[Valorize]] approach which guarantees that the owner will get the percentage of any new tokens minted. This is completely unfeasible to enforce in a legal context (there are other more complicated contracts which would be impossible like flash loans).

Given that most contracts necessitate an arbitrer for their validity, that is ambiguity is a feature of the current state of contract law in meatspace, smart contracts have a long way to go. Currently, a lot of our meatspace legal procedures need the intent of the contract to be interpreted, and certain aspects are intentionally left ambiguous. This is desirable and something that crypto maximalists tend to gloss over. [[Mattereum]], [[Kleros]], [[OpenLaw]](https://www.openlaw.io/) is one of the few projects taking this seriously, and treating it as a feature.
            - https://twitter.com/javier123454321/status/1399786793650774024
