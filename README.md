# PLASMA
## Policy Language for Solid's Metadata-based Access Control

PLASMA is an attempt at proposing a "policy language" that wraps Solid's existing access control mechanisms and enables data and legal governance within the Solid ecosystem. 

## Goals

1. *Providing an ontology of Solid's actors, roles, and processes (RO1)*: Currently, Solid has [Vocabularies](https://solid.github.io/vocab/) [Solid-Vocab], [Web Access Control](https://solid.github.io/web-access-control-spec/) [WAC], and an [Access Control Policy](https://solid.github.io/authorization-panel/acp-specification) [ACP] language which does not include specific actors and processes e.g. Providers for Pods, Infrastructure (e.g. Servers), Apps' services - through which implementers can accurately describe their use of Solid, and which is necessary towards understanding its legal compliance implications. Therefore, the first step is to identify relevant concepts for representing Solid's information flows and processes and create a lightweight ontology. 

2. *Align Solid's taxonomy with [GDPR](http://data.europa.eu/eli/reg/2016/679/oj) [GDPR] concepts (RO2)*: This step will identify relevance and alignments between (identified) Solid and (existing) GDPR concepts regarding roles, information flows, and legal compliance requirements. This will be achieved by extending the existing [reports](https://go.digita.ai/reuse-patterns) [Digita-Patterns], [Data Privacy Vocabulary](https://w3id.org/dpv) [DPV], and [use of ODRL for Solid policies](https://doi.org/10.1109/EuroSPW54576.2021.00038) [Solid-ODRL] as a State of the Art resource providing comprehensive vocabularies ( data categories, legal roles, jurisdictions, etc.) that can be used in a jurisdiction-agnostic manner or specifically for laws such as GDPR. The output will be the _PLASMA_ ontology to integrate the identified concepts from RO1 within the larger framework of [Open Digital Rights Language](https://www.w3.org/TR/odrl-model/) [ODRL] and DPV's vocabularies.

3. *Creating a "machine-readable privacy policy" (RO3)*: PLASMA will be used to create a machine-readable specification for expressing various kinds of policies that will enable representing information about actors, processes, information flows, and legal compliance concepts for Solid's implementations and use-cases. PLASMA will complement the existing Solid ACP and will enable a higher-degree of information representation for conventional information such as what data is required, who is utilising it for what purposes and on what legal basis. 

## Benefits

PLASMA will enable providers and consumers of Solid infrastructure, apps, service, and data to create and utilise innovative features based on linked data fundamentals and semantics, such as: automated consent/permission notice generation, alignment between provider and consumer policies, performing user-side risk assessments (e.g. privacy concerns), and assisting Pod and App developers and providers in expressing their use-case and understanding legal requirements (e.g. providing a textual privacy policy). An example of policies being used in such tasks is the creator of a [policy editor](https://doi.org/10.1007/978-3-031-11609-4_3) These features require automation which is only possible when the necessary information is provided in a machine-readable form and has the necessary semantic interoperability to be useful within the Solid ecosystem.

PLASMA will also provide a comprehensive overview and recommendations on specific topics that will act as the starting point for any future research regarding Solid & GDPR, and will assist the community by breaking down the current complexities of 'law & tech' into specific sub-topics that can then be addressed. This will be done by taking each specific topic (e.g. personal data, purpose, processing, legal basis, legal role - controller, processor) and expressing how it applies to Solid, what GDPR expects, what are the questions to ask, and finding some answers through the application of developed machine-readable policy. This work will also assist Solid and the semantic web community in general regarding addressing future regulations within EU (especially Data Governance Act, Data Act, and Data Spaces) and other jurisdictions through the utilisation of Data Privacy Vocabulary [DPV] as the underlying semantic vocabulary - which can act as a semantic interoperability layer to represent and communicate legal compliance information across diverse use-cases and locations.

## References

- [ACP] Access Control Policy (ACP) https://solid.github.io/authorization-panel/acp-specification
- [Digita Patterns] Data Sharing Patterns as a Tool to Tackle Legal Considerations about Data Reuse with Solid: Theory and Applications in Europe. De Bot, and Haegemans (2021) https://go.digita.ai/reuse-patterns
- [DPV] Data Privacy Vocabulary (DPV) https://w3id.org/dpv
- [GDPR] General Data Protection Regulation http://data.europa.eu/eli/reg/2016/679/oj
- [ODRL] Open Digital Rights Language https://www.w3.org/TR/odrl-model/
- [Solid-ODRL] ODRL Profile for Expressing Consent through Granular Access Control Policies in Solid. Esteves, Pandit, Doncel (2021) https://doi.org/10.1109/EuroSPW54576.2021.00038 Open Access links: https://harshp.com/research/publications/048-odrl-profile-consent-solid-acp
- [Solid-Vocab] Solid Vocabularies https://solid.github.io/vocab/
- [SOPE] Using the ODRL Profile for Access Control for Solid Pod Resource Governance. Esteves, Doncel, Pandit, Mondada, McBennett. Extended Semantic Web Conference (ESWC). https://doi.org/10.1007/978-3-031-11609-4_3
- [WAC] Web Access Control https://solid.github.io/web-access-control-spec/

## Funding

This work has been made possible by funding from the Short Term Scientific Mission (STSM) grants from [COST ACTION CA19134 Ditributed Knowledge Graphs (DKG)](https://cost-dkg.eu/) - funded by the Horizon 2020 Framework Programme of the European Union. The author (Harshvardhan J. Pandit) has received funding from the ADAPT SFI Centre for Digital Media Technology is funded by Science Foundation Ireland through the SFI Research Centres Programme and is co-funded under the European Regional Development Fund (ERDF) through Grant #13/RC/2106_P2.
