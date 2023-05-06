This document is divided into different sections for easy acquaintance and categorization. The different sections can be seen as a waterfall step, where the flow of a step comes from a step above. Starting with the [Preamble][preamble] that defines the intentions to start this project and establishes the principles to adhere to while in development. The next section is [Design Concept][dc] that describes the high-level design of the mechanism. After that it is the [Definition of terms][dot] section to provide the definitions of the contextual terms. Then we have the [Software Components][sc] section detailing the software components that need to be implemented. The next section is [Entities][ent] that would define the entities for data modeling. After that we have the section [Design details][dt] that will contain the design in detail and establish what will be the functional specifications. These sections would be fluid and in general explanatory. The next set of sections would eventually become concrete (depending on their status) and will form the foundation of the actual implementation.

The [FSD][fsd] section will meticulously document the precise functional specifications. Based on this, we would have the [TSD][tsd] section that will document the technical specifications. Lastly, we would have the documentation for system [APIs][api]. These three sections can have multiple layers of sub-sections and will be the source of reference for both tests and code. Each sub-section can have its own running status.

For system designers, section [1][preamble], [2][dc] and [6][dt] are of main interest. For developers, it is the rest of the sections.

[preamble]: Preamble.md
[dc]: Design-Concept.md
[dot]: Definition-of-Terms.md
[sc]: Software-Components.md
[ent]: Entities.md
[dt]: Design-Details.md
[fsd]: fsd/Functional-Specification-Document.md
[tsd]: tsd/Technical-Specification-Document.md
[api]: apis/API.md
