# Validation framework

!!! warning "Draft guidance — project review pending"
    The first two sections contain proposed planning guidance. Later stages remain outlines. No study-specific procedures, acceptance criteria or clinical-readiness conclusions are established here.

This framework connects a proposed innovation to a documented validation plan across the five NESTOR domains. Start with the problem and proposed use, then carry those decisions into the [validation protocol template](../templates/validation-protocol-template.md).

The prompts and illustrative example below are editorial proposals for this repository. Sources support the stated methodological principles; they do not constitute NESTOR approval. NICE guidance concerns digital health technologies in a UK context, and the cited IMDRF document concerns software as a medical device. Applying these ideas beyond those contexts requires domain review, not automatic adoption as EU requirements.

## Topic selection and clinical problem

### Purpose

Describe the need before choosing how to evaluate the innovation. NICE's evidence framework asks developers to describe the existing care process, its population and the changes a digital technology would introduce. This helps locate an innovation within actual practice. See [NICE, standards 10–13](https://www.nice.org.uk/corporate/ecd7/chapter/how-to-meet-the-standards).

### Questions to answer

- What problem is being investigated, and who experiences it?
- What happens today, and where is the proposed gap?
- Which observations or publications support that gap?
- What benefit is hypothesised, and what remains unknown?

### Activities

Prepare a short problem brief and a simple description of the current workflow. Cite the evidence behind the problem statement and identify assumptions separately. Discuss the description with relevant users and record unresolved disagreements.

For NESTOR topic selection, also record the relevant research domain, responsible contributors and why the topic is suitable for a translation-oriented case study. These are proposed project-planning fields, not a validated topic-selection score.

### Expected output

Complete [protocol section 2](../templates/validation-protocol-template.md#2-clinical-problem-and-rationale) with the problem brief, supporting references and rationale for selecting the topic. A useful drafting pattern is:

> In [setting], [population or users] encounter [problem] during [activity]. Current practice is [approach]. Evidence from [sources] indicates [gap]. We propose to investigate whether [innovation] can address [specific aspect]; [uncertainties] remain unresolved.

### Common pitfalls to check

As an editorial review check based on NICE's pathway-and-benefit framing, look for descriptions that name only a technology, omit current practice, or present an expected benefit as an established result. Rewrite these as a problem, a proposed change and a question to investigate. See [NICE, standards 11–13](https://www.nice.org.uk/corporate/ecd7/chapter/how-to-meet-the-standards).

## Intended use

### Purpose

Define the particular use for which evidence will be sought. For medical-device software, IMDRF separates evidence connecting an output to a clinical condition, evidence that the software processes inputs correctly, and evidence that its output achieves the intended purpose in the target population and care context. Technical performance alone does not answer all three questions. See [IMDRF N41, sections 5–7](https://www.imdrf.org/sites/default/files/docs/imdrf/final/technical/imdrf-tech-170921-samd-n41-clinical-evaluation_1.pdf).

### Questions to answer

- Who will use the method, for which population and in which setting?
- What inputs does it require, and what output does it produce?
- What activity or decision would that output support?
- What role does the user retain, and which uses are outside scope?

### Activities

Draft one bounded use statement. Identify the method version and distinguish the proposed future clinical role from the use actually being investigated in the current study. Keep changes to that statement visible in the protocol history.

The following fields are a proposed NESTOR writing aid, not a regulatory declaration:

| Field | What to record |
| --- | --- |
| Method | Name and version being investigated |
| Users | Roles and relevant expertise |
| Population and setting | Who the proposed use concerns and where it occurs |
| Inputs and outputs | What enters the method and what it returns |
| Workflow role | How the output is proposed to be used |
| Boundaries | Excluded uses and unresolved assumptions |
| Current evidence scope | What this study can address, separately from future claims |

### Expected output

Complete [protocol section 3](../templates/validation-protocol-template.md#3-intended-use-population-and-setting). Use the same statement when developing study objectives, data requirements and the evaluation plan; flag any mismatch for review.

### Common pitfalls to check

For software studies, do not turn a technically accurate output into a clinical-benefit claim without the corresponding evidence. Likewise, do not silently extend a finding to a different population or care setting. These checks follow IMDRF's distinction between technical and clinical validation and its emphasis on intended purpose and context. See [IMDRF N41, sections 5–7](https://www.imdrf.org/sites/default/files/docs/imdrf/final/technical/imdrf-tech-170921-samd-n41-clinical-evaluation_1.pdf).

### Illustrative example linking the two sections

!!! example "Hypothetical planning example — not a NESTOR result"
    **Candidate problem:** A team proposes to investigate whether manual annotation of embryo time-lapse images is inconsistent. The extent and importance of that possible problem still need evidence.

    **Proposed study use:** A named version of an image-analysis method would produce candidate boundaries on a defined retrospective image set for review by research annotators. This example does not propose using its output for embryo selection or treatment decisions.

    **Open questions:** Which images, structures, reference annotations and assessments are appropriate? Those choices remain to be justified in later protocol sections. No clinical benefit is asserted.

Before proceeding, record unresolved questions and responsible contributors in the protocol's open-items table. Completing these sections establishes a planning baseline, not permission to collect data or deploy a method.

## Data requirements and collection

TODO: Develop the outline for sample and patient-data collection, provenance, quality and relevant supporting data-management requirements.

## Validation study design

TODO: Develop guidance for experimental/clinical validation design, questions, comparators and analysis planning. No study size or design is prescribed here.

## Computational validation

TODO: Define how computational analyses and method versions should be documented, with domain-specific evaluation procedures to follow review.

## Performance assessment

TODO: Develop the approach to selecting and reporting appropriate precision/performance measures, uncertainty and acceptance criteria. No thresholds are specified.

## Reproducibility and robustness

TODO: Identify documentation and assessment needs for reproducibility, robustness and limitations across relevant conditions.

## Clinical interpretation

TODO: Develop guidance for interpreting validation findings in relation to intended use and remaining evidence gaps.

## Ethics and data protection

TODO: Identify applicable ethical review and data-protection considerations with appropriate project expertise and verified sources.

## Problems, possible solutions and implementation

TODO: Develop an approach to documenting observed problems, proposed solutions, implementation considerations and unresolved translation barriers.

## Reporting and publication

TODO: Agree reporting content, review responsibilities and publication routes, linked to the planned [templates](../templates/index.md) and [references](../references.md).
