# Embryo image-analysis example

This example presents the NESTOR study of embryo development and hatching through the five stages of the [practical workflow](practical-workflow.md). It brings together the research objective, the image-analysis approach and the visual review procedure used to select segmentation outputs for measurement.

The embryo-analysis work was carried out through a collaboration between members of INF and UM at the hospital in Maastricht.

## 1. Task definition

The research objective was to study changes in the zona pellucida (ZP), inner cell mass (ICM) and trophectoderm (TE) during embryo development and hatching. Automated segmentation identified these structures in time-lapse images, supporting the assessment of size, shape, ZP thickness and image intensity over time.

Visual observations and quantitative measurements were used together to examine developmental changes. Hatching was identified visually, providing an observation separate from the measurements extracted by the analysis pipeline.

## 2. Data description

The analysis used time-lapse image sequences of embryo development and hatching. Each sequence contained successive frames associated with an embryo, allowing changes in the identified structures to be followed over time.

Images, segmentation overlays and videos provided the material for visual assessment. Review determined which frames, and in some cases which entire embryo sequences, were retained for analysis and metric extraction.

The measurements were organised by embryo and frame. This preserved the relationship between each quantitative record and its position within the corresponding image sequence.

## 3. Model identification

The analysis pipeline used a segmentation model to identify ZP, ICM and TE in individual time-lapse frames. Its outputs represented the three anatomical structures and supported visualisation of their boundaries and extraction of quantitative measurements.

Segmentation overlays and videos allowed the predicted structures to be inspected in relation to the source images. The outputs also supported the assessment of image intensity and structural changes during development.

The model's role in this application was to identify the structures used for analysis. Visual review determined whether the resulting segmentation was suitable for measurement.

## 4. Evaluation and visual review

The quality-review procedure used in this application was based on visual inspection of the segmentation results for each run. It was comprised of three stages:

1. Visual inspection of the predicted ZP, ICM and TE structures.
2. Exclusion of frames with incomplete or incorrect segmentation from analysis.
3. Exclusion of an embryo from analysis and metric extraction when too many of its frames were incorrectly segmented.

The embryo-level decision relied on qualitative visual judgement, without a fixed numerical cutoff. The resulting measurements therefore describe the frames and embryos retained after this review.

Images, overlays and videos were examined alongside quantitative measurements to assess changes over time. This describes the visual quality review applied in the study; numerical segmentation-performance results are not presented in this example.

## 5. Documentation and interpretation

Quantitative measurements were stored in one CSV file per embryo, with one row per time-lapse frame. This organisation supported assessment of changes in size, shape, ZP thickness and image intensity across each sequence.

Hatching was assessed visually and was not recorded in the measurement CSV files. The visual observations and the quantities extracted by the pipeline therefore provide distinct sources of information about development and hatching.

Interpretation concerns the retained frames and embryos because incomplete or incorrect segmentation led to exclusions. The procedure illustrates how automated segmentation, visual review and quantitative assessment were combined in a research application. Its suitability for embryo selection or treatment decisions has not been established by this workflow alone.
