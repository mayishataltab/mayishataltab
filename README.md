
<div align="center">


<br>

# Mayishat Altab Mridu

### Computer Science Graduate | Machine Learning | Computational Research

*Building intelligent systems and exploring data-driven approaches to complex problems.*

<br>

[![Research](https://img.shields.io/badge/Focus-Computational%20Research-5B3828?style=flat-square&labelColor=21140F)](#research-interests)
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Deep%20Learning-B77943?style=flat-square&labelColor=21140F)](#technical-toolkit)
[![Open to Research](https://img.shields.io/badge/Goal-PhD%20Research-CB9A62?style=flat-square&labelColor=21140F)](#academic-goals)

<br>

**RESEARCH · COMPUTE · INVESTIGATE · DISCOVER**

</div>

---

## About Me

I am a Computer Science and Engineering graduate from Daffodil International University, Bangladesh, with interests in machine learning, deep learning, and computational research.

My work explores how computational methods can be applied to problems in healthcare, environmental sound analysis, and genomics. I am particularly interested in developing reproducible machine-learning workflows, evaluating models carefully, and interpreting results within the limitations of the available evidence.

I am building this portfolio to document my technical work, research development, and preparation for future **PhD research opportunities**.

- 🎓 **Background:** Computer Science and Engineering
- 🧠 **Core interests:** Machine learning, deep learning, and data-driven modeling
- 🩺 **Healthcare AI:** Retinal fundus image analysis and glaucoma detection
- 🧬 **Computational genomics:** Evidence integration and candidate-gene prioritization
- 🔊 **Audio intelligence:** Urban environmental sound classification
- 🔬 **Research approach:** Careful evaluation, reproducibility, and evidence-based interpretation

---

## Research Interests

<table>
<tr>
<td width="50%" valign="top">

### 🧬 Computational Genomics

Integrating genetic-association, transcriptomic, tissue-expression, interaction-network, and pathway evidence to prioritize candidate genes for further biological investigation.

</td>
<td width="50%" valign="top">

### 🩺 Medical AI

Applying deep learning and computer vision to retinal fundus images, with an interest in model evaluation, explainability, and practical screening applications.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### 🔊 Machine Learning for Audio

Investigating audio feature extraction and supervised learning for the classification of urban environmental sounds.

</td>
<td width="50%" valign="top">

### 🔍 Reliable Machine Learning

Exploring evaluation design, leakage prevention, model comparison, interpretability, and the limitations of computational predictions.

</td>
</tr>
</table>

---

## Featured Research & Projects

### 01 · 🧬 Multi-Evidence Gene Prioritization for Type 2 Diabetes

**Computational Genomics · Machine Learning · Evidence Integration**

A genetics-centered computational study investigating whether heterogeneous gene-level evidence can help prioritize candidate genes associated with a defined human pancreatic β-cell type 2 diabetes (T2D) differential-expression phenotype.

**Research components**
- Integrated genetic-association, regulatory, transcriptomic, tissue-expression, protein–protein interaction, and pathway evidence.
- Constructed an analytical dataset of **3,868 genes**, comprising 51 positive genes, 1,991 strict controls, and 1,826 unlabeled genes.
- Used a fixed set of 14 predictors while excluding target-derived GSE221156 measurements from the primary predictor matrix.
- Evaluated L2-regularized logistic regression using nested grouped five-fold cross-validation, with three inner folds.
- Examined both discrimination and ranking performance to support candidate prioritization.

**Reported primary evaluation**
| Metric | Result |
|---|---:|
| ROC-AUC | 0.7857 |
| PR-AUC | 0.0832 |
| Precision at top 10 | 0.40 |
| Precision at top 20 | 0.20 |
| Precision at top 40 | 0.10 |
| Precision at top 100 | 0.09 |

*Interpretation:* These results concern prioritization against the study's defined phenotype. They do not establish causal genes or experimental validation. Independent evaluation and biological investigation remain necessary.

**Methods:** Python · pandas · scikit-learn · Logistic Regression · Grouped Cross-Validation · Genomic Evidence Integration

https://github.com/mayishataltab/T2D-Gene

---

### 02 · 🩺 GlaucomaDetect — Retinal Fundus Image Analysis

**Deep Learning · Medical Image Analysis · Explainable AI**

A comparative machine-learning and deep-learning project for glaucoma detection from retinal fundus images, with the best-performing model integrated into a web-based prediction application.

**Research and implementation**
- Evaluated traditional machine-learning models: Support Vector Machine (SVM) and XGBoost.
- Compared handcrafted image descriptors—Histogram of Oriented Gradients (HOG), Local Binary Patterns (LBP), and color histograms—with automatic deep feature learning.
- Investigated transfer-learning architectures: EfficientNetB3 and DenseNet121.
- Applied a two-stage training strategy involving warm-up training and fine-tuning.
- Used Grad-CAM to investigate model attention and examine potential reliance on image-background regions.
- Developed **GlaucomaDetect**, a browser-based interface for retinal image prediction.

**Reported DenseNet121 results**

| Metric | Result |
|---|---:|
| Accuracy | 91.00% |
| Precision | 91.55% |
| Recall | 90.33% |
| F1-score | 90.94% |
| AUROC | 0.9638 |

**Methods:** Python · TensorFlow/Keras · scikit-learn · OpenCV · Computer Vision · Grad-CAM · Flask

*Research scope:* The reported results come from the project's evaluated dataset and experimental setup. They should not be interpreted as proof of clinical readiness or performance on every external population.

https://github.com/mayishataltab/Glaucoma-Detection

---

### 03 · 🔊 Urban Sound Classification

**Audio Machine Learning · Signal Processing · Neural Networks**

A multi-class audio-classification project using the UrbanSound8K dataset to investigate the classification of urban environmental sounds.

**Technical components**
- Extracted audio features using Mel-frequency cepstral coefficients (MFCCs).
- Represented audio using concatenated MFCC means and standard deviations.
- Developed an artificial neural network (ANN) with tunable architecture and regularization.
- Evaluated an RBF-kernel Support Vector Machine as a baseline.
- Used a stratified 70% training, 15% validation, and 15% test split.
- Applied audio augmentation to training data and reserved the test set for final evaluation.
- Saved model artifacts and preprocessing components to support future inference.

**Methods:** Python · TensorFlow/Keras · KerasTuner · librosa · scikit-learn · MFCC · Audio Classification

*Evaluation note:* Performance metrics will be added after the final results have been verified and documented.

https://github.com/mayishataltab/Urbansound

---

## Technical Toolkit

<div align="center">

### Machine Learning & Data Science

![Python](https://img.shields.io/badge/Python-241710?style=for-the-badge&logo=python&logoColor=E2B77B)
![TensorFlow](https://img.shields.io/badge/TensorFlow-241710?style=for-the-badge&logo=tensorflow&logoColor=E2B77B)
![scikit-learn](https://img.shields.io/badge/scikit--learn-241710?style=for-the-badge&logo=scikitlearn&logoColor=E2B77B)
![XGBoost](https://img.shields.io/badge/XGBoost-241710?style=for-the-badge&logoColor=E2B77B)
![NumPy](https://img.shields.io/badge/NumPy-241710?style=for-the-badge&logo=numpy&logoColor=E2B77B)
![pandas](https://img.shields.io/badge/pandas-241710?style=for-the-badge&logo=pandas&logoColor=E2B77B)

### Computer Vision & Audio

![OpenCV](https://img.shields.io/badge/OpenCV-241710?style=for-the-badge&logo=opencv&logoColor=E2B77B)
![Keras](https://img.shields.io/badge/Keras-241710?style=for-the-badge&logo=keras&logoColor=E2B77B)
![Flask](https://img.shields.io/badge/Flask-241710?style=for-the-badge&logo=flask&logoColor=E2B77B)

### Software Development & Tools

![React](https://img.shields.io/badge/React-241710?style=for-the-badge&logo=react&logoColor=E2B77B)
![Node.js](https://img.shields.io/badge/Node.js-241710?style=for-the-badge&logo=nodedotjs&logoColor=E2B77B)
![JavaScript](https://img.shields.io/badge/JavaScript-241710?style=for-the-badge&logo=javascript&logoColor=E2B77B)
![Git](https://img.shields.io/badge/Git-241710?style=for-the-badge&logo=git&logoColor=E2B77B)
![GitHub](https://img.shields.io/badge/GitHub-241710?style=for-the-badge&logo=github&logoColor=E2B77B)

</div>

---

## Research Practices

I aim to make my computational work understandable and reproducible through:

- **Transparent evaluation:** reporting relevant metrics rather than relying on a single score.
- **Leakage-aware workflows:** separating training, validation, and test data appropriately.
- **Evidence-based claims:** distinguishing measured results from interpretation and future possibilities.
- **Model interpretability:** examining model behavior where suitable methods are available.
- **Documented limitations:** identifying data, evaluation, and generalization constraints.

---

## Academic Goals

I am interested in pursuing doctoral research in areas connecting computer science, machine learning, and computational investigation.

Potential research directions include:

- Machine learning for computational genomics and biological evidence integration.
- Trustworthy and explainable AI for healthcare applications.
- Robust evaluation of machine-learning models on complex, heterogeneous data.
- Computational methods for extracting useful information from images and audio.

I welcome opportunities to learn from researchers, contribute to collaborative projects, and develop research questions into rigorous computational studies.

---

## GitHub & Contact

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-Explore%20My%20Work-5B3828?style=for-the-badge&logo=github&logoColor=F3E5D0)](https://github.com/mayishataltab)

<br>

*Interested in research collaboration, computational methods, and opportunities to learn.*

<br>

---

*“Curiosity begins the question; careful evidence guides the answer.”*

**☾ RESEARCH · COMPUTE · INVESTIGATE · DISCOVER ☽**

</div>
