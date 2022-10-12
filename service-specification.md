---
titlepage: true
toc: true
toc-own-page: true
title: "Service specification for the MCP Service Registry Global Ledger"
author: [MCP Consortium]
date: "2022-08-10"
keywords: [Maritime technical service, MCP, Service registry, global ledger]
logo: "materials/mcplogo.png"
titlepage-text-color: "476E7D"
footer-center: "G1128 Service Specification"
bibliography: references.yml
csl: acm.csl
...

# Introduction

The International Maritime Organization (IMO) in its 'Strategy for the
development and  implementation of e‐Navigation' (MSC85/26, Annex 20) [@IMO-ENAV1]
resolution, provides the following definition of e‐Navigation:

***E-Navigation, is the harmonised collection, integration, exchange,
presentation and analysis of maritime information on-board and ashore by
electronic means to enhance berth-to-berth navigation and related services, for
safety and security at sea and protection of the marine environment.***

In IMO resolution MSC.467(101) “Guidance on the Definition and Harmonization of
the Format and Structure of Maritime Services in the Context of e-Navigation”
[@IMO-ENAV2], IMO defines Maritime Services and Technical Services in the context of
e-Navigation. In this resolution, the Maritime Services are on the highest 
level, describing a service in an entirely non-technical manner. One or more
Technical Services are associated with a Maritime Service, and these Technical
Services are the ones defining the actual information exchange needed to take
place in order to carry our a Maritime Service.

The MCP Service Registry [@msr] service, or MSR for short, assumes the role of a
general registry for Technical Services. It provides a reference point to the
most relevant information and the respective end-points of the registered
services and thus to improve the accessibility of available services in the
maritime domain.

The Technical Services in the resolution are defined on three levels following
the same structure as in IALA G-1128 [@g1128] guideline. The MSR supervises all
service providers to describe their service in the format of G-1128. MSR contains service information from those the three levels to facilitate the service discoverability,
but services without the G-1128 documentation also can be registered.

## Purpose

The MSR Gl

## Intended readership

<!--
This service specification template is intended to be read by service architects who shall produce service A description.
This section shall describe the intended readers. e.g.: -->

This service specification is intended to be read by service architects, system engineers and developers in charge of designing and developing an instance of the MCP Service Registry Global Ledger service.

Furthermore, this service specification is intended to be read by enterprise architects, service architects, information architects, system engineers and developers in pursuing architecting, design and development activities of other related services.

## Inputs from other sources
<!--
This section lists previous work on the subject covered by this document.
Special emphasis shall be put on what has been reused from other (already finished) projects. -->
This section provides an overview of activities, which are dealing with similar topics and lists already finished ones that provided inputs to this activity.

# Service identification

The purpose of this section is to provide a unique identification of the service and describe where the service is in terms of the engineering lifecycle.

<!-- Table below shall be completed. -->

Attribute    | Content
--           | ----
Name         | Maritime Service Registry Global Ledger
ID           | urn:mrn:mcp:service:mcc:mcc:specification:msr-ledger
Version      | 0.0.1
Description  | A global ledger acting as a reference point to provide metadata about where to find the information on services instances that are registered in different Maritime Service Registries.
Keywords     | service, registry, discoverability, specification, G-1128, technical, global, ledger, distributed
Architect(s) | MCC MSR WG
Status       | Provisional

# Operational context

This section describes the context of the service from an operational perspective.
<!--
The operational context description shall be based on the description of the operational model, consisting of a structure of operational nodes and operational activities.  If such an operational model exists, this section shall provide references to it.  If no such operational model exists, then its main aspects shall be described in this section.

Optionally, a simple high level use case, described in layman’s terms, could be provided as an introduction to this section.

The operational context shall be a description of how the service supports interaction among operational nodes. This can be achieved in two different levels of granularity:
1. A description of how the service supports the interaction between operational nodes. This basically consists of an overview about which operational nodes shall provide the service and which operational nodes will consume the service.
2. A more detailed description that indicates what operational activities the service supports in a process model.

