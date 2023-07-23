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

    **(CQ1.)** What is the unique identifier of the policy?
    **(CQ2.)** Who is the creator of the policy?
    **(CQ3.)** When was the policy issued?
    **(CQ4.)** Who is the assignee of the policy?
    **(CQ5.)** What application/service is being used to access the data?
    **(CQ6.)** What access mode is being requested?
    **(CQ7.)** What personal data is being accessed?
    **(CQ8.)** What is the purpose for accessing the data?

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
      odrl:rightOperand ex:AcademicResearchProjectX ] ] .

:userA a plasma:User .

:userB a plasma:DataSubject .

:applicationA a plasma:App .

:AcademicResearchProjectX a dpv:AcademicResearch ;
  rdfs:label "Conduct research in the academic project X." .
```

## ODPs for logs

### ODP for data logs

![ODP for a data log](./img/log-odp.png)

## ODPs for registries

### ODP for data registries

![ODP for a data registry](./img/registry-odp.png)