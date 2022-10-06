Introduction
============
The Supply Chain Integrity, Transparency, and Trust (SCITT) work forms a set of interoperable building blocks that will allow implementers to build integrity and accountability into supply chain systems to help assure trustworthy operation.
For example, a public computer interface system could report its software composition that can then be compared against known software compositions or certifications for such a device thereby giving confidence that the system is running the software expected and has not been modified, either by attack or accident, in the supply chain.
While potentially broadly applicable, SCITT will initially focus on the software supply chain.

Problem Statement
=================
Some of the fundamental security issues that face the supply chain ecosystem today are as follows:

1. A single product is composed of multiple sub-products coming from different suppliers.
There are several standards to compose supply chain information with different producers choosing different methods.
2. There are no uniform APIs or services to publish supply chain information to third parties, nor are there ways to verify the integrity or date of publication of that information.
3. There is a lack of decentralized, globally interoperable, transparent services to publish supply chain data.
4. The lack of sufficient standards for independently verifying the presence of supply chain data in tamper-proof data stores.
5. Fractured verification methodologies across software distribution ecosystems create inconsistent security guarantees for end users.
6. Software consumers have no trustworthy way to verify that a software signature on a software package is legitimate.

A minimal, simple, and concise set of building blocks that interact in a standardized way will assure long-term accountability and interoperability for supply chain components throughout their lifecycles across architecturally diverse systems.

Goals
=====
Based on an input document on the architecture (draft-birkholz-scitt-architecture-00), the WG will standardize the technical flows for providing information about a software supply chain, which also includes firmware, and covering the essential building blocks that make up the architecture.
The WG may refine the input document on the architecture in the
process.

The WG will:
- reuse existing work from IETF WGs such as COSE and RATS, as appropriate,
- coordinate with other standards bodies, such as the OpenSSF, W3C, ISO, and the Trusted Computing Group.

Non-Goals
=========
The WG does not:

1. make recommendations or suggestions on best practices on how to design the supply chain,
2. establish a universal/centralized registry for supply chain data,
3. define methods to prevent authenticated supply chain issuers from making false claims,
4. define data formats for payload content, such as Bills of Materials data formats.

Program of Work
===============
Documents produced by the working group will address one or more of the
following programs of work:

## Architectural Model: Actors, Interactions, Terminology

The WG shall start by documenting and defining terms in an architectural model for:

1. essential actors, such as the claim's "issuer" (one which generates supply chain artifacts and statements about them), "notary", and "consumer" and
2. the basic interactions these have with other actors, and their duties in the ecosystem.

The architectural model shall provide an aggregated overview of corresponding actor-specific information models and interaction models.
It will provide examples of composition patterns that illustrate how to address a concise set of use cases.

The architectural model shall include an abstract threat model that minimally encompasses the initial use cases and will be based on a set of to be defined security objectives.

## Consistent Actor Identification

The WG shall select (and potentially profile) acceptable common identity
format/formats that will be used to identify and authenticate various actors in the SCITT ecosystem.
The WG shall create guidance on how to create and manage new identity documents, their trust anchors, and corresponding security considerations in the context of supply chains.

## Information Models and Interaction Models for:

1. Registry: The WG shall define an Abstract Transparent Registry and also define the interactions and conceptual messages that will be supported by registries with an aim to generate homogeneity across multiple supply chains.
2. Notarization: The WG shall develop a specification that describes the
notarization information model and the interaction model a notary will use to interact with supply chain entities.
3. Auditing: The WG shall develop standards to permit auditing of supply chain claims that are introduced in the transparent registry.
This will, in turn, generate audit claims based on an information model (results of an audit), which can be introduced in the same registry.
A corresponding interaction model will describe how audit information can be queried by supply chain consumers (e.g., end customers) before making critical business decisions.

## Versatile Countersigning Format in Support of Transparency Services

The WG shall specify a standard format for authenticity data returned from the transparent registry such as proofs, etc.
The standard shall enable independent verification of supply chain claims at a (much) later point on multiple platforms across multiple geographical locations.

## Generic Protocol Bindings for Information Model and Interaction Models

The WG shall standardize request-response interactions ("external API") and potentially other generic interaction schemes provided to various external entities to interact with the supply chain ecosystem.
This includes standardizing inter-component messages (based on the interaction models) and payload serialization between supply chain actors to support common reference implementations of SCITT building blocks by various organizations to expedite industry-wide adaptation.

Introduction
============
Over the years, rapid technological advancements have motivated organizations to implement efficient processes for supply chains (i.e., from design to manufacturing, logistics, and just-in-time delivery).
While these improvements help organizations increase efficiency and swiftly bring innovations to market, the rapid increase in scale, size, and complexity of supply chains has led to more frequent and more sophisticated supply chain attacks.
The traditional methods of safeguarding supply chains (e.g., pre- and post-audit methodologies) are no longer adequate.