Moreover, the operational context shall describe any requirement the service will fulfil or adhere to.  This refers to functional as well as non-functional requirements at high level (business/regulatory requirements, system requirements, user requirements).  Especially, information exchange requirements are of much interest since the major objective of services is to support interaction between operational nodes.
The source material for the operational context description should ideally be provided by operational users and is normally expressed in dedicated requirements documentation.  Ensure that the applicable documents are defined in the References section.  If no requirements documents are available, then the basic requirements for the service shall be defined in the section D 3.1.

Architectural elements applicable for this description are:
* Service;
* Nodes;
* Operational activities;
* Information exchange requirements.
-->

## Functional and non-functional requirements

<!--
This section lists all (functional and non-functional) requirements applicable to the service being described. A tabular list of requirements shall be added here.  If external requirements documents are available, then the tables shall refer to these requirements, otherwise the requirements shall be documented here.

The service must be linked to at least one requirement.  At least one of the following tables shall be presented in this section.  The first table lists references to requirements available from external documents.  Make sure you document the sources from where the requirements are coming from.  The second table lists new requirements defined for the first time in this service specification document.
-->

### Functional requirements

Requirement Id | Requirement Name | Requirement Text | References
--- | --- | --- | ---
MSR-FR001 | Service Reference Registration | Allow the registration of a new reference to a service instance and the MSR that it is registered in. | MCC MSR WG
MSR-FR002 | Service Reference Update | Allow updates of existing service instance references. | MCC MSR WG
MSR-FR003 | Global Service Discoverability | Allow services to be globally discoverable across several different MSRs. | MCC MSR WG

#### Requirement definitions - XYZ-FR003

Requirement Id | Requirement Name
--- | ---
Requirement Name |
Requirement Text |
Rationale |
Author |

### Non-functional requirements

Requirement Id | Requirement Name | Requirement Text | References
--- | --- | --- | ---
MSR-NFR001 | Authenticity | The service consumer must be able to verify the authenticity of the received data. | MCC MSR WG
MSR-NFR002 | Integrity | The service consumer must be able to verify that the received data has not been tampered with. | MCC MSR WG
MSR-NFR003 | something | something | something

# Service overview
<!--
This section aims at providing an overview of the main elements of the service.  The elements in this view are all usually created by an UML modelling tool.

Architectural elements applicable for this description are:
* Service - the element representing the service in its entirety;
* Service Interfaces - the mechanisms by which a service communicates. Defined by allocating service operations to either the provider or the consumer of the service;
* Service Operations - describe the logical operations used to access the service.
* Service Operations Parameter Definitions - identify data structures being exchanged via Service Operations.

The above elements may be depicted in one or more diagrams.  Which and how many diagrams are needed depends on the chosen architecture description framework and complexity of the service.
-->
A description should be given.

## Service interfaces

<!--
Describe the interfaces of the service including the selected Message Exchange Pattern (MEP) by using an UML diagram5 that illustrates the service interfaces definitions and operations and in tabular form.

It is also recommended to describe the considerations resulting in the selection of a certain message exchange pattern.

A service interface supports one or several service operations. Depending on the message exchange pattern, service operations are either to be implemented by the service provider (e.g. in a Request/Response MEP, query operations are provided by the service provider – the service consumer uses them in order to submit query requests to the service provider), or by the service consumer (e.g. in a Publish/Subscribe MEP, publication operations are provided by the service consumer – the service provider uses them to submit publications to the service consumer). This distinction shall be clearly visualised in a service interface table (see example below): for each service interface, it shall be stated whether it is either provided or used by the Service. A service provides at least one service interface.
An example diagram and corresponding table is given below.
-->
This section describes the interfaces of the service including the selected Message Exchange Pattern (MEP) by using UML diagrams that illustrate the service interfaces definitions and operations and in tabular form.

![MSR Global Ledger Interface Definition Diagram](materials/Service-Interfaces.svg)

Service Interface | Role (from service provider point of view) | Service Operation
| --- | --- | --- |
| MsrAdminInterface        | Provided | addMsr \newline deleteMsr |
| MsrInterface             | Provided | registerServiceInstance \newline changeInstanceStatus |
| ServiceConsumerInterface | Provided | getMsrs \newline getServiceInstance \newline getServiceInstances \newline getServiceInstancesByKeyword \newline getServiceInstancesByDesign |

