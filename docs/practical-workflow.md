# Practical workflow

Evaluation of a data-driven method involves a defined research question, a documented dataset and an identifiable model. The workflow below organises these elements into five stages, from the definition of the task to the interpretation of findings. Each stage describes its purpose, the information involved and its contribution to the overall analysis.

The workflow provides a general framework for organising method evaluation. The data, performance measures and criteria for an acceptable result depend on the task being studied. A worked application is presented in the [embryo image-analysis example](embryo-image-analysis.md), using the same five stages.

## Organising the evaluation

| Step | Description | Documentation |
| --- | --- | --- |
| [1. Task definition](#1-task-definition) | Definition of the research question, intended use and expected outputs. | Scope of the analysis and responsibilities for review. |
| [2. Data description](#2-data-description) | Description of data sources, reference information and the separation of training and evaluation data. | Dataset description, preparation methods and selection records. |
| [3. Model identification](#3-model-identification) | Identification of the model version, configuration and meaning of its outputs. | Model record and analysis settings. |
| [4. Evaluation and visual review](#4-evaluation-and-visual-review) | Assessment of performance and review of outputs before further analysis. | Evaluation results, review decisions and exclusion records. |
| [5. Documentation and interpretation](#5-documentation-and-interpretation) | Presentation of findings in relation to the research question and the limits of the analysis. | Results, supporting observations and further evaluation needs. |

## 1. Task definition

The research question establishes what the method is intended to identify, measure or predict. Its intended use provides the context for interpreting the outputs: the same measurement may have different requirements when used for exploratory research or to support a particular decision.

The scope describes the population or material being studied, the features of interest and the expected outputs. It also identifies responsibilities for reviewing those outputs and the role of human assessment within the analysis. This makes the relationship between automated processing and expert judgement clear from the outset.

Criteria for an acceptable result follow from this scope. They describe the level of accuracy, completeness or consistency needed for the task and the types of error that would make an output unsuitable. A documented scope gives data selection, model evaluation and interpretation a common basis.

## 2. Data description

The dataset description covers the source of the data, how they were collected, the material included and any preparation applied before analysis. Relevant preparation may include image resizing, intensity normalisation or the handling of missing observations. These details help explain the conditions under which the method is evaluated.

When an analysis involves patient data, restrictions on data transfer may require the work to be performed within the hospital's approved computing environment. The arrangements for data access and processing therefore form part of the analysis setup.

Where evaluation involves comparison with reference information, its origin and review process form part of the description. For image analysis, this may include annotations identifying the structures of interest. Uncertainty or inconsistency in the reference information affects the interpretation of differences between the model and the reference.

The separation of training and evaluation data accounts for related observations from the same source, such as repeated measurements from one participant or images from one sequence. Their allocation to each set affects how independently the method is being evaluated.

Dataset documentation also describes the criteria for inclusion and exclusion. Links between the original observations, processed inputs and retained results make it possible to understand how the analysed dataset was formed. This is particularly relevant when quality review removes part of the original data.

## 3. Model identification

Model identification covers the version used for analysis, its associated configuration and the preparation of its inputs. The model and its settings together define the method being evaluated; a change in either may alter the resulting outputs.

The description of the outputs explains what each label, value or region represents. In an image-segmentation method, for example, the association between output labels and anatomical structures determines how overlays and subsequent measurements are interpreted. Units and any processing applied after prediction are also relevant to understanding the results.

A model record connects the input preparation, model version and analysis settings with the resulting evaluation. This supports reproducibility and allows comparisons between analyses to account for changes in the method, rather than attributing every difference to the data.

## 4. Evaluation and visual review

Evaluation examines how well the outputs address the task defined in step 1. Where suitable reference information is available, comparison with that reference provides a basis for calculating performance measures. The calculation and level of analysis are part of the evaluation description, since a result calculated per image may answer a different question from one calculated per sequence or participant.

Visual review complements quantitative measures in image-based applications. It reveals the nature and distribution of errors, including incomplete outputs or incorrect identification of structures that may be obscured by an overall performance value. Review of individual results also helps determine whether they can support subsequent measurements.

Quality review addresses three related aspects:

1. The characteristics that distinguish usable outputs from incomplete or incorrect results.
2. The level at which a decision applies, such as an individual observation or a complete sequence.
3. The basis for retaining, reprocessing or excluding the affected data.

The review criteria and reasons for exclusion explain how the final analysis set differs from the original dataset. Numerical thresholds and qualitative judgements represent different bases for these decisions and are described accordingly. Evaluation of the original outputs and analysis of the retained data answer different questions; the latter describes the subset that passed review.

Performance measures describe the quality of the method's outputs. Measurements subsequently derived from those outputs address the research question. Keeping these two types of result distinct clarifies what the evaluation establishes and how output quality affects the findings.

## 5. Documentation and interpretation

Documentation brings together the research question, dataset, model configuration, evaluation results and review decisions. Their connection allows a finding to be traced to the data and processing steps from which it was derived.

Quantitative results and qualitative observations provide different forms of evidence. Their presentation identifies how each was obtained, the observations to which it applies and any exclusions affecting its interpretation. This makes the basis of each finding clear without treating a visual judgement as an automatically calculated measurement.

Interpretation relates the findings to the task defined in step 1. It considers the coverage of the dataset, the quality of the reference information, the errors observed and the effect of data selection. These factors explain the conditions under which the findings are supported and the questions that remain open.

The resulting account describes both the contribution of the method and any further evaluation needed for its intended use. The [embryo image-analysis example](embryo-image-analysis.md) shows how the five stages relate to a specific NESTOR research application.