The Supply Chain Integrity, Transparency, and Trust (SCITT) work forms a set of interoperable building blocks that will allow implementers to build integrity and accountability into supply chain systems to help assure trustworthy operation.
For example, a public computer interface system could report its software composition that can then be compared against known software compositions or certifications for such a device thereby giving confidence that the system is running the software expected and has not been modified, either by attack or accident, in the supply chain.

Problem Statement
=================
It is challenging to manage the conformance of products across end-to-end, global supply chains.

Some of the fundamental security issues that face the supply chain ecosystem today are as follows:

1. A single product is composed of multiple sub-products coming from different suppliers. There are several standards to compose supply chain information with different producers choosing different methods.
2. There are no uniform APIs or services to publish supply chain information to third parties, nor are there ways to verify the integrity or date of publication of that information.
3. There is a lack of decentralized, globally interoperable, transparent services to publish supply chain data.
4. Available standards are not sufficient for independently verifying the presence of supply chain data in tamper-proof data stores.
5. Fractured verification methodologies across software distribution ecosystems create inconsistent security guarantees for end users.
6. Software consumers have no trustworthy way to verify that a software signature on a software package is legitimate.

A minimal, simple, and concise set of building blocks that interact in a standardized way will assure long-term accountability and interoperability for supply chain components throughout their lifecycles across architecturally diverse systems.

Goals
=====
Based on an input document on the architecture (draft-birkholz-scitt-architecture-00), the WG will:

1. Standardize the technical flows for providing information about a software supply chain, which also includes firmware, and covering the essential building blocks that make up the architecture.
2. In addition to this, the WG shall employ the existing work already done within
    - other IETF WGs such as COSE and RATS, as appropriate,
    - coordination with other standards bodies, such as OpenSSF, W3C, ISO, and the Trusted Computing Group.

The WG may refine the input document on the architecture in the process.

Non-Goals
=========
The WG does not:

1. make recommendations or suggestions on best practices on how to design the supply chain,
2. establish a universal/centralized registry for supply chain data,
3. define methods to prevent authenticated supply chain issuers from making false claims,
4. define data formats for payload content, such as Bills of Materials data formats.

Program of Work
===============

The main deliverables defined by this program of work provide a guideline for milestones that are in scope of the WG charter.
Documents produced by the working group will address one or more of the following main deliverables:

## Architectural Model: Actors, Interactions, Terminology

The WG shall start by documenting and defining terms in an architectural model for:

1. essential actors, such as the claim's "issuer" (one which generates supply chain artifacts and statements about them), "notary", and "consumer" and
2. the basic interactions these have with other actors, and their duties in the ecosystem.

The architectural model shall provide an aggregated overview of corresponding actor-specific information models and interaction models.
It will provide examples of composition patterns that illustrate how to address a concise set of use cases.

The architectural model shall include an abstract threat model that minimally encompasses the initial use cases and will be based on a set of to be defined security objectives.

## Consistent Actor Identification

The WG shall select (and potentially profile) acceptable common identity format/formats that will be used to identify and authenticate various actors in the SCITT ecosystem.
The WG shall create guidance on how to create and manage new identity documents, their trust anchors, and corresponding security considerations in the context of supply chains.

## Information Models and Interaction Models for:

1. Registry: The WG shall define an Abstract Transparent Registry and also define the interactions and conceptual messages that will be supported by registries with an aim to generate homogeneity across multiple supply chains.

2. Notarization: The WG shall develop a specification that describes the notarization information model and the interaction model a notary will use to interact with supply chain entities.

3. Auditing: The WG shall develop standards to permit auditing of supply chain claims that are introduced in the transparent registry.
This will, in turn, generate audit claims based on an information model (results of an audit), which can be introduced in the same registry.
A corresponding interaction model will describe how audit information can be queried by supply chain consumers (e.g., end customers) before making critical business decisions.

## Versatile Countersigning Format in Support of Transparency Services

The WG shall specify a standard format for authenticity data returned from the transparent registry such as proofs, etc.
The standard shall enable independent verification of supply chain claims at a (much) later point on multiple platforms across multiple geographical locations.

## Generic Protocol Bindings for Information Model and Interaction Models

The WG shall standardize request-response interactions ("external API") and potentially other generic interaction schemes provided to various external entities to interact with the supply chain ecosystem.
This includes standardizing inter-component messages (based on the interaction models) and payload serialization between supply chain actors to support common reference implementations of SCITT building blocks by various organizations to expedite industry-wide adaptation.

Milestones
==========
* Architecture and Terminology
* Use Cases, Security Objectives, and concise Threat Model
* Information and Interaction Models
* Countersigning Format for Claim Registration
* HTTP-based REST API for Request-Response Interactions including examples as implementation guidance