# Service data model

This section describes the information model, i.e., the logical data structures to be exchanged between providers and consumers of the service.

<!--
It is recommended to visualise the data structures by using UML diagrams.  The full information model (logical data structure) shall be shown using diagram(s) and explanatory tables (see below).
-->

![UML class diagram of data model](materials/msr-ledger-data-model.svg){ width=500px }

<!--
It is mandatory to give a description of each entity item (class), its attributes and the associations between entity items after each diagram showing data items.

If the service data model is related to an external data model (e.g. being a subset of a standard data model, e.g. based on an S-100 specification), then the service data model shall refer to it: each data item of the service data model shall be mapped to a data item defined in the external data model.  This mapping may be added in the same table that describes the data items and their attributes and associations.  The idea is: when reading the service specification (including the logical service data model), the payload structures shall become clear to the reader.  If the service re-uses structures of an external data model, then these structures can be referred to rather than replicated in the service specification.  The tabular presentation of the payload allows for providing references to an externally defined model.

The table below is an example for describing a service data model including traces to an external model.
-->

# Service interface specifications

This section describes the details of each service interface. One sub-section is provided for each Service Interface.
The Service Interface specification covers only the static design description while the dynamic design (behaviour) is described in section D 5.
<!--
The static interface description is vital since it describes how the interfaces shall be constructed.
Architectural elements applicable for this description are:
* Service Interfaces;
* Operations - function or procedures which enable programmatic communication with a Service via a Service interface;
* Parameters - constants or variables passed into or out of a Service interface as part of the execution of an Operation.
A Service may have one or more Service Interfaces.  Please describe each in separate sections below.
-->

## Service interface *MsrAdminInterface*
<!--
Please explain the purpose, message exchange pattern and architecture of the Interface.
A Service Interface supports one or several service operations.  Each operation in the service interface shall be described in the following sections.
-->
The *MsrAdminInterface* interface is used by administrators to add MSRs that should be allowed to register service instances in the ledger and also to them again if their privilege should be revoked for one reason or another.

### Operation *addMsr*
<!--
Give an overview of the operation: Include here a textual description of the operation functionality. In most situations this will be the same as the operation description taken from the UML modelling tool.
-->
The purpose of the *addMsr* operation is to allow administrators of the MSR Global Ledger to add MSR instances to the MSR Global Ledger's internal index of MSRs and at the same time give the added MSR instances permission to register service instances.

#### Operation functionality
<!--
Describe the functionality of the operation, i.e. how does it produce the output from the input payload.
-->
Upon receiving a request to add an MSR from a user, the MSR Ledger will first check if the user has the administrative permissions to do so. If the user does not have the necessary permissions, the MSR Ledger will stop execution and optionally return a response with the failure reason to the user.
If the user does have the necessary permissions, the MSR Ledger will create an *Msr* object representation of the MSR using the given the information, create an entry that maps from the given address of the MSR to the created representation in its internal index of MSRs and assign permissions for creating and updating service instances to the added MSR.

#### Operation parameters
<!--
Describe the logical data structure of input and output parameters of the operation (payload) by using an explanatory table (see below) and optionally UML diagrams (which are usually sub-sets of the service data model described in previous section above).
Figure 3 shows an example of a UML diagram (subset of the service data model, related to one operation).
-->

<!--
It is mandatory to provide a table with a clear description of each service operation parameter and the information about which data types defined in the service data mode are used by the service operation in its input and output parameters.
Note: While the descriptions provided in the service data model shall explain the data types in a neutral format, the descriptions provided here shall explicitly explain the purpose of the parameters for the operation.
-->
| Parameter (in) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| name | string | 1 | The name of the MSR that is to be added |
| url | string | 1 | The URL of the API of the MSR that is to be added |
| account | address | 1 | The account address in the MSR Ledger of the MSR that is to be added |

| Return Type (out) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| result from operation | none \| string | 1 | The result of the add operation. Will be empty if successful, else it will contain the failure reason as a string |

### Operation *deleteMsr*

The purpose of the *deleteMsr* operation is to allow administrators of the MSR Global Ledger to delete previously added MSR instances from the internal index and also revoke their permission to register service instances.

