Introduction
============
Over the years, rapid technological advancements have motivated organizations to implement efficient processes for supply chains (i.e., from design to manufacturing, logistics, and just-in-time delivery).
While these improvements help organizations increase efficiency and swiftly bring innovations to market, the rapid increase in scale, size, and complexity of supply chains has led to more frequent and sophisticated supply chain attacks.
The traditional methods of safeguarding supply chains (e.g., pre- and post-audit methodologies) are no longer adequate.

Problem Statement
=================
It is challenging to manage the compliance of products across end-to-end, global supply chains. 

Some of the fundamental security issues that face the supply chain ecosystem today are as follows:

1. A single product is composed of multiple sub-products coming from different suppliers. There is no agreed-upon standard to compose information from different producers.
2. There are no APIs defined for automated publishing, retrieval, or independent verification of the information above.
3. The absence of decentralized, globally interoperable, transparent services to publish the supply chain data.
4. The lack of sufficient standards for independently verifying the presence of supply chain data in tamper-proof data stores.

A minimal, simple, and concise set of building blocks that interact in a standardized way will assure long-term accountability and interoperability for supply chain components throughout their lifecycles across architecturally diverse systems.

Goals
=====
Based on an input document on the architecture (draft-birkholz-scitt-architecture-00), the WG will:

1. Standardize the overall security flows for securing a software supply chain, covering the essential building blocks that make up the architecture, and
2. specify these building blocks, employing the existing work already done within other IETF WGs such as COSE WG, and IETF RATS WG, as appropriate.

The WG may refine the input document on the architecture in the process.

Non-Goals
=========
The WG does not:

1. make recommendations or suggestions on best practices on how to design the supply chain,
2. establish a universal/centralized registry for supply chain data,
3. try to prevent supply chain issuers from making false claims,
4. define specific implementation guidance on storage, query, or retrieval of supply chain statements, or
5. select a specific Bill of Materials (BOM) formats and metadata headers.

Program of Work
===============

## Actors, Interactions, Terminology ("Architecture")

The WG will start out by documenting and defining terms for essential classes of actors, such as the supply chain "issuer" (one which generates supply chain artifacts), the basic interactions these have with other actors, and their duties in the ecosystem.

The WG will select (and potentially profile or augment) acceptable common **identity format/formats** that shall be used to identify and authenticate actors in the SCITT ecosystem. ~~This will enable interoperability across geographical regions and also trace the identity chain seamlessly when a product comprises of multiple sub-products from multiple issuers. ~~

## Information Sets

* Data at rest/prerequisites
    * representable via a combination of SCITT messages
    * external beliefs
* Interactions/data in motion: The WG will define the envelope and common schema for carrying supply chain claims/endorsements.  How do messages compose in order to generate meaningful beliefs?

### Versatile Countersigning Format in Support of Transparency Services

A standard format for authenticity data returned from the transparent registry, such as proof, etc. The standard will enable independent verification of supply chain claims at a (much) later point on multiple platforms across multiple geographical locations.

## Interaction Set: Registries

The WG will define an **Abstract Transparent Registry** that describes the interactions that will and can be provided by registries to generate homogeneity across multiple supply chains.

## Interaction Set: Auditing

The WG will develop standards for auditing the supply chain claims that are introduced in the transparent registry. This will, in turn, generate audit claims (results of the audit) which can be introduced in the same registry. Audit information can be queried by supply chain consumers (end customers) before making critical business decisions.

## Interaction Set: Notarization

The WG will develop standards that define the notarization process and outline the core functions/actions that a notary will perform in the supply chain ecosystem.

## Mapping the Interaction Sets to HTTP/REST

Standardize request-response interactions ("external API") and potentially other interaction models provided to various actors to interact with the supply chain ecosystem. This includes standardizing inter-component messages between supply chain building blocks to support easy reference implementations of SCITT building blocks by various organizations and easy industry-wide adaptation.

Milestones
==========
* Architecture and Terminology
* Information and Interaction Models
* Countersigning Format for Claim Registration
* HTTP-based REST API for Request-Response Interactions 
