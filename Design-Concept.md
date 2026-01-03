[![status](https://img.shields.io/badge/status-Open-blue?style=for-the-badge&logo=appveyor)](https://img.shields.io/badge/status-Open-blue)

## Design Concept: Satyarat (DSoT)

This document outlines the preliminary design concepts for Satyarat (DSoT). It builds upon the principles established in the Preamble and will be followed by more detailed design specifications.

As previously stated, Satyarat will utilize a peer-to-peer (P2P) architecture where data storage and processing are distributed across all participating nodes. Key goals include ensuring the security, immutability, distribution, availability, and persistence of data.

A core design principle is that the entire system, and its adoption, should contribute to achieving these goals, rather than relying on isolated technological solutions. This approach aligns with the principles outlined in the [Preamble][preamble], particularly number eight.

**Human-Memory-Based Data Security:** A distinguishing feature is the incorporation of human memory as a security mechanism. Users can optionally anchor their data with personal memories, creating a uniquely secure key that is resistant to computational compromise.

**Data States:** Data within the system, primarily represented as messages forming the Source of Truth (SoT), will exist in various states of persistence: local, afloat, concrete, and fulfilled. The "fulfilled" state signifies a secure and verifiable basis for contractual agreements between entities.  Definitions of key terms can be found in the [Definitions of Terms][dot] section.

The design adheres to the principles defined in the [Preamble][preamble]. This document will examine how the design concept addresses each principle.

### <ins>Principle 1</ins>: System closed to any dominion and alterations

The core P2P architecture distributes computing and storage across all nodes, preventing centralized control. To ensure further security, a “Forge” component is introduced. The Forge is responsible for generating and validating software binaries for nodes joining the network, forming an "ether" when interconnected. Nodes must register with and be validated by the Forge before joining the ether, receiving a unique signature.

The basic ideas is as follows: An entity can initiate and publish a Forge. Users requesting binaries from this Forge run a node on the ether. Upon registration, the Forge adds the node to its list of valid nodes. A new node is notified to existing nodes, which in turn can ping the new node and add it to their own lists. Node adjacency is inferred through response time calculations. New nodes can request a list of peers from the Forge and update their local lists by pinging the listed nodes.

Each node carries a fingerprint of the Forge, enabling the rejection of binaries generated from compromised versions. This mechanism prevents unauthorized data alterations by ensuring all nodes belong to their originating Forge.

### <ins>Principle 2</ins>: Data should always be immutable

The design incorporates immutable and tamper-proof storage systems, leveraging open-source solutions where appropriate. However, the system also mitigates risks associated with potential storage breaches through data replication and consensus mechanisms.

### <ins>Principle 3</ins>: Output remains unaffected by data corruption

Data is categorized as: one - user-generated information and two - associated metadata. Modifying metadata for data originating from the user's own node is acceptable, if not used in message processing. Altering any other data or its metadata constitutes data corruption. This can occur through compromised nodes or by breaching data store immutability.

Compromised nodes are addressed by the node registration and validation process described above. Data store immutability is further protected through multi-layered encryption, intelligent key management, and consensus-based data replication. A consensus mechanism is employed to validate data, mark compromised nodes as “dirty,” and prevent further replication. Contracts over a message require 100% consensus across a predetermined number of nodes (TBD).

### <ins>Principle 4</ins>: Data persistence for as long as required

Data persistence is inherently ensured through network adoption and data replication. There will be an upper limit on the number of nodes where data would be replicated.

### <ins>Principle 5 & 6</ins>: Data to be used only for intended purposes

These principles are reinforced by restricting data exchange to provided APIs, employing robust encryption, and maintaining an immutable data store. The integrity of nodes is protected through the registration and validation process.

### <ins>Principle 7</ins>: APIs for end user

The system will provide a simple and intuitive set of APIs, allowing users to exchange messages and secure their data with configurable options. These options include layered encryption, key management, and generation of secure keys using human-memory anchoring.

### <ins>Principle 8</ins>: Simplicity and inextensibility

The design prioritizes logical and organic solutions, avoiding complex algorithms that can introduce unintended side effects. To maintain focus and avoid complexity, the system will be designed to be closed to extensibility.

[preamble]: Preamble.md
[dot]: Definition-of-Terms.md
