# Practical workflow

Evaluation of a data-driven method involves a defined research question, a documented dataset and an identifiable model. The workflow below organises these elements into five stages, from the definition of the task to the interpretation of findings. Each stage describes its purpose, the information involved and its contribution to the overall analysis. For each stage, a short note sets out the additional considerations that apply when the work spans several sites or moves towards clinical use.

The workflow provides a general framework for organising method evaluation. The data, performance measures and criteria for an acceptable result depend on the task being studied. A worked application is presented in the embryo image-analysis example ([Chapter 6](embryo-image-analysis.md)), using the same five stages.

<span id="table-6"></span>

**Table 6. Organising the evaluation**

| Step | Description | Documentation | Key checkpoints |
| --- | --- | --- | --- |
| [1. Task definition](practical-workflow.md#section-5-1) | Definition of the research question, intended use and expected outputs. | Scope of the analysis and responsibilities for review. | Intended purpose; regulatory qualification; ethics and DPIA screening. |
| [2. Data description](practical-workflow.md#section-5-2) | Description of data sources, reference information and the separation of training and evaluation data. | Dataset description, preparation methods and selection records. | Lawful basis per site; agreements; processing location; representativeness; harmonised metadata. |
| [3. Model identification](practical-workflow.md#section-5-3) | Identification of the model version, configuration and meaning of its outputs. | Model record and analysis settings. | Version control; same model at every site; IP and licensing. |
| [4. Evaluation and visual review](practical-workflow.md#section-5-4) | Assessment of performance and review of outputs before further analysis. | Evaluation results, review decisions and exclusion records. | Pre-specified criteria; reference standard; human oversight; risk register. |
| [5. Documentation and interpretation](practical-workflow.md#section-5-5) | Presentation of findings in relation to the research question and the limits of the analysis. | Results, supporting observations and further evaluation needs. | Reporting guidelines; stage of evidence; responsible claims. |

<span id="section-5-1"></span>

## 1. Task definition

[Checklist items](validation-checklist.md#1-task-definition) · [Regulatory checkpoints](regulatory-guidance.md#table-4) · [Worked example](embryo-image-analysis.md#section-6-1)

The research question establishes what the method is intended to identify, measure or predict. Its intended use provides the context for interpreting the outputs: the same measurement may have different requirements when used for exploratory research or to support a particular decision.

The scope describes the population or material being studied, the features of interest and the expected outputs. It also identifies responsibilities for reviewing those outputs and the role of human assessment within the analysis. This makes the relationship between automated processing and expert judgement clear from the outset.

Criteria for an acceptable result follow from this scope. They describe the level of accuracy, completeness or consistency needed for the task and the types of error that would make an output unsuitable. A documented scope gives data selection, model evaluation and interpretation a common basis.

Cross-site and regulatory considerations. The intended use should be written as an explicit intended-purpose statement, naming the clinical question, the intended user and the target population. That statement determines whether the method would qualify as a medical device or IVD ([Section 3.2](regulatory-guidance.md#section-3-2)) and which device study requirements or AI Act research exclusions apply to the specific activity. In multi-site work, all sites should agree the same task definition and acceptance criteria before data are prepared. Clinicians and, where appropriate, patient representatives should be involved in defining which errors are unacceptable.

<span id="section-5-2"></span>

## 2. Data description

[Checklist items](validation-checklist.md#2-data-description) · [Regulatory checkpoints](regulatory-guidance.md#table-4) · [Worked example](embryo-image-analysis.md#section-6-2)

The dataset description covers the source of the data, how they were collected, the material included and any preparation applied before analysis. Relevant preparation may include image resizing, intensity normalisation or the handling of missing observations. These details help explain the conditions under which the method is evaluated.

When an analysis involves patient data, restrictions on data transfer may require the work to be performed within the hospital’s approved computing environment. The arrangements for data access and processing therefore form part of the analysis setup.

Where evaluation involves comparison with reference information, its origin and review process form part of the description. For image analysis, this may include annotations identifying the structures of interest. Uncertainty or inconsistency in the reference information affects the interpretation of differences between the model and the reference.

The separation of training and evaluation data accounts for related observations from the same source, such as repeated measurements from one participant or images from one sequence. Their allocation to each set affects how independently the method is being evaluated.

Dataset documentation also describes the criteria for inclusion and exclusion. Links between the original observations, processed inputs and retained results make it possible to understand how the analysed dataset was formed. This is particularly relevant when quality review removes part of the original data.

Cross-site and regulatory considerations. For each contributing site, record the lawful basis for processing, the consent or opt-out status, the ethics approval and the agreements in place between partners ([Section 3.1](regulatory-guidance.md#section-3-1)). Describe each site’s data using the harmonised metadata in [Table 5](harmonisation.md#table-5), so that differences in equipment, laboratory practice and population can be taken into account. Where possible, hold out at least one site entirely for external validation. Describe the population represented and any known gaps, such as under-representation of particular age groups.

<span id="section-5-3"></span>

## 3. Model identification

[Checklist items](validation-checklist.md#3-model-identification) · [Regulatory checkpoints](regulatory-guidance.md#table-4) · [Worked example](embryo-image-analysis.md#section-6-3)

Model identification covers the version used for analysis, its associated configuration and the preparation of its inputs. The model and its settings together define the method being evaluated; a change in either may alter the resulting outputs.

The description of the outputs explains what each label, value or region represents. In an image-segmentation method, for example, the association between output labels and anatomical structures determines how overlays and subsequent measurements are interpreted. Units and any processing applied after prediction are also relevant to understanding the results.

A model record connects the input preparation, model version and analysis settings with the resulting evaluation. This supports reproducibility and allows comparisons between analyses to account for changes in the method, rather than attributing every difference to the data.

Cross-site and regulatory considerations. In federated evaluation, every site must run exactly the same model. A checksum of the model weights and a record of the software environment make this verifiable. Version control and change records at this stage are the foundation of the software life-cycle documentation that would later be required for an applicable medical-device software life cycle and regulatory route; see [quality and technical standards](regulatory-guidance.md#section-3-2). The ownership and licensing of the model and of any training data should also be recorded, in line with the NESTOR intellectual property management plan.

<span id="section-5-4"></span>

## 4. Evaluation and visual review

[Checklist items](validation-checklist.md#4-evaluation-and-visual-review) · [Regulatory checkpoints](regulatory-guidance.md#table-4) · [Worked example](embryo-image-analysis.md#section-6-4)

Evaluation examines how well the outputs address the task defined in Step 1. Where suitable reference information is available, comparison with that reference provides a basis for calculating performance measures. The calculation and level of analysis are part of the evaluation description, since a result calculated per image may answer a different question from one calculated per sequence or participant.

Visual review complements quantitative measures in image-based applications. It reveals the nature and distribution of errors, including incomplete outputs or incorrect identification of structures that may be obscured by an overall performance value. Review of individual results also helps determine whether they can support subsequent measurements.

Quality review addresses three related aspects:

1. The characteristics that distinguish usable outputs from incomplete or incorrect results.

2. The level at which a decision applies, such as an individual observation or a complete sequence.

3. The basis for retaining, reprocessing or excluding the affected data.

The review criteria and reasons for exclusion explain how the final analysis set differs from the original dataset. Numerical thresholds and qualitative judgements represent different bases for these decisions and are described accordingly. Evaluation of the original outputs and analysis of the retained data answer different questions; the latter describes the subset that passed review.

Performance measures describe the quality of the method’s outputs. Measurements subsequently derived from those outputs address the research question. Keeping these two types of result distinct clarifies what the evaluation establishes and how output quality affects the findings.

Cross-site and regulatory considerations. Review criteria and exclusion rules should be agreed before evaluation and applied identically at each site, using coded exclusion reasons so that exclusion rates can be compared. Report performance per site as well as overall, with confidence intervals. When a method moves towards clinical use, visual review becomes part of the human oversight design. The documentation should state who reviews outputs, what they can override, and how disagreements are resolved. Failure modes identified during review should be recorded in a risk register.

<span id="section-5-5"></span>

## 5. Documentation and interpretation

[Checklist items](validation-checklist.md#5-documentation-and-interpretation) · [Regulatory checkpoints](regulatory-guidance.md#table-4) · [Worked example](embryo-image-analysis.md#section-6-5)

Documentation brings together the research question, dataset, model configuration, evaluation results and review decisions. Their connection allows a finding to be traced to the data and processing steps from which it was derived.

Quantitative results and qualitative observations provide different forms of evidence. Their presentation identifies how each was obtained, the observations to which it applies and any exclusions affecting its interpretation. This makes the basis of each finding clear without treating a visual judgement as an automatically calculated measurement.

Interpretation relates the findings to the task defined in Step 1. It considers the coverage of the dataset, the quality of the reference information, the errors observed and the effect of data selection. These factors explain the conditions under which the findings are supported and the questions that remain open.

The resulting account describes both the contribution of the method and any further evaluation needed for its intended use. The embryo image-analysis example shows how the five stages relate to a specific NESTOR research application.

Cross-site and regulatory considerations. Report studies according to recognised guidelines: TRIPOD+AI for prediction models [24](references.md#ref-24), CLAIM for AI in medical imaging [25](references.md#ref-25) and DECIDE-AI for early clinical evaluation of AI decision support [26](references.md#ref-26). State explicitly which stage of evidence has been reached ([Table 2](clinical-translation.md#table-2)). Findings from Stage A or B should not be presented as evidence of clinical benefit, whether in publications, communication materials or discussions with patients. Records should be archived according to the NESTOR data management plan so that they can support later studies or regulatory submissions.

*Source: D3.3, Chapter 5. See the [full deliverable](references.md#downloads).*
