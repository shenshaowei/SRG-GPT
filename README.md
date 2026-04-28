# Stroke Report Generation

This repository contains the implementation for medical report generation on ischemic stroke MRI and brain CT datasets.

##  Datasets

We conduct experiments on two public datasets:

### 1. StrokeQD Dataset
*   **Task**: Ischemic stroke MRI/CT report generation
*   **Data**: 22,626 MRI-DWI images from 1,181 anonymized patients
*   **Split**: Train : Val : Test = 7 : 2 : 1
*   **Link**: [https://github.com/qustvr501/StrokeQD](https://github.com/qustvr501/StrokeQD)

### 2. CTRG-Brain Dataset
*   **Task**: Brain CT report generation
*   **Data**: 160,336 CT slices paired with 6,000 Chinese medical reports
*   **Preprocessing**: Each CT sequence is partitioned into 8 groups of 3 consecutive slices (24 slices per sample)
*   **Split**: Train : Val : Test = 7 : 1 : 2
*   **Link**: [https://github.com/tangyuhao2016/CTRG](https://github.com/tangyuhao2016/CTRG)
