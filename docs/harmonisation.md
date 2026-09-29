# Harmonisation across sites

<span id="section-4-1"></span>

## Why harmonisation matters

Validation across several sites is only informative if the sites are measuring the same thing in comparable ways. Without harmonisation, differences in performance between sites cannot be interpreted. They may reflect genuine differences in the method’s behaviour, or merely differences in how images were acquired, how structures were annotated, or which cases were excluded. Poorly harmonised data can also make a method look better than it is: if site-specific features correlate with outcomes, a model can learn the site rather than the biology.

For NESTOR, harmonisation also has a capacity-building purpose. Shared procedures allow partners in Estonia and Greece to contribute data and expertise to multi-centre studies on equal terms, and they give clinics a common language in which to discuss methods with technology developers. The Description of Action accordingly foresees harmonised TLM data collection protocols, harmonised data collection at AN, and clinical guidelines disseminated to ART providers for the harmonisation of clinical care practices.

<span id="section-4-2"></span>

## Principles

- A common minimum, not uniformity. Partners do not need identical equipment or laboratory protocols. They need to agree on a minimum dataset, shared definitions and shared documentation, and to record how they differ.

- Shared vocabulary. Morphological and morphokinetic terms should follow the updated ESHRE/ALPHA Istanbul consensus (2025) [21](references.md#ref-21), and time-lapse practice should follow the ESHRE good practice recommendations on time-lapse technology [22](references.md#ref-22).

- FAIR data. Metadata should be findable, accessible, interoperable and reusable [23](references.md#ref-23), in line with the metadata standards agreed under T3.4.

- Pre-specification. Criteria for quality review, exclusion and performance should be agreed before evaluation, not adjusted afterwards.

- Transparency about deviations. Where a site cannot follow the common minimum, the deviation and its reason are recorded.

<span id="section-4-3"></span>

## What to harmonise

[Table 5](harmonisation.md#table-5) sets out the elements that NESTOR partners should harmonise when validating a data-driven method at more than one site. The elements are illustrated for embryo image analysis, but they apply by analogy to genomic and clinical prediction methods.

<span id="table-5"></span>

**Table 5. Minimum harmonised practices for multi-site validation**

| Element | Harmonised minimum | Purpose |
| --- | --- | --- |
| Image acquisition metadata | TLM system and software version; imaging interval; focal planes; image resolution and format; culture conditions; fertilisation method; time reference (e.g. hours post-insemination). | Makes technical and laboratory differences between sites visible and analysable. |
| Annotation and terminology | Written annotation protocol with reference examples; terminology following the Istanbul consensus update; training of annotators; double annotation of a subset. | Ensures that the reference standard means the same at each site; quantifies inter-observer agreement. |
| Data dictionary and identifiers | Common variable names, units and codes; pseudonymous identifiers at embryo, cycle and patient level; linking keys held only at the originating site. | Enables pooling or federated analysis without exposing identities. |
| Dataset partitioning | Splits made at patient or cycle level; at least one site held out entirely for external validation. | Prevents leakage between training and evaluation data; tests generalisation to new sites. |
| Model record | Model version and weights checksum; configuration; input preparation; code version; software environment. | Makes the method version and environment at each site verifiable. |
| Quality review | Common frame-level and embryo-level review criteria; numerical thresholds where possible; coded exclusion reasons; second reviewer for borderline cases. | Makes exclusions comparable and reproducible across sites. |
| Performance measures | Agreed measures for each task (e.g. overlap measures for segmentation; discrimination and calibration for prediction); defined unit of analysis; confidence intervals; subgroup results. | Allows results to be compared and combined. |
| Reporting | TRIPOD+AI [24](references.md#ref-24) or CLAIM [25](references.md#ref-25) for model studies; DECIDE-AI [26](references.md#ref-26) for early clinical evaluation. | Ensures complete and comparable reporting. |
| Legal and ethics documentation | Ethics review outcome and approval where required; lawful basis; DPIA screening and assessment where required; applicable data processing or joint-controllership agreements; processing location. | Demonstrates lawful processing in each jurisdiction. |
| Roles and competence | Named responsible persons for data, analysis and review at each site; training records. | Supports accountability and quality management. |

<span id="section-4-4"></span>

## Organisational models for multi-site evaluation

Three models can be used to evaluate a method across sites:

- Centralised pooling. Data from all sites are transferred to one location. This is the simplest model analytically, but it requires legal agreements in every jurisdiction and exposes the most data to transfer risk.

- Federated, model-to-data evaluation. The model and analysis scripts travel to each site. Evaluation runs within each institution’s approved environment, and only aggregate results, such as performance measures and exclusion counts, leave the site. The Maastricht example illustrates the local model-to-data principle: analysis took place inside the hospital. It does not demonstrate a completed multi-site federated evaluation.

- Hybrid. Core evaluation is federated, and a limited, anonymised or strictly pseudonymised subset is shared centrally for tasks such as joint annotation review.

For cross-border validation in NESTOR, the federated model is recommended as the default. It aligns with the GDPR principle of data minimisation, it reduces the need to transfer patient-level datasets while each site still addresses its legal and governance requirements, and it anticipates the secure processing environments of the EHDS. It does, however, place greater demands on harmonisation. Each site must run the same model version, with the same input preparation and review criteria, and must report results in a common format. The elements in [Table 5](harmonisation.md#table-5) are designed for exactly this purpose. Aggregate outputs should be checked to ensure that small counts cannot identify individuals.

<span id="section-4-5"></span>

## Building harmonisation into the partnership

Harmonisation depends on people as much as on documents. NESTOR secondments give researchers first-hand experience of partner environments, and that experience is the most effective way to align practice. The following measures are recommended to sustain harmonisation beyond individual secondments:

- maintain the harmonised elements in [Table 5](harmonisation.md#table-5) as a shared, version-controlled SOP set, linked from the open-access website;

- hold a short calibration exercise, with joint review of a common image set, before each new multi-site study and after major protocol or equipment changes;

- designate a contact person for data, analysis and review at each participating site;

- use the Advisory Board to review the legal and ethical documentation set and the communication of results to patients;

- record lessons learned from each validation study and feed them back into the guidelines.

*Source: D3.3, Chapter 4. See the [full deliverable](references.md#downloads).*
