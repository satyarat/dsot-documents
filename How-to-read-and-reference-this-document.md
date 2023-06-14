This document is divided into different sections for easy acquaintance and categorization. These sections can be seen as waterfall steps, where the flow of a step comes from the step above. It starts with the [Preamble][preamble], which establishes the intentions of the project and defines the principles to adhere to while in development. The next section [Design Concept][dc]  describes the high-level design of the mechanism. It prescibes to the Preamble and provides foundational ideas about the implementation. The [Definition of terms][dot] section contains the definitions of the contextual terms used within these documents. Then the [Software Components][sc] section presents the software components that will be needed to piece together the complete implementation. The next section is [Entities][ent] that would define the entities for data modeling. After that, the [Design details][dt] section will elaborate on the designs in detail and establish what will become the functional specifications. These sections would be fluid and in general explanatory. The next set of sections would eventually become concrete (depending on their status) and will form the foundation of the actual implementation.

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
