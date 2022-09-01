Introduction
============
A Device's supply chain, including its components, is complex often being comprised of both common libraries and custom components. Knowing the identity of a Device or its component is critical to determining its compliance. However, the scale, size, and complexity of supply chains, from design, manufacturing, logistics, and just-in-time delivery has led to more frequent and sophisticated supply chain attacks. The traditional methods of safeguarding supply chains (e.g., pre- and post-audit methodologies) are no longer adequate, therefore, with the increase in suppliers and increase in the complexity of the various supply chains the means to determine a Device or component's identity requires standardization.


The output of the SCITT WG is a set of standards that define the essential building blocks enabling the security of supply chain systems and assisting implementers in securing deployments.
For example, a public computer interface system could report its software composition, which can be compared against known software compositions for such a device, as recorded in an append-only transparent registry.
Therefore, providing an individual using the system with confidence that it will behave as and when expected, consistently and without deviation.


Problem Statement
=================
It is challenging to manage the compliance of products across end-to-end, global supply chains. 

Some of the fundamental security issues that face the supply chain ecosystem today are as follows:

1. A single product is composed of multiple sub-products coming from different suppliers. There are several standards to compose supply chain information with different producers choosing different methods.
2. There are no APIs defined for automated publishing, retrieval, or independent verification of the information above.
4. The absence of decentralized, globally interoperable, transparent services to publish the supply chain data.
5. The lack of sufficient standards for independently verifying the presence of supply chain data in tamper-proof data stores.
6. Software consumers have no trustworthy way to verify that a software signature on a software package is legitimate.

[//]: # (MW: #6 is not true, SWID tags can be signed today.)

A minimal, simple, and concise set of building blocks that interact in a standardized way will provide long-term accountability and interoperability for supply chain components throughout their lifecycles across architecturally diverse systems.

Goals
=====
Based on an input document on the architecture (draft-birkholz-scitt-architecture-00), the WG will:


1. Standardize the technical flows for providing information about a software supply chain, which also includes firmware, and covering the essential building blocks that make up the architecture.
2. In addition to this, the WG shall employ the existing work already done within
    - other IETF WGs such as COSE WG, and IETF RATS WG, as appropriate,
    - coordination with other bodies, such as the, OpenSSF, W3C, ISO, and the Trusted Computing Group.

The WG may refine the input document on the architecture in the process.

Non-Goals
=========
The WG does not:

1. make recommendations or suggestions on best practices on how to design the supply chain,
2. establish a universal/centralized registry for supply chain data,
3. define methods to prevent supply chain issuers from making false claims,
3. try to prevent supply chain issuers from making false claims,
4. define data formats for payload content, such as Bills of Materials data formats

[//]: # (Bill of Materials \(BOM\): We don't define this term prior to use. I like including this term, shouldn't we define it as a component of the supply chain)

Program of Work
===============

The main deliverables defined by this program of work provide a guideline for milestones that are in scope of the WG charter. Documents produced by the working group will address one or more of the following main deliverables:

## Architectural Model: Actors, Interactions, Terminology

The WG shall start by documenting and defining terms in an architectural model for:

1. essential actors, such as the claim's "issuer", "notary", and "consumer" (one which generates supply chain artifacts and statements about them) and
2. the basic interactions these have with other actors, and their role in the ecosystem.

The architectural model shall provide an aggregated overview of corresponding actor-specific information models and interaction models. It will provide examples of composition patterns that illustrate how to address a concise set of use cases.

[//]: # (MW: What does "aggregated" add in the above paragraph?)

The architectural model shall include an abstract threat model that minimally encompasses the initial use cases and will be based on a set of to be defined security objectives.

## Consistent Actor Identification

The WG shall select (and potentially profile) acceptable common identity format/formats that will be used to identify and authenticate various actors in the SCITT ecosystem. The WG shall create guidance on how to create and manage new identity documents, their trust anchors, and corresponding security considerations in the context of supply chains.

## Information Models and Interaction Models for:

1. Registry: The WG shall define an Abstract Transparent Registry and also define the interactions and conceptual messages that will be supported by registries with an aim to generate homogeneity across multiple supply chains.

2. Notarization: The WG shall develop a specification that describes the notarization information model and the interaction model a notary will use to interact with supply chain entities.

3. Auditing: The WG shall develop standards to permit auditing of supply chain claims that are introduced in the transparent registry. This will, in turn, generate audit claims based on an information model (results of an audit), which can be introduced in the same registry. A corresponding interaction model will describe how audit information can be queried by supply chain consumers (e.g., end customers) before making critical business decisions.

## Versatile Countersigning Format in Support of Transparency Services

The WG shall specify a standard format for authenticity data returned from the transparent registry such as proofs, etc. The standard shall enable independent verification of supply chain claims at a (much) later point on multiple platforms across multiple geographical locations.

[//]: # (MW: authenticity data is not defined above. What is it?)

## Generic Protocol Bindings for Information Model and Interaction Models

The WG shall standardize request-response interactions ("external API") and potentially other generic interaction schemes provided to various actors to interact with the supply chain ecosystem. This includes standardizing inter-component messages (based on the interaction models) and payload serialization between supply chain actors to support common reference implementations of SCITT building blocks by various organizations to expedite industry-wide adaptation.

Milestones
==========
* Architecture and Terminology
* Use Cases, Security Objectives, and concise Threat Model
* Information and Interaction Models
* Countersigning Format for Claim Registration
* HTTP-based REST API for Request-Response Interactions
