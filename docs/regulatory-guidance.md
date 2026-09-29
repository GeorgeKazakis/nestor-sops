# Legal, regulatory and ethical guidance

Data-driven methods in reproductive medicine sit at the intersection of several legal regimes. Some apply from the first moment patient data are used; others apply only once a method is placed on the market or used to inform patient care. This chapter summarises the frameworks most relevant to NESTOR partners and relates them to the stages in [Table 2](clinical-translation.md#table-2). It is intended as practical orientation for researchers and developers, not as legal advice. Institutional data protection officers, ethics committees, regulatory affairs staff and, where necessary, national competent authorities should be consulted for specific cases.

!!! info "Regulatory sources checked: 29 September 2026"
    The Commission reports revised AI Act high-risk application dates, a proposed MDR/IVDR revision, SoHO application from August 2027 and phased EHDS implementation. See the [dated source register](#implementation-status-sources). Check the applicable provisions when planning a study or changing its intended purpose.

Start with the [workflow checkpoints](#table-4), then consult the supporting framework below. The evidence stages organise validation work; legal scope must be assessed for the actual method and activity.

<span id="table-3"></span>

**Table 3. Overview of the main legal and ethical instruments**

| Instrument | What it governs | Relevance to NESTOR validation work | When it applies |
| --- | --- | --- | --- |
| GDPR (EU) 2016/679 and national laws [7](references.md#ref-7) | Processing of personal data, including health and genetic data. | Use of embryo images, clinical records and genomic data linked to patients. | From Stage A onwards. |
| MDR (EU) 2017/745 [8](references.md#ref-8) | Medical devices, including software, placed on the market or used in health institutions. | Software intended to support conception, such as embryo assessment tools. | Assess intended purpose and study activity from the outset; clinical investigation and clinical-use requirements apply where relevant. |
| IVDR (EU) 2017/746 [9](references.md#ref-9) | In vitro diagnostic devices, including software. | Genomic tests such as non-invasive PGT, NIPT and receptivity tests, and their analysis software. | Assess intended purpose and any performance-study requirements from the outset. |
| AI Act (EU) 2024/1689, as amended by (EU) 2026/1744 [10](references.md#ref-10), [11](references.md#ref-11) | AI systems; high-risk requirements for AI in regulated products. | AI-based medical device software requiring notified-body assessment. | High-risk product rules apply from 2 August 2028 under the Commission’s current timeline; research exclusions have specific conditions. |
| SoHO Regulation (EU) 2024/1938 [12](references.md#ref-12) | Quality and safety of substances of human origin, including gametes and embryos. | Quality management in ART establishments; authorisation of new SoHO preparations and processes. | From 7 August 2027. |
| EHDS Regulation (EU) 2025/327 [13](references.md#ref-13) | Primary and secondary use of electronic health data. | Future route for accessing multi-country health data for research and innovation. | Phased; secondary use mainly from March 2029. |
| National ART, research and ethics laws | Embryo protection, medically assisted reproduction and research on human subjects. | Consent, permitted uses of treatment data, ethics review. | From Stage A onwards. |

<span id="section-3-1"></span>

## Data protection

**Personal data in embryo image analysis.** Embryos are not data subjects under the GDPR. However, time-lapse images and their associated metadata are linked to patients’ treatment records and therefore relate to identifiable individuals, the prospective parents. Such data are health data, and genomic data derived from embryos or patients are genetic data. Both belong to the special categories of Article 9 GDPR. For the originating institution, pseudonymised data linked back to patients remain personal data. Pseudonymisation should not be treated as anonymisation; assess identifiability and the available means of re-identification for the processing in question. Only data that have been effectively anonymised, with no reasonably likely means of re-identification, fall outside the GDPR. For rich clinical and image datasets this threshold is difficult to reach, so partners should generally assume that the GDPR applies.

**Lawful basis for research.** Processing requires both a lawful basis under Article 6 and a condition under Article 9(2). For scientific research, Article 9(2)(j) permits processing where it is based on EU or national law and is subject to appropriate safeguards under Article 89(1), such as data minimisation and pseudonymisation. Explicit consent (Article 9(2)(a)) is an alternative, but it is not always the most suitable basis for retrospective research on routinely collected treatment data.

**National divergence.** Article 9(4) allows Member States to introduce further conditions for health and genetic data, and research safeguards are largely defined nationally. In the NESTOR countries, the relevant implementing laws are the Dutch GDPR Implementation Act (UAVG), the Estonian Personal Data Protection Act and Greek Law 4624/2019 [17](references.md#ref-17). These differ in how they treat research without consent, in the role of ethics committees and in the conditions for further processing. A dataset that can be used lawfully in one country may therefore require a different justification, or additional safeguards, in another. This is one of the main practical obstacles to cross-border validation, and it is why the documentation described in [Chapter 4](harmonisation.md) includes the lawful basis at each site.

**Roles and agreements across sectors.** When an SME and a hospital work together, their roles must be defined. The hospital is usually the controller of patient data. A company that analyses data on the hospital’s instructions acts as a processor and needs a data processing agreement (Article 28). Partners who jointly determine the purposes and means of a study are joint controllers and need an arrangement under Article 26. Seconded researchers working within a host institution’s environment should be covered by that institution’s confidentiality and access procedures.

**Data protection impact assessment.** Screen the planned processing under Article 35 and the competent authority’s requirements. A DPIA is required where processing is likely to create a high risk to individuals, including large-scale processing of special-category data; the use of new technology is relevant to that assessment. Record the screening outcome and update any DPIA when the processing changes. See [GDPR Article 35](references.md#ref-7).

**Keeping data in place.** The embryo-analysis work in this deliverable was carried out within the approved computing environment at MUMC+, because restrictions on data transfer applied. This “model-to-data” approach, in which the analysis is brought to the data rather than the other way round, reduces transfer risk and simplifies cross-border compliance. It is recommended as the default for NESTOR multi-site validation ([Section 4.4](harmonisation.md#section-4-4)).

<span id="section-3-2"></span>

## Medical device and in vitro diagnostic regulation

**Qualification.** Under Article 2(1) of the MDR, software intended by its manufacturer to be used for purposes including diagnosis, prediction or prognosis of disease, or the “control or support of conception”, is a medical device. Software that assesses embryos to support selection for transfer is therefore likely to qualify as a medical device. Software that analyses specimens examined in vitro, such as genomic data from spent culture medium, cell-free DNA or endometrial biopsies, will generally fall under the IVDR. Qualification depends on the intended purpose stated by the manufacturer, not on the technology itself. The Medical Device Coordination Group guidance MDCG 2019-11 on software qualification and classification [18](references.md#ref-18) should be consulted. This is why intended use is recorded at Step 1 of the workflow ([Section 5.1](practical-workflow.md#section-5-1)).

**Classification.** Under MDR Annex VIII, Rule 11, software that provides information used to make decisions for diagnostic or therapeutic purposes is classified at least as class IIa, which requires assessment by a notified body. Under the IVDR, most genetic tests fall in class C.

**Research use.** Assess the software’s intended purpose and the study activity before deciding which requirements apply. A research label alone does not exclude a medical device investigation or an IVD performance study from regulation, even when outputs do not guide treatment. Document the applicable study or clinical-use route with the institution’s regulatory staff before starting the activity or changing its purpose. See the [MDR](references.md#ref-8), [IVDR](references.md#ref-9) and [software qualification guidance](references.md#ref-18).

**The in-house exemption and its limits.** Article 5(5) provides a conditional route for devices manufactured and used within EU health institutions. Requirements include appropriate quality management, a public declaration and compliance with applicable general safety and performance requirements. The device must not be transferred to another legal entity; this restriction also matters within one country. Detailed conditions and application dates differ between the MDR and IVDR, so assess the relevant regulation rather than using one combined checklist. Sharing a written protocol is distinct from transferring a device. See [MDCG 2023-1](https://health.ec.europa.eu/system/files/2023-01/mdcg_2023-1_en.pdf).

For multi-site work, determine the appropriate research, investigation or clinical-use route at each institution. The Commission’s December 2025 simplification proposal is described on its [medical devices overview](https://health.ec.europa.eu/medical-devices-new-regulations/overview_en); proposed changes should not be treated as applicable law.

**Quality and technical standards.** The standards commonly used to demonstrate conformity provide a useful template even at the research stage. They include ISO 13485 for quality management, IEC 62304 for the software life cycle, ISO 14971 for risk management and, for laboratories, ISO 15189 [20](references.md#ref-20). Adopting their core habits early, such as version control, documented requirements and risk registers, makes later conformity assessment far less costly. NESTOR SMEs already hold experience with these standards, which is a key cross-sectoral asset for academic partners.

<span id="section-3-3"></span>

## Artificial intelligence regulation

**Research exclusion.** The AI Act does not apply to AI systems developed and put into service for the sole purpose of scientific research and development (Article 2(6)). It also does not apply to research, testing and development before a system is placed on the market, with the exception of testing in real-world conditions (Article 2(8)). Assess these conditions for each activity rather than inferring exclusion from Stage A or B alone. See the [AI Act Article 2 scope provisions](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-2).

**High-risk classification.** An AI system is high-risk under Article 6(1) if it is, or is a safety component of, a product covered by the legislation listed in Annex I that requires third-party conformity assessment. The MDR and IVDR are on that list. An AI-based embryo assessment tool that is a class IIa or higher medical device would therefore be a high-risk AI system. Following the amendment adopted in 2026 [11](references.md#ref-11), the high-risk obligations for such products apply from 2 August 2028. The Commission’s MDR/IVDR proposal would change how the AI Act interacts with the medical device framework, which may affect this classification in future.

**What the requirements mean for validation.** Where research falls within an exclusion, the high-risk requirements can still inform preparation for later clinical use. They map onto the five-stage workflow:

- a risk management system (Article 9), which corresponds to defining unacceptable errors at Step 1;

- data governance, including relevance, representativeness and examination for possible biases (Article 10), which corresponds to Step 2;

- technical documentation and record-keeping (Articles 11 and 12), which corresponds to the model record in Step 3;

- transparency, human oversight, and accuracy and robustness (Articles 13 to 15), which correspond to Steps 4 and 5.

Documentation produced according to this workflow can therefore form the basis of future AI Act technical documentation.

<span id="section-3-4"></span>

## Substances of human origin and assisted reproduction law

**SoHO Regulation.** Regulation (EU) 2024/1938 on substances of human origin [12](references.md#ref-12) will replace the EU Tissues and Cells Directives from 7 August 2027 and applies to gametes and embryos. It requires SoHO entities, including ART establishments, to operate a quality management system and to obtain authorisation for new SoHO preparations. Such an application must be supported by a benefit–risk assessment and, where appropriate, clinical outcome monitoring. Whether and how an AI-supported embryo assessment method affects this authorisation is a matter for national competent authorities. At a minimum, clinics should expect to document such tools within their quality systems. Validation evidence produced according to these guidelines will support that documentation.

**National ART law.** The use of embryos and treatment data is also governed by national legislation, which differs between NESTOR countries. Relevant laws include the Dutch Embryo Act (Embryowet), Greek Law 3305/2005 on medically assisted reproduction (with oversight by the National Authority for Medically Assisted Reproduction) and the Estonian Artificial Insemination and Embryo Protection Act. The analysis of images recorded during routine treatment does not in itself involve embryo research. However, the consent given for treatment and the permitted secondary uses of treatment data must be checked under the applicable national law at each site.

<span id="section-3-5"></span>

## Research ethics and patient perspectives

**Ethics review.** Each site contributing data should obtain the appropriate ethics review under national rules. In the Netherlands, a medical research ethics committee determines whether a study falls under the Medical Research Involving Human Subjects Act (WMO). Retrospective studies on existing data are often outside the WMO but remain subject to institutional review and the GDPR. Greece and Estonia have their own review procedures. The revised Declaration of Helsinki (2024) [14](references.md#ref-14) remains the reference for research involving identifiable human data. NESTOR’s Ethics and Gender Management Plan records the approvals obtained for project activities.

**Responsible claims.** Validation findings should be communicated with care. Patients undergoing ART are a vulnerable group, and they are exposed to commercial claims about add-ons whose benefit is unproven. Findings from a research-stage study must not be presented as evidence of clinical benefit ([Section 5.5](practical-workflow.md#section-5-5)).

**Equity and representativeness.** Methods validated only on selected populations may perform worse for others, for example for patients of advanced reproductive age, a central concern of NESTOR. Validation datasets should be described in terms of the populations they represent, and performance should be reported for relevant subgroups where numbers allow.

**Patient engagement.** NESTOR’s Advisory Board includes patient representation through Fertility Europe, as well as experts in privacy law and biomedical ethics. Their perspectives should inform the definition of intended use and acceptable error, and the way validation results are communicated to patients.

<span id="section-3-6"></span>

## Health data governance: the European Health Data Space

The EHDS Regulation (EU) 2025/327 creates an EU-wide framework for the secondary use of electronic health data for research, innovation and policy. Access will be managed through national health data access bodies and secure processing environments. Most of the secondary-use rules apply from March 2029, and certain data categories, including genetic data, will follow later. The EHDS will not change the validation principles in these guidelines. However, it will offer a structured legal route to multi-country datasets, and it reinforces the model-to-data approach through its reliance on secure processing environments. Metadata and data-quality practices adopted now ([Chapter 4](harmonisation.md)) will ease future participation.

<span id="section-3-7"></span>

## Regulatory checkpoints in the practical workflow

[Table 4](regulatory-guidance.md#table-4) translates the frameworks above into checkpoints for each stage of the practical workflow described in [Chapter 5](practical-workflow.md).

<span id="table-4"></span>

**Table 4. Legal, regulatory and ethical checkpoints by workflow stage**

| Workflow stage | Checkpoints |
| --- | --- |
| [1. Task definition](practical-workflow.md#section-5-1) | Write down the intended purpose, the intended user and the target population. Assess whether the intended purpose would make the method a medical device or IVD, and whether it remains within the research exclusion. Confirm the need for ethics review and screen for a DPIA. |
| [2. Data description](practical-workflow.md#section-5-2) | Record the lawful basis and consent or opt-out status at each site. Complete a DPIA where required, and put data processing or joint-controllership agreements in place. Record where processing takes place, and apply data minimisation and pseudonymisation. Describe the representativeness of the data and known gaps (cf. AI Act Art. 10). |
| [3. Model identification](practical-workflow.md#section-5-3) | Keep a version-controlled model record covering code, weights, configuration and input preparation (cf. IEC 62304). Record the ownership and licensing of models and data (cf. the NESTOR IP management plan). |
| [4. Evaluation and visual review](practical-workflow.md#section-5-4) | Pre-specify acceptance and exclusion criteria. Document the reference standard and who produced it. Describe the role of human review (cf. AI Act Art. 14) and record identified failure modes in a risk register (cf. ISO 14971). |
| [5. Documentation and interpretation](practical-workflow.md#section-5-5) | Report according to recognised guidelines (TRIPOD+AI, CLAIM; DECIDE-AI for early clinical evaluation). State the stage of evidence reached ([Table 2](clinical-translation.md#table-2)) and avoid claims of clinical benefit that the evidence does not support. Archive records according to the data management plan. |

*Source: D3.3, Chapter 3. See the [full deliverable](references.md#downloads).*

## Implementation status sources

These official sources were checked on **29 September 2026**. Review them alongside the legal text for a new study or a change of intended use.

| Topic | Source and implementation status |
| --- | --- |
| AI Act timeline | The Commission’s [AI Omnibus notice](https://digital-strategy.ec.europa.eu/en/news/ai-omnibus-enters-force) reports entry into force on 27 July 2026, with high-risk Annex III rules applying from 2 December 2027 and Annex I product rules from 2 August 2028. |
| Medical devices revision | The Commission’s [overview](https://health.ec.europa.eu/medical-devices-new-regulations/overview_en) describes COM(2025) 1023 as a proposal. Use the applicable regulations while the proposal is considered. |
| SoHO | The Commission’s [SoHO implementation page](https://health.ec.europa.eu/blood-tissues-cells-and-organs/soho-regulation/new-eu-rules-substances-human-origin_en) gives 7 August 2027 as the general application date, with a further year for some provisions. |
| EHDS | The Commission’s [EHDS overview](https://health.ec.europa.eu/ehealth-digital-health-and-care/european-health-data-space-regulation-ehds_en) describes phased implementation, with most secondary-use rules from March 2029 and remaining categories, including genomic data, from March 2031. |
| In-house devices | [MDCG 2023-1](https://health.ec.europa.eu/system/files/2023-01/mdcg_2023-1_en.pdf) explains Article 5(5), the legal-entity restriction and differences between MDR and IVDR conditions. |

Record study-specific conclusions, the sources consulted and the responsible reviewer in the study documentation.
