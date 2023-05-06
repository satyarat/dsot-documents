[![status](https://img.shields.io/badge/status-Open-blue?style=for-the-badge&logo=appveyor)](https://img.shields.io/badge/status-Open-blue)

This document describes the preliminary design concepts for Satyarat (DSoT). This will further ensue documenting the design in detail.

As can be inferred from the introduction, this will be a P2P based mechanism where data and local processing will be borne by every node. The main goals are security, immutability, distribution, availability and persistence of data.

An essential idea is that the entire mechanism itself should be the way to achieve all the goals, including resilience to data corruption. Which means no single technological technique is going to fulfill all or any of the features in isolation, but all of them should be accomplished by the entire mechanism and the spread of adoption. This is in adherence to the principles listed in the preamble, especially the 7th.

Another distinctive idea is that data security can be based on short and precise human memories. Users can choose to secure their data based on their real-life memories around the data, something which they can remember back. This mitigates the need for any overcomplicated computational way to secure the data.

Data, of essence, will be mainly composed of messages, which will be the actual SoT. Based on their distribution, these messages can be in different states of persistence. These are – local, afloat, concrete and fulfilled. The ‘fulfilled’ state is for transactions between two different entities, which is when we can say it is safe and secure to form contracts over them. The definitions of contextual terms can be found in the [Definitions of terms][dot] section.

The design has to take into the consideration the principles defined in the [Preamble][preamble], and so we start with a high level design concept that can ensure that these principles are adhered to.

For principle 1, we already have described the basic design that will be a P2P, distributed computing and storage mechanism. Each node will have the same logical computing and will operate on its own without any means for external influence, but should also be able to connect to a central service to find peers. This service can be provided by the Forge. Will it affect independent functioning? I would say no, because the Forge’s functioning only involves registering the nodes that have come ‘online’ as one of the binaries published by it. In other words, all nodes that would be running binaries published by the Forge would be under one umbrella.

For principle 2, we would be using a storage system that would be immutable and tamper-proof. We already have a few very good open-source storage systems that we can use and/or extend to meet this requirement. However, we also do not want to rely completely on the capabilities of the storage system. What happens if the storage system is breached? That is why principle 3 is important.

To ensure principle 3, data replication will trace the path (Tracing of data paths will be defined after we define the way to categorize data) and validate if data has altered anywhere in between, based on origin and consensus. If it finds a node where data has changed, it stops any further replication from the node and that node would be evicted from the list of valid nodes. In this regard, we can divide data into two categories - identifiers and values. If the identifiers are changed, then they become totally new records, dangled and useless. If the values, which will generally be encrypted, are changed then decryption won’t work for those values and for these cases we would trace the path of the data from its origin to ensure we are not replicating corrupt data. This operation will be performed by the node that is accepting the replicating data. It has to skim all the nodes that have held the data and determine origin, consensus and validity. So in this mechanism, replication will relatively be a much slower and of course asynchronous operation.

Principle 4 is ensured by the adoption of the medium. If there are sufficient nodes available, replication will ensure that data persistence gradually becomes almost absolute. However, we need to put an upper limit on the number of times a data can be replicated. To my mind, 9 should be a good number.

For principle 5 & 6, we would have encryptions. For sensitive data, it would be double-layered encryption. I would like to provide the options to manage keys or let the system manage the keys. I also propose the option to generate the encryption keys based on human (user) memories.

Principle 7 is ensured by limiting the features of the system to just be about SoT. Also, by providing required APIs for this purpose.

Principle 8 is about the very design of the mechanism. It is about delivering on the goals without making it complex. It is about using/creating ingenious techniques rather than falling onto some absolute complex mechanism (which generally leads to unmanageable and thorny side-effects) to provision the requirements.

[preamble]: Preamble.md
[dot]: Definition-of-Terms.md
