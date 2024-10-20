# PLASMA
## Policy Language for Solid's Metadata-based Access Control

PLASMA proposes a "policy language" that wraps Solid's existing access control
mechanisms, and enables data and legal governance within the Solid ecosystem.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.10259728.svg)](https://doi.org/10.5281/zenodo.10259728)

Cite this work: Esteves, Beatriz, and Harshvardhan J. Pandit. "Using Patterns to Manage Governance of Solid Apps." (2023). https://ceur-ws.org/Vol-3636/paper5.pdf 

## Goals

1. *Providing a vocabulary of Solid's actors, roles, and processes (RO1)*:
Currently, Solid has [Vocabularies](https://solid.github.io/vocab/) [Solid-Vocab],
[Web Access Control](https://solid.github.io/web-access-control-spec/) [WAC],
and an [Access Control Policy](https://solid.github.io/authorization-panel/acp-specification) [ACP]
language that do not include specific actors and processes, e.g. Providers for
Pods, Infrastructure (e.g. Servers), Apps' services - through which implementers
can accurately describe their use of Solid, and which is necessary towards
understanding its legal compliance implications. Therefore, the first step is to
identify relevant concepts for representing Solid's information flows and
processes, and to create a lightweight vocabulary. 

2. *Align Solid's taxonomy with [GDPR](http://data.europa.eu/eli/reg/2016/679/oj) [GDPR]
concepts (RO2)*: This step will identify relevance and alignments between
(identified) Solid and (existing) GDPR concepts regarding roles, information
flows, and legal compliance requirements. This will be achieved by extending the
existing [reports](https://go.digita.ai/reuse-patterns) [Digita-Patterns],
[Data Privacy Vocabulary](https://w3id.org/dpv) [DPV], and
[use of ODRL for Solid policies](https://doi.org/10.1109/EuroSPW54576.2021.00038) [Solid-ODRL]
as a State-of-the-Art resource providing comprehensive vocabularies (e.g., data
categories, legal roles, jurisdictions, etc.) that can be used in a
jurisdiction-agnostic manner or specifically for laws such as GDPR. The output
will be the _PLASMA_ vocabulary to integrate the identified concepts from RO1
within the larger framework of 
[Open Digital Rights Language](https://www.w3.org/TR/odrl-model/) [ODRL] and
DPV's vocabularies.

3. *Creating a "machine-readable privacy policy" (RO3)*: PLASMA will be used to
create a machine-readable specification for expressing various kinds of policies
that will enable representing information about actors, processes, information
flows, and legal compliance concepts for Solid's implementations and use-cases.
PLASMA will complement the existing Solid ACP and will enable a higher-degree of
information representation for conventional information, such as what data is
required, who is using it for what purposes, and on what legal basis. 

## Benefits

PLASMA will enable providers and consumers of Solid infrastructure, apps, 
services, and data to create and use innovative features based on Linked Data
fundamentals and semantics, such as: automated consent/permission notice
generation, alignment between provider and consumer policies, performing
user-side risk assessments (e.g. privacy concerns), and assisting Pod and App
developers and providers in expressing their use-cases, and understanding legal
requirements (e.g. providing a textual privacy policy). An example of policies
being used in such tasks is the creation of a
[policy editor](https://doi.org/10.1007/978-3-031-11609-4_3). These features
require automation, which is only possible when the necessary information is
provided in a machine-readable form and has the necessary semantic
interoperability to be useful within the Solid ecosystem.

PLASMA will also provide a comprehensive overview and recommendations on
specific topics that will act as the starting point for any future research
regarding Solid and GDPR, and will assist the community by breaking down the
current complexities of 'law & tech' into specific sub-topics that can then be
addressed. This will be done by taking each specific topic (e.g. personal data,
purpose, processing, legal basis, legal role - controller, processor) and
expressing how it applies to Solid, what GDPR expects, what are the questions to
ask, and finding the answers through the application of developed
machine-readable policy. This work will also assist Solid and the semantic web
community in general regarding addressing future regulations within the EU
(especially the Data Governance Act, Data Act, and Data Spaces) and other
jurisdictions through the use of the Data Privacy Vocabulary [DPV] as the
underlying semantic vocabulary - which can act as a semantic interoperability
layer to represent and communicate legal compliance information across diverse
use-cases and locations.

## References

- [ACP] Access Control Policy (ACP): https://solid.github.io/authorization-panel/acp-specification
- [Digita Patterns] Data Sharing Patterns as a Tool to Tackle Legal
  Considerations about Data Reuse with Solid: Theory and Applications in Europe.
  De Bot, and Haegemans (2021): https://go.digita.ai/reuse-patterns
- [DPV] Data Privacy Vocabulary (DPV): https://w3id.org/dpv
- [GDPR] General Data Protection Regulation: http://data.europa.eu/eli/reg/2016/679/oj
- [ODRL] Open Digital Rights Language: https://www.w3.org/TR/odrl-model/
- [Solid-ODRL] ODRL Profile for Expressing Consent through Granular Access
  Control Policies in Solid. Esteves, Pandit, Doncel (2021):
  https://doi.org/10.1109/EuroSPW54576.2021.00038 Open Access links:
  https://harshp.com/research/publications/048-odrl-profile-consent-solid-acp
- [Solid-Vocab] Solid Vocabularies: https://solid.github.io/vocab/
- [SOPE] Using the ODRL Profile for Access Control for Solid Pod Resource
  Governance. Esteves, Doncel, Pandit, Mondada, McBennett. Extended Semantic Web
  Conference (ESWC): https://doi.org/10.1007/978-3-031-11609-4_3
- [WAC] Web Access Control: https://solid.github.io/web-access-control-spec/

## Funding

Beatriz Esteves has received funding from the European Union’s Horizon 2020
research and innovation programme under the Marie Skłodowska-Curie grant
agreement No 813497 (PROTECT). 

Harshvardhan J. Pandit has received funding from the ADAPT SFI Centre for
Digital Media Technology is funded by Science Foundation Ireland through the SFI
Research Centres Programme and is co-funded under the European Regional
Development Fund (ERDF) through Grant #13/RC/2106_P2, and by the Short Term
Scientific Mission (STSM) grants from
[COST ACTION CA19134 Distributed Knowledge Graphs (DKG)](https://cost-dkg.eu/) - 
funded by the Horizon 2020 Framework Programme of the European Union.