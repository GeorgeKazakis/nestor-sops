# Practical workflow

The purpose is to make clear what was evaluated, how it was evaluated and what the evidence supports.

For the current example, the research objective is to study changes in ZP, ICM and TE during embryo development and hatching. Segmentation supports visual assessment and analysis of metrics over time.

| Step | Action | Record to keep |
| --- | --- | --- |
| 1. Define the task | State which structures the method identifies, who will inspect its outputs and what use is being investigated. | A short scope statement, including excluded uses. |
| 2. Describe the data | Identify image sources, annotations and their review status. Explain how training and evaluation sets were separated, including whether related images share an embryo or patient. | Dataset description and saved split records. |
| 3. Identify the model | Record the actual checkpoint, training configuration, preprocessing and output-class order. | Model/version record linked to its original training run. |
| 4. Evaluate and inspect | Compare predictions with appropriate reference annotations and inspect errors. Explain how reported measures were calculated. | Evaluation results and a reviewed error summary. |
| 5. Report limits and next steps | Distinguish measured performance from exploratory visualisations and proposed future clinical use. | Findings, missing evidence and follow-up work. |

## Visual review and exclusion

The team describes the following quality-review procedure used in the embryo image-analysis work:

1. Visually inspect the segmentation results for each run.
2. Exclude frames judged to be incorrectly segmented from the analysis.
3. Where too many frames within an embryo are judged incorrect, exclude that embryo entirely from analysis and metric extraction.

The embryo-level decision was based on visual judgement; no numerical cutoff has been supplied for this description. This records the team's practice, rather than establishing a universal exclusion threshold. Interpretation of the resulting analysis should make clear that it concerns the retained frames and embryos.

## Short procedure: checking a transferred model

This draft procedure is based on the local implementation and the need to trace a model trained on another machine.

1. Match the checkpoint to its original training record; mark missing provenance as pending.
2. Check output labels against the saved class order. In the current example, TE and ICM occupy different channel positions from the local baseline models.
3. Confirm that input preprocessing matches the training setup. Record differences for investigation.
4. Review sample outputs and retain the evaluation report belonging to this checkpoint. Do not substitute another model's results.

The expected output is a traceable model record with discrepancies listed for review. This procedure does not itself demonstrate clinical validity.

## Basis and limits

These steps are a working synthesis of the NESTOR T3.1 activities (proposal, printed page 24) and the repository inspection summarised in the [worked example](embryo-image-analysis.md). They are not a validated cross-domain SOP or a regulatory checklist. Data permissions, scientific acceptance criteria and clinical implementation decisions remain subject to the relevant project and institutional review.
