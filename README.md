# StrokeReportGen: Medical Report Generation for Ischemic Stroke and Brain CT

This repository contains the code and resources for our work on automated medical report generation from brain imaging data, focusing on ischemic stroke (MRI-DWI) and general brain CT scans.

We evaluate our method on two large-scale public datasets: **StrokeQD** and **CTRG-Brain**, both curated with expert annotations and following standard clinical preprocessing pipelines.

---

## 📊 Datasets

### 1. StrokeQD Dataset (Ischemic Stroke MRI/CT Report Generation)

The **StrokeQD** dataset is a large-scale collection of diffusion-weighted imaging (DWI) MRI scans paired with diagnostic reports for ischemic stroke patients.

- **Total Images**: 22,626 MRI-DWI images
- **Patients**: 1,181 anonymized cases
- **Modalities**: Single modality (DWI)
- **Split Ratio**: Train : Val : Test = 7 : 2 : 1
- **Source**: Curated by a medical consortium; publicly available via [GitHub](https://github.com/qustvr501/StrokeQD)

> *Note: The dataset will be made publicly available soon if not already accessible.*

#### 🔍 Data Visualization Example

![StrokeQD Sample](imgs/strokeqd_sample.png)  
*Fig. 1. Example DWI slice with lesion annotation (red mask) from the StrokeQD dataset.*

*(You should replace `imgs/strokeqd_sample.png` with an actual image path in your repo — see below for how to add it.)*

---

### 2. CTRG-Brain Dataset (General Brain CT Report Generation)

The **CTRG-Brain** dataset consists of Chinese-language medical reports aligned with 3D brain CT volumes.

- **Total Reports**: 6,000
- **Total Images**: 160,336 CT slices
- **Modalities**: Single modality (CT), but processed as multi-slice sequences
- **Preprocessing**: Each volume split into 8 groups × 3 consecutive slices → 24-slice input per sample
- **Split Ratio**: Train : Val : Test = 7 : 1 : 2
- **Source**: Publicly available via [GitHub](https://github.com/tangyuhao2016/CTRG)

#### 🔍 Data Visualization Example

![CTRG-Brain Sample](imgs/ctrg_brain_sample.png)  
*Fig. 2. Multi-slice CT visualization from CTRG-Brain dataset showing axial views with anatomical landmarks.*

*(Replace `imgs/ctrg_brain_sample.png` with your own visual example.)*

---

## 🛠️ Preprocessing & Input Format

To ensure compatibility with deep learning models:

- For **StrokeQD**: Raw DWI images are normalized and resized to 256×256.
- For **CTRG-Brain**: Following prior work \citep{b25}, each 3D CT volume is partitioned into 8 overlapping triplets of consecutive slices, yielding standardized 24-slice inputs per training sample.

---

##  Citations

If you use these datasets or this codebase, please cite:

```bibtex
@article{ref21,
  title={StrokeQD: A Large-Scale Dataset for Ischemic Stroke Report Generation},
  author={Author et al.},
  journal={Journal Name},
  year={202X}
}

@inproceedings{tang2024work,
  title={CTRG-Brain: Towards Automated Chinese Brain CT Report Generation},
  author={Tang, Yuhao and others},
  booktitle={Conference Name},
  year={2024}
}
