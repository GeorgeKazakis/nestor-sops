# Embryo image-analysis example

## Research objective

The objective is to study changes in the zona pellucida (ZP), inner cell mass (ICM) and trophectoderm (TE) during embryo development and hatching using time-lapse images.

Segmentation identifies these structures in individual frames, supporting the assessment of changes in size, shape, ZP thickness and image intensity over time.

## How changes were assessed

The team used a segmentation model trained on a separate computing workstation. Changes were assessed through visual inspection of images, overlays and videos, together with quantitative metrics saved in CSV files. Each CSV represents one embryo, with one row per time-lapse frame.

Hatching was established visually and was not recorded in the measurement CSVs.

This report summarises the research approach and available implementation. It does not present quantitative findings from the CSVs.

## Relationship to the practical workflow
 
### Quality review used in this work

The team visually reviewed segmentation results for each run. Frames that appeared incorrectly segmented were excluded from analysis. If too many frames within an embryo appeared incorrect, the whole embryo was excluded from analysis and metric extraction.

This was a qualitative review decision; no numerical exclusion cutoff has been specified here. The resulting analysis describes the retained frames and embryos.

### Applying the workflow

The example illustrates the sequence described in the [practical workflow](practical-workflow.md): define the research question, prepare the images, apply the model, inspect the outputs and document observations and limitations.

The research implementation remains in the separate `embryo-vision` repository. This guidelines site explains the approach without reproducing the software, private images or detailed measurement records.

## Current scope

This is an example of research into changes during embryo development and hatching. It does not establish suitability for embryo selection or treatment decisions. Model performance and any proposed clinical application require their own supporting evaluation.

## Evidence and project connection
 
### Conclusions

The activity combined segmentation, visual assessment and frame-level quantitative records to investigate embryo development and hatching. Visual quality review determined which frames and embryos were retained for analysis. The practical contribution of this report is the description of that workflow and its exclusion procedure, providing a basis for further documentation and evaluation rather than a claim of clinical validation.

### Sources

This overview draws on the project contributor's description and inspection of the `embryo-vision` documentation and analysis tools. A permanent implementation reference can be added for a reviewed release.

The NESTOR proposal connects time-lapse image-recognition development to ST2.2.3 (printed page 22, PDF page 93), and validation guidance to T3.1 (printed page 24, PDF page 95). This example documents a contribution to that work, not completion of every planned outcome.