#### Operation functionality

Upon receiving a request to add an MSR from a user, the MSR Ledger will first check if the MSR has the necessary permissions to do so. If the MSR does not have the necessary permissions, the MSR Ledger will stop execution and optionally return a response with the failure reason to the user.
If the user does have the necessary permissions, the MSR Ledger will delete the MSR entry that maps from the given account address in its internal index and revoke the permissions of the MSR with the given account address.

#### Operation parameters

| Parameter (in) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| msrAddress | address | 1 | The account address of the MSR that is to be deleted |

| Return Type (out) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| result from operation | none \| string | 1 | The result of the delete operation. Will be empty if successful, else it will contain the failure reason as a string |

## Service Interface *MsrInterface*

The *MsrInterface* interface is used by MSR instances, that have necessary permissions, to register and change the status of service instances.

### Operation *registerServiceInstance*

The purpose of the *registerServiceInstance* operation is to allow MSR instances that have the necessary permissions to register service instances in the MSR Global Ledger.

#### Operation functionality

Upon receiving a request to register a service instance from an MSR instance, the MSR Ledger will first check if the MSR has the necessary permissions to do so. If the MSR does not have the necessary permissions, the MSR Ledger will stop execution and optionally return a response with the failure reason to the MSR.
If the MSR does have the necessary permissions, the MSR Ledger will update the received *ServiceInstance* object with the name and URL of the MSR that sent the request. Then the MSR Ledger will store the *ServiceInstance* object in its internal list of service instances and also index it according to the given list of keywords.

#### Operation parameters

| Parameter (in) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| instance | ServiceInstance | 1 | The service instance that should be registered |
| keywords | string | 0..* | A list of keywords that the service instance should be indexed by |

| Return Type (out) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| result from operation | none \| string | 1 | The result of the registering operation. Will be empty if successful, else it will contain the failure reason as a string |

### Operation *changeInstanceStatus*

The purpose of the *changeInstanceStatus* operation is to allow an MSR instance to update the status of a service instance it has previously registered.

#### Operation functionality

Upon receiving a request to change the status of an existing service instance, the MSR Ledger will check if the MSR has the necessary permissions to do so, and also that the MSR sending the request is the one that originally registered it. If any of these checks fail, the MSR Ledger will stop execution and optionally return a response with the failure reason to the MSR.
If the checks succeed, the MSR Ledger will update the service instance in question with the given service status.

#### Operation parameters

| Parameter (in) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| instanceMrn | string | 1 | The MRN of the service instance that is to be updated |
| instanceVersion | string | 1 | The version of the service instance that is to be updated |
| status | InstanceStatus | 1 | The instance status that the service instance is to updated with |

| Return Type (out) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| result from operation | none \| string | 1 | The result of the registering operation. Will be empty if successful, else it will contain the failure reason as a string |

## Service interface *ServiceConsumerInterface*

The *ServiceConsumerInterface* interface is used by service consumers to get the list of MSR instances that are registered and to get registered service instances.

### Operation *getMsrs*

The *getMsrs* operation allows service consumers to get the list MSR instances that are registered in the MSR Global Ledger.

#### Operation functionality

Upon receiving a request to get the list of MSR instances the MSR Ledger will return the list of MSR instances.

#### Operation parameters

| Parameter (in) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |

| Return Type (out) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| Msr | binary | 0..* | The list of MSR instances that are registered in the MSR Global Ledger |

### Operation *getServiceInstance*

The *getServiceInstance* operation allows service consumers to get a service instance with a specific MRN and version.

#### Operation functionality

Upon receiving a request for getting a service instance, the MSR Global Ledger will look up in its list of service instances to find one with the given MRN and version. If no service instance was found, the MSR Ledger will return a *ServiceInstance* object where all attributes are empty.

#### Operation parameters

| Parameter (in) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| instanceMrn | string | 1 | The MRN of the service instance to be returned|
| version | string | 1 | The version of the service instance to be returned |

| Return Type (out) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| ServiceInstance | binary | 1 | The service instance that was found based on the given parameters |

### Operation *getServiceInstances*

