Introduction
============
Over the years rapid technological advancements have motivated organizations to implement efficient processes for supply chain (i.e from design to manufacturing, logisitics and just-in time delivery). While these improvements help organizations increase efficiency and swiftly bring innovations to market, the rapid increase in scale, size and complexity of supply chain have led to more and more sophisticated supply chain attacks. The traditional methods of safeguarding the supply chain (e.g. pre and post audit
methodologies) is no longer adequate.

Problem Statement
=================
Here are the fundamental security issues that face the supply chain ecosystem today:
1. A single product is composed of multiple sub-products coming from different suppliers. There is no agreed upon standard to compose information from different producers
2. No APIs defined for automated publishing, retrieval or independent verification of the information above.
3. Absence of decentralized globally inter-operable transparency services to publish the supply chain data in a transparent manner
4. Insufficient standards for independently verifying the presence of supply chain data in tamper proof data stores 


A minimally, simple and concise set of building blocks that interact in a standardized way could guarantee a long term accountability and inter-operability for supply chain components throught their lifecylces across architecturally diverse systems.

Goals
=====
The WG has defined a proposed architecture (link to architecture) for securing a software supply chain. The WG will standardize the overall workflow and essential building blocks that make up the architecture.

The WG will use the existing work already done within other IETF WGs such as 
COSE WG, IETF RATS WG, as appropriate.

Non-Goals
=========
The WG does not:
1. Make recommendations or suggestions on best practices on how to design the supply chain
2. Proposing a universal/centralized registry for supply chain data.
3. Prevent supply chain issuers from making false claims. 
4. Any specific implementation guidance on Storage, Query or retrieval of supply chain statements
5. Various Bill of Material Formats and metadata header

Program of Work
===============
The working group will develop standards supporting interoperable supply chain building blocks. The main deliverables are as follows:

1. The identity of the supply chain issuer (one which generates the artefact) is an essential element in the ecosystem. The WG will define acceptable common identity format/formats that shall be used in the SCITT eco-system. This will enable inter-operability across geographical regions and also tracing the identity chain in a seamless manner when a product is comprised of mutliple sub-products coming from multiple issuers.

2. The WG will define envelope and common schema for carrying supply chain claims/endorsements

3. The WG will standardize the Transparent Registry requirements to generate homogenity across multiple supply chains

4. The WG will develop a standard that define the format for authenticity data returned from the transparent registry, like proof etc.
 The standard will enable independent verification about supply chain claims at later point on multiple platforms across multiple geographical locations.

5. The WG will develop standards for auditing the supply chain claims that are introduced in the transparent registry. This will in turn generate audit claims (results of the audit) which can be introduced in the same registry. Audit information can be queried by 
supply chain consumers (end customers) before making business critical descisions.

6. The WG will develop standards that define the process of notarization and outline the core functions/actions that a notary will perform in supply chain ecosystem

7. Standardize external API provided to various actors to interact with the Supply Chain Ecosystem. Also standardize inter-component messages between supply chain building blocks. This will enable easy reference implementation of SCITT building blocks by various organizations and enable easy industry wide adaptation