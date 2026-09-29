# Limitations and next steps

The guidelines in this deliverable are a first, practical synthesis. They draw on one worked example and on a legal landscape that is still changing. This chapter sets out the main limitations of the current work and of data-driven validation in the NESTOR setting more generally, together with the solutions that partners can apply. [Table 8](limitations.md#table-8) groups them into four areas: evidence and methods, data and harmonisation, legal and regulatory constraints, and organisation and sustainability.

<span id="table-8"></span>

**Table 8. Limitations and solutions**

| Limitation | Consequence | Solution |
| --- | --- | --- |
| **Evidence and methods** |  |  |
| The guidelines are illustrated by a single worked example from one research strand (embryo image analysis). | Guidance for genomic, uterine-health and feto-maternal applications is less concrete. | The workflow is written to be domain-neutral. Worked examples for non-invasive genomic methods and feto-maternal applications should be added, building on [NEO-LIFE](references.md#ref-15). |
| The embryo study is at Stage A: segmentation performance was not quantified and embryo-level exclusion relied on qualitative judgement. | The findings cannot support clinical claims, and exclusions may bias the retained dataset. | Establish expert reference annotations, report per-structure performance with confidence intervals, and pre-specify exclusion criteria with a second reviewer ([Table 7](embryo-image-analysis.md#table-7)). |
| Embryo assessment is inherently subjective, and reference annotations vary between embryologists. | Apparent model errors may partly reflect disagreement in the reference standard. | Use a written annotation protocol based on the Istanbul consensus update [21](references.md#ref-21), double-annotate a subset and report inter-observer agreement. AI-assisted annotation can reduce workload but must itself be validated. |
| The guidelines have not yet been tested end to end in a multi-site study. | Practical obstacles may emerge only in use. | Pilot the workflow and checklist on the harmonised TLM data collected at AN, and feed lessons learned back into the web guidelines. |
| **Data and harmonisation** |  |  |
| Data come from a single clinical setting and time-lapse platform. | Generalisability to other clinics, platforms and populations is unknown. | Run site-held-out validation across partner clinics using the harmonised minimum practices ([Table 5](harmonisation.md#table-5)) and federated evaluation ([Section 4.4](harmonisation.md#section-4-4)). |
| Datasets are small and imbalanced, particularly for rare outcomes and subgroups such as patients of advanced reproductive age. | Models may perform worse in exactly the groups NESTOR aims to serve. | Pool evidence across sites, report subgroup performance and consider synthetic data for training [4](references.md#ref-4). Synthetic data can support development but cannot replace validation on real patient data. |
| IT infrastructure and technical capacity differ between partners, especially smaller clinics. | Federated evaluation is harder to run where local capacity is limited. | Use containerised, versioned analysis pipelines, the data-stewardship training and interoperability work of T3.4, and a shared SOP set maintained on the website. |
| **Legal and regulatory** |  |  |
| National implementations of the GDPR, ethics review and ART law differ between the Netherlands, Estonia and Greece. | Cross-border studies face delays and legal uncertainty. | Adopt model-to-data evaluation by default, use a common legal documentation set ([Table 5](harmonisation.md#table-5)) and standard agreement templates, and involve data protection officers and ethics committees early. Draw on the Advisory Board’s privacy-law expertise. |
| The in-house exemption does not allow a tool to be transferred to another legal entity. | Validated tools cannot simply be shared between partner clinics. | Plan the regulatory route early, draw on SME experience with quality management and CE marking, and follow the MDR/IVDR revision [19](references.md#ref-19). |
| The regulatory landscape is moving: the AI Act has been amended, the MDR/IVDR revision is pending, and the SoHO and EHDS rules are being phased in. | Parts of [Chapter 3](regulatory-guidance.md) may date quickly. | Review the regulatory content at least annually and whenever a major instrument changes. |
| **Organisation and sustainability** |  |  |
| Validation know-how is concentrated in the individuals who took part in secondments. | Practice may erode once secondments and the project end. | Keep written SOPs, the open website and training materials up to date, and continue staff exchanges through NEO-LIFE. |
| There is pressure to communicate promising results to clinics and patients early. | Research-stage findings risk being presented as clinical benefit. | State the stage of evidence in every output ([Table 2](clinical-translation.md#table-2)), follow reporting guidelines [24](references.md#ref-24), [25](references.md#ref-25), [26](references.md#ref-26), and involve patient representatives in communication. |

## Next steps

Recommended next steps are to:

- apply the workflow and harmonised minimum practices in multi-site validation of the embryo image-analysis approach, starting with the harmonised TLM data collected at AN;

- extend the worked examples to other NESTOR research sub-fields, notably non-invasive genomic methods, where the IVDR rather than the MDR applies;

- update the guidelines as the MDR/IVDR revision, the AI Act implementation and the SoHO and EHDS frameworks develop;

- use NESTOR dissemination channels, including ESHRE and national professional networks, to share the guidelines with ART providers in Estonia, Greece and beyond;

- carry the workflow, checklist and data-sharing standards forward into the follow-on project [NEO-LIFE](references.md#ref-15).

*Source: D3.3, Chapters 8 and 9. See the [full deliverable](references.md#downloads).*