The *getServiceInstances* operation allows service consumers to get the list of all service instances that are registered in the MSR Global Ledger.

#### Operation functionality

Upon receiving a request to get the list of service instances, the MSR Ledger will return the list of all registered service instances.

#### Operation parameters

| Parameter (in) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |

| Return Type (out) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| ServiceInstance | binary | 0..* | The list of all service instances that are registered in the MSR Global Ledger |

### Operation *getServiceInstancesByKeyword*

The *getServiceInstancesByKeyword* operation allows service consumers to get the list of all registered service instance that have a given keyword.

#### Operation functionality

Upon receiving a request for getting service instances by a keyword, the MSR Global Ledger will look up in its index to find all service instances that have the given keyword in their lists of keywords. All the found service instances will be collected in a list which is then returned to the service consumer.

#### Operation parameters

| Parameter (in) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| keyword | string | 1 | The keyword that will be used to find service instances |

| Return Type (out) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| ServiceInstance | binary | 0..* | The list that contains all the registered service instances that have the given keyword |

### Operation *getServiceInstancesByDesign*

The *getServiceInstancesByDesign* operation allows service consumers to get the list of service instances that implement a given service design. **MAKE REFERENCE TO G1128 HERE**

#### Operation functionality

Upon receiving a request to the list of service instances that implement a given service design, the MSR Global Ledger will look up in its index to find all service instances that implement the given service design. All the found service instances will be collected in a list which is then returned to the service consumer.

#### Operation parameters

| Parameter (in) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| designMRN | string | 1 | The MRN of the service design that the service instances implement |
| designVersion | string | 1 | The version of the service design that the service instance implement |

| Return Type (out) | Encoding | Mult. | Description |
| ------ | --- | --- | --------- |
| ServiceInstance | binary | 0..* | The list that contains all the registered service instances that implement the given design MRN and version |

# Service dynamic behaviour
<!--
This section describes the interactive behaviour between service interfaces (interaction specification) and, if required, between different services (orchestration).  Architectural elements applicable for this description are:
* Service Interaction Specifications;
* Service State machines;
* Service orchestration.
Following types of views and UML diagrams can be used to describe the dynamic behaviour:
* Sequence diagrams;
* Interaction diagrams;
* State machine diagrams.
-->
A description should be given.

## Service interface INTERFACE NAME
<!--
Include some information about the dynamic aspects of the service interface; each operation shall be exposed on at least one diagram.
An example sequence diagram is shown in Figure 4.
-->
A description should be given.

## Service orchestration (Optional)
<!--
This section shall be provided, if the composition of the service and/or the relation to other services (e.g., which other services are used to provide this service; which other services are intended to use this service) is deemed relevant for the service specification.
An example sequence diagram is given below. This very simple example indicates that the AddressForPersionLookupService (i.e., the service that is being described in this Service Specification Document) acts as a consumer of a “notifyAddressChange” operation of another service, called “AddressForPersionService”. Note that the other service needs to be described by its own Service Specification Document; a reference to that document shall be added here).
-->
A description should be given.

# Service provisioning (Optional)

<!--
This section shall describe the way services are planned to be provided and consumed.  It is labelled optional since one of the key aspects of service-orientation is to increase flexibility of the overall system by separating the definition of services from their implementation.  This means that a service can be provided in several different contexts that are not necessarily known at the time, when the service is designed.
-->
A description should be given.

# Definitions

The definitions of terms used in this document can be found in the International Dictionary of Marine Aids to Navigation (IALA Dictionary) at http://www.iala-aism.org/wiki/dictionary and were checked as correct at the time of going to print.  Where conflict arises, the IALA Dictionary shall be considered as the authoritative source of definitions used in IALA documents.

## Terminology

Persons producing the Technical Service are invited to add definitions to the following list as appropriate.

Term | Definition
---  | ---
IALA | International Association of Marine Aids to Navigation and Lighthouse Authorities
IMO  | International Maritime Organization
MCC  | Maritime Connectivity Platform Consortium
MCP  | Maritime Connectivity Platform
MIR  | Maritime Identity Registry
MRN  | Maritime Resource Name
MSR  | Maritime Service Registry

# References