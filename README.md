<div align="center">

<br>

# Mayishat Altab Mridu

### Computer Science Graduate · Computational Research

*Building intelligent systems and exploring data-driven approaches to complex problems.*

<br>

[![Focus](https://img.shields.io/badge/Focus-Computational%20Research-5B3828?style=flat-square&labelColor=21140F)](#-research-interests)
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Deep%20Learning-B77943?style=flat-square&labelColor=21140F)](#-technical-toolkit)
[![Goal](https://img.shields.io/badge/Goal-PhD%20Research-CB9A62?style=flat-square&labelColor=21140F)](#-academic-goals)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0006--5069--3097-A6CE39?style=flat-square&logo=orcid&logoColor=white&labelColor=21140F)](https://orcid.org/0009-0006-5069-3097)

<br>

**RESEARCH · COMPUTE · INVESTIGATE · DISCOVER**

<br>

[About](#-about-me) · [Research](#-research-interests) · [Projects](#-featured-research--projects) · [Toolkit](#-technical-toolkit) · [Practices](#-research-practices) · [Goals](#-academic-goals) · [Contact](#-contact)

</div>

---

## 👋 About Me

I am a Computer Science and Engineering graduate from **Daffodil International University, Bangladesh**, with interests in machine learning, deep learning and computational research.

My work applies computational methods to problems in **healthcare**, **genomics** and **environmental sound analysis**. I care most about building reproducible machine-learning workflows, evaluating models carefully, and interpreting results within the limits of the available evidence.

This portfolio documents my technical work and research development as I prepare for **PhD research opportunities**.

| | |
|---|---|
| 🎓 **Background** | Computer Science and Engineering |
| 🧠 **Core interests** | Machine learning, deep learning and data-driven modeling |
| 🧬 **Computational genomics** | Evidence integration and candidate-gene prioritization |
| 🩺 **Healthcare AI** | Retinal fundus image analysis and glaucoma detection |
| 🔊 **Audio intelligence** | Urban environmental sound classification |
| 🔬 **Research approach** | Careful evaluation, reproducibility and evidence-based interpretation |

---

## 🔭 Research Interests

<table>
<tr>
<td width="50%" valign="top">

### 🧬 Computational Genomics

Integrating genetic-association, transcriptomic, tissue-expression, interaction-network and pathway evidence to prioritize candidate genes, and testing what really drives the ranking.

</td>
<td width="50%" valign="top">

### 🩺 Medical AI

Applying deep learning and computer vision to retinal fundus images, with attention to evaluation, explainability and practical screening use.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🔊 Machine Learning for Audio

Investigating audio feature extraction and supervised learning for classifying urban environmental sounds.

</td>
<td width="50%" valign="top">

### 🔍 Reliable Machine Learning

Evaluation design, leakage prevention, model comparison, interpretability and an honest account of the limits of computational predictions.

</td>
</tr>
</table>

---

## 📂 Featured Research & Projects

### 01 · 🧬 Multi-Evidence Gene Prioritization for Type 2 Diabetes

**Computational Genomics · Machine Learning · Evidence Integration**

An exploratory study testing whether heterogeneous gene-level evidence can prioritize genes linked to a defined human pancreatic β-cell type 2 diabetes (T2D) differential-expression phenotype. It also measures how much of the ranking signal reflects gene expression level and detectability rather than genetic or network evidence.

> 📄 *Manuscript:* "An Exploratory Machine-Learning Ranking of Type 2 Diabetes-Associated Pancreatic β-Cell Genes Using Heterogeneous Gene-Level Evidence"

<details open>
<summary><b>Research components</b></summary>

<br>

- Integrated genetic-association, islet regulatory, transcriptomic, tissue-expression, protein–protein interaction and pathway evidence.
- Built an analytical dataset of **3,868 genes**: 51 positive genes, 1,991 strict controls and 1,826 unlabeled genes, with HGNC and Ensembl GRCh38 identifiers.
- Used a fixed set of **14 predictors** and excluded every measurement from GSE221156, the dataset that defines the labels.
- Evaluated an **L2-regularized logistic regression (C = 0.1, fixed in advance)** with grouped five-fold cross-validation, ten repeated splits, bootstrap confidence intervals, permutation tests and held-out Precision@K.
- Benchmarked nine further classifiers on identical folds; gradient boosting was kept as a secondary benchmark.
- Ran diagnostics to quantify expression and detectability confounding:
  - feature-family ablation
  - near-miss and expression-matched negative sets
  - expression-only models

</details>

**Primary evaluation (held-out predictions)**

| Metric | Result |
|---|---:|
| ROC-AUC | 0.7848 |
| PR-AUC | 0.0749 *(prevalence 0.025)* |
| ROC-AUC, ten repeated splits | 0.771 ± 0.017 |
| Precision at top 10 | 0.10 |
| Precision at top 20 | 0.05 |
| Precision at top 40 | 0.10 |
| Precision at top 100 | 0.09 |
| ROC-AUC vs near-miss / expression-matched negatives | 0.586 / 0.574 |

*Key finding:* The model ranks positives above strict controls better than chance, with a modest two- to four-fold enrichment among the top-ranked genes. Diagnostics show that this signal is driven mainly by gene expression level and detectability. The genetic, network and pathway predictors alone did not discriminate.

*Interpretation:* These results concern prioritization against the study's defined phenotype. They do not identify causal genes or provide experimental validation; independent evaluation and biological investigation remain necessary.

**Methods:** Python · pandas · scikit-learn · Logistic Regression · Grouped Cross-Validation · Genomic Evidence Integration

🔗 **Code & data:** [github.com/mayishataltab/T2D-Gene](https://github.com/mayishataltab/T2D-Gene)

---

### 02 · 🩺 GlaucomaDetect — Retinal Fundus Image Analysis

**Deep Learning · Medical Image Analysis · Explainable AI**

A comparative machine-learning and deep-learning project for glaucoma detection from retinal fundus images. The best-performing model is integrated into a web-based prediction application.

<details open>
<summary><b>Research and implementation</b></summary>

<br>

- Evaluated traditional machine-learning models: Support Vector Machine (SVM) and XGBoost.
- Compared handcrafted image descriptors with automatic deep feature learning. The descriptors were:
  - Histogram of Oriented Gradients (HOG)
  - Local Binary Patterns (LBP)
  - color histograms
- Investigated transfer-learning architectures: EfficientNetB3 and DenseNet121.
- Applied a two-stage training strategy: warm-up training, then fine-tuning.
- Used Grad-CAM to inspect model attention and check for reliance on image-background regions.
- Developed **GlaucomaDetect**, a browser-based interface for retinal image prediction.

</details>

**Reported DenseNet121 results**

| Metric | Result |
|---|---:|
| Accuracy | 91.00% |
| Precision | 91.55% |
| Recall | 90.33% |
| F1-score | 90.94% |
| AUROC | 0.9638 |

*Research scope:* These results come from the project's evaluated dataset and experimental setup. They are not proof of clinical readiness or of performance on every external population.

**Methods:** Python · TensorFlow/Keras · scikit-learn · OpenCV · Computer Vision · Grad-CAM · Flask

🔗 **Repository:** [github.com/mayishataltab/Glaucoma-Detection](https://github.com/mayishataltab/Glaucoma-Detection)

---

### 03 · 🔊 Urban Sound Classification

**Audio Machine Learning · Signal Processing · Neural Networks**

A multi-class audio-classification project that uses the UrbanSound8K dataset to classify urban environmental sounds.

<details open>
<summary><b>Technical components</b></summary>

<br>

- Extracted Mel-frequency cepstral coefficient (MFCC) features and represented each clip by concatenated MFCC means and standard deviations.
- Developed an artificial neural network (ANN) with tunable architecture and regularization.
- Evaluated an RBF-kernel Support Vector Machine as a baseline.
- Used a stratified 70% / 15% / 15% training, validation and test split.
- Applied audio augmentation to the training data only and reserved the test set for final evaluation.
- Saved model artifacts and preprocessing components to support future inference.

</details>

*Evaluation note:* Performance metrics will be added once the final results have been verified and documented.

**Methods:** Python · TensorFlow/Keras · KerasTuner · librosa · scikit-learn · MFCC · Audio Classification

🔗 **Repository:** [github.com/mayishataltab/Urbansound](https://github.com/mayishataltab/Urbansound)

---

## 🧰 Technical Toolkit

<div align="center">

**Machine Learning & Data Science**

![Python](https://img.shields.io/badge/Python-241710?style=for-the-badge&logo=python&logoColor=E2B77B)
![TensorFlow](https://img.shields.io/badge/TensorFlow-241710?style=for-the-badge&logo=tensorflow&logoColor=E2B77B)
![scikit-learn](https://img.shields.io/badge/scikit--learn-241710?style=for-the-badge&logo=scikitlearn&logoColor=E2B77B)
![XGBoost](https://img.shields.io/badge/XGBoost-241710?style=for-the-badge&logoColor=E2B77B)
![NumPy](https://img.shields.io/badge/NumPy-241710?style=for-the-badge&logo=numpy&logoColor=E2B77B)
![pandas](https://img.shields.io/badge/pandas-241710?style=for-the-badge&logo=pandas&logoColor=E2B77B)

**Computer Vision & Audio**

![OpenCV](https://img.shields.io/badge/OpenCV-241710?style=for-the-badge&logo=opencv&logoColor=E2B77B)
![Keras](https://img.shields.io/badge/Keras-241710?style=for-the-badge&logo=keras&logoColor=E2B77B)
![librosa](https://img.shields.io/badge/librosa-241710?style=for-the-badge&logoColor=E2B77B)
![Flask](https://img.shields.io/badge/Flask-241710?style=for-the-badge&logo=flask&logoColor=E2B77B)

**Software Development & Tools**

![React](https://img.shields.io/badge/React-241710?style=for-the-badge&logo=react&logoColor=E2B77B)
![Node.js](https://img.shields.io/badge/Node.js-241710?style=for-the-badge&logo=nodedotjs&logoColor=E2B77B)
![JavaScript](https://img.shields.io/badge/JavaScript-241710?style=for-the-badge&logo=javascript&logoColor=E2B77B)
![Git](https://img.shields.io/badge/Git-241710?style=for-the-badge&logo=git&logoColor=E2B77B)
![GitHub](https://img.shields.io/badge/GitHub-241710?style=for-the-badge&logo=github&logoColor=E2B77B)
![Google Colab](https://img.shields.io/badge/Google%20Colab-241710?style=for-the-badge&logo=googlecolab&logoColor=E2B77B)

</div>

---

## 🧪 Research Practices

I aim to make my computational work understandable and reproducible:

| Practice | What it means in my work |
|---|---|
| **Transparent evaluation** | Reporting several relevant metrics, with uncertainty, rather than relying on a single score |
| **Leakage-aware workflows** | Keeping label-defining data out of the predictors and fitting all preprocessing inside training folds |
| **Held-out reporting** | Headline results come from data the model has not seen; in-sample values are labelled as apparent |
| **Testing for confounding** | Running diagnostics that check whether a signal reflects the intended evidence or a shortcut |
| **Evidence-based claims** | Separating measured results from interpretation and future possibilities |
| **Documented limitations** | Stating data, evaluation and generalization constraints explicitly |

---

## 🎯 Academic Goals

I plan to pursue doctoral research that connects computer science, machine learning and computational investigation. Directions I am interested in:

- Machine learning for computational genomics and biological evidence integration
- Trustworthy and explainable AI for healthcare
- Robust evaluation of machine-learning models on complex, heterogeneous data
- Computational methods for extracting useful information from images and audio

I welcome opportunities to learn from researchers, contribute to collaborative projects, and develop research questions into rigorous computational studies.

---

## 📬 Contact

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-Explore%20My%20Work-5B3828?style=for-the-badge&logo=github&logoColor=F3E5D0)](https://github.com/mayishataltab)
[![Email](https://img.shields.io/badge/Email-altabmayishat%40gmail.com-5B3828?style=for-the-badge&logo=gmail&logoColor=F3E5D0)](mailto:altabmayishat@gmail.com)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0006--5069--3097-5B3828?style=for-the-badge&logo=orcid&logoColor=F3E5D0)](https://orcid.org/0009-0006-5069-3097)

<br>

*Interested in research collaboration, computational methods and opportunities to learn.*

<br>

---

*"Curiosity begins the question; careful evidence guides the answer."*

**☾ RESEARCH · COMPUTE · INVESTIGATE · DISCOVER ☽**

</div>
