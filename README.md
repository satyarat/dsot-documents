# Documentation for Decentralized Source of Truth (DSoT) 

This document serves as the definitive source for the design and specifications of **Decentralized Source of Truth (DSoT)**, bearing the moniker - **Satyarat**. It is meant to be a mechanism for persisting a source of truth (**SoT**) across distributed nodes operating under a common software component set.  An introductory overview of this concept was presented [here](https://satyarat.github.io/home).

**Purpose:** This document aims to define, refine, and formally document the design and specifications for the DSoT mechanism. It will be the central reference point for development and implementation.

**Progression:** All sections of this document are open for review and modification. However, all proposed changes must align with the overarching intentions outlined in the [Preamble][preamble]. The initial content, particularly the conceptual and design sections, represents preliminary approaches and may evolve to influence the detailed specifications.

## Design and Development Process

The development process for DSoT will follow these phases:

1.  **Concept:** Initial ideation and conceptual design evolutions 
2.  **Design:** Concrete high-level architecture and system design
3.  **Functional Specifications:** Defining the system's behavior and capabilities
4.  **Technical Specifications:** Defining technical requirements for implementation
5.  **Test-Driven Development (TDD):** Implementation guided by unit and integration tests
6.  **Code:** Implementation of the DSoT mechanism
7.  **Functional Testing:** Verification of system functionality against specifications
8.  **Unit Implementation:** Development and testing of individual components
9.  **Integration Testing:** Verification of component interactions
10. **Final Implementation:** Production-ready deployment

## Document Structure

This document is organized into the following sections. The status of each section will be indicated prominently.

- [How to Read and Reference This Document][reref]
- [Preamble][preamble]: Establishes the guiding principles and objectives of DSoT
- [Design Concept][dc]: Explores the high-level design principles and overall architecture
- [Definition of Terms][dot]: Defines key terminology used throughout the documentation
- [Software Components][sc]: Describes the software components comprising the DSoT mechanism
- [Entities][ent]: Defines the object entities that will represent the data in the system 
- [Design Details][dt]: Provides detailed design considerations, choices and finalized items
- [Functional Specification Document][fsd]: Details the expected behavior and functionality of DSoT.  (*Located in the `fsd/` directory*)
- [Technical Specification Document][tsd]: Describes the technical implementation details. (*Located in the `tsd/` directory*)
- [APIs][api]: Defines the interfaces for interacting with DSoT. (*Located in the `apis/` directory*)

## Contribution & Licensing

If you intend to contribute to this project or utilize the information contained within, please review the [License][licence] and [Contributing][contributing] sections.

[reref]: How-to-read-and-reference-this-document.md
[preamble]: Preamble.md
[dc]: Design-Concept.md
[dot]: Definition-of-Terms.md
[sc]: Software-Components.md
[ent]: Entities.md
[dt]: Design-Details.md
[fsd]: fsd/Functional-Specification-Document.md
[tsd]: tsd/Technical-Specification-Document.md
[api]: apis/API.md
[licence]: Licence.md "Satyarat Documentation License"
[contributing]: Contributing.md "Satyarat Contributing Guide"

## Community Engagement

Join our [Discord](https://discord.gg/pAEzwZY9Su) 💬 for discussions, questions, and collaboration.
