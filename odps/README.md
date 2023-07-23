# Ontology Design Patterns (ODPs) for PLASMA

**Table of Contents**

- [Ontology Design Patterns (ODPs) for PLASMA](#ontology-design-patterns-odps-for-plasma)
  * [Namespaces](#namespaces)
  * [ODPs for policies](#odps-for-policies)
    + [ODP for data requests](#odp-for-data-requests)
  * [ODPs for logs](#odps-for-logs)
    + [ODP for data logs](#odp-for-data-log)
  * [ODPs for registries](#odps-for-registries)
    + [ODP for data registries](#odp-for-data-registry)

## Namespaces

## ODPs for policies

### ODP for data requests

The pattern for a data request policy aims to answer the following competency questions:

**(CQ1)** What is the unique identifier of the policy?

**(CQ2)** Who is the creator of the policy?

**(CQ3)** When was the policy issued?

**(CQ4)** Who is the assignee of the policy?

**(CQ5)** What application/service is being used to access the data?

**(CQ6)** What access mode is being requested?

**(CQ7)** What personal data is being accessed?

**(CQ8)** What is the purpose for accessing the data?

A visualisation of the pattern is presented in the figure below:

![ODP for a data request](./img/policy-odp.png)

The pattern is used in the example below to represent a data request policy created by `userA` with `applicationA` to `Read` `Age` data from `userB` to conduct research in the academic project X.

```turtle
:request1 a odrl:Request, plasma:DataRequest;
  odrl:uid :request1 ;
  odrl:profile oac: ;
  dct:description "Request to use age data for academic research." ;
  dct:creator :userA ;
  dct:issued "2023-05-08T18:15:56"^^xsd:dateTime ;
  odrl:permission [
    odrl:assignee :userB ;
    oac:application :applicationA ;
    odrl:action oac:Read ;
    odrl:target oac:Age ;
    odrl:constraint [
      dct:title "Purpose for access is to conduct research in the academic project X." ;
      odrl:leftOperand oac:Purpose ;
      odrl:operator odrl:eq ;
      odrl:rightOperand :AcademicResearchProjectX ] ] .

:userA a plasma:User .

:userB a plasma:DataSubject .

:applicationA a plasma:App .

:AcademicResearchProjectX a dpv:AcademicResearch ;
  rdfs:label "Conduct research in the academic project X." .
```

## ODPs for logs

### ODP for data logs

The pattern for a data log aims to answer the following competency questions:

**(CQ1)** What type of action, e.g., create, update, erase, is being performed to the data?

**(CQ2)** Who is the entity interacting with the data?

**(CQ3)** Who is the entity publishing the log?

**(CQ4)** When was the log issued?

**(CQ5)** Where is the data being stored?

**(CQ6)** What application/service is being used to generate the data, if any?

A visualisation of the pattern is presented in the figure below:

![ODP for a data log](./img/log-odp.png)

The pattern is used in the example below to represent a data log created by Beatriz when a new resource was created and stored at `https://solidweb.me/besteves4/energyConsumption/july-2023.ttl`.

```turtle
:datalog1 a as:Create ;
  dct:issued "2023-07-02T23:01:15"^^xsd:dateTime ;
  as:summary "Beatriz added new resource to the Pod" ;
  as:object <https://solidweb.me/besteves4/energyConsumption/july-2023.ttl> ;
  as:actor <https://solidweb.me/besteves4/profile/card#me> ;
  dct:publisher <https://solidweb.me/besteves4/profile/card#me> .
```
## ODPs for registries

### ODP for data registries

The pattern for a data registry aims to answer the following competency questions:

**(CQ1)** Who is the maintaining the registry?

**(CQ2)** When was the registry created/updated?

**(CQ3)** What types of data are available?

**(CQ4)** Where is a specific type of data being stored?

**(CQ5)** What policy is associated with the data?

A visualisation of the pattern is presented in the figure below:

![ODP for a data registry](./img/registry-odp.png)

The pattern is used in the example below to record a dataset with `Contact` data, stored at `https://solidweb.me/besteves4/personalContacts/contactList.ttl` which has a policy associated with it.

```turtle
:dataregistry a dcat:Catalog ;
  dct:created "2023-07-01T13:21:18"^^xsd:dateTime ;
  dct:publisher :DRappProvider ;
  dcat:dataset :dataset1 .

:DRappProvider a plasma:AppProvider .

:dataset1 a dcat:Dataset ;
  dpv:hasPersonalData dpv-pd:Contact ;
  foaf:page <https://solidweb.me/besteves4/personalContacts/contactList.ttl> ;
  odrl:hasPolicy :policy2 .

:policy2 a odrl:Policy .
```