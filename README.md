# Balancing Privacy and Performance: The Impact of Facial Defacing on AI in Medical Imaging

<img src="Pics/Overall_pipeline.png" align="middle" width="75%">

The 2025 NIH Data Management and Sharing policy mandates facial anonymization for publicly shared medical imaging data, prompting concerns about potential degradation of AI model performance. We systematically evaluated three representative defacing algorithms, two invasive (QuickShear, Deface) and one geometry-preserving, non-invasive method (Reface), across MRI and CT datasets from 600 subjects. Model performance was assessed across complementary clinical tasks: (1) brain segmentation and Evans ratio measurement in MRI of normal pressure hydrocephalus (NPH), (2) representative slice selection and diagnostic reasoning for brain tumor MRI using vision–language models (VLMs), and (3) automated report generation from emergency department CT head scans via VLMs. Invasive defacing substantially impaired segmentation accuracy, diagnostic precision, and report fidelity, whereas the non-invasive Reface approach preserved model performance with minimal deviation from original data. These findings quantify the privacy–utility trade-off introduced by facial defacing and underscore the importance of non-invasive, geometry-preserving anonymization techniques to ensure both patient privacy and AI model reproducibility under the emerging NIH data-sharing mandate.

## Datasets Description
This retrospective study was approved by the Institutional Review Boards of Johns Hopkins University (IRB00318113 for the NPH MRI dataset, IRB00452757 for the Brain Tumor MRI dataset, and IRB00424745 for the ED head CT dataset) with a waiver of informed consent. A data transfer agreement with the University of Pennsylvania (identification number: 73481-00) was also established for the Brain Tumor MRI dataset.


### Data Structure

| Type                      | No. (ALL)   | No. (Include) | Format |
| --------------------------| ------------| ------------- | -------|
| NPH MRI Dataset           | 534         | 200           | DICOM  |
| Brain Tumor MRI Dataset   | 2453        | 200           | NiFTI  |
| ED CT Head Dataset        | 33,128      | 200           | DICOM  |

## Dafec methods and implementation details

### Quickshear
- **GitHub:** https://github.com/nipy/quickshear
- **Latest release:** **v1.1.0** (May 23, 2017) :contentReference[oaicite:0]{index=0}

### Deface (Deep Learning)
- **GitHub:** https://github.com/yeonuk-Jeong/Defacer
- **Repo versions:** **ver.0.1**, **ver.0.2** (no formal GitHub “Releases”; latest code under `ver.0.2/`) :contentReference[oaicite:1]{index=1}

### Reface (mri_reface)
- **Home (no official GitHub):** https://www.nitrc.org/projects/mri_reface
- **Notable releases:** **v0.3** (Jul 15, 2022), **v0.3.2** (May 2, 2023), **v0.3.5** (Mar 25, 2025). Earlier **v0.2** also widely referenced in studies. :contentReference[oaicite:2]{index=2}
