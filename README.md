# Neuro-Symbolic Vision Language Framework for Explainable Medical Diagnosis

![MIT License](https://img.shields.io/badge/License-MIT-green.svg)

## Overview
This project presents a **Neuro-Symbolic Vision-Language Framework** for medical diagnosis that integrates **deep learning perception with structured symbolic reasoning** to deliver **accurate, interpretable, and clinically grounded predictions**.

The system is designed to address a fundamental limitation in medical AI:  
> Traditional models operate as black boxes, whereas clinical decision-making requires **transparent reasoning and multimodal evidence synthesis**.

---

## Key Contributions

- **Multimodal Learning Framework**  
  Combines chest X-ray imaging and clinical symptom understanding.

- **Domain-Adapted DenseNet-121**  
  Improves generalization from NIH ChestX-ray14 → COVID Radiography dataset.

- **Bio_ClinicalBERT Symptom Extractor**  
  Generates structured symptom probability vectors from clinical text.

- **Soft Neuro-Symbolic Reasoning Layer (SNRL)**  
  Encodes clinical diagnostic rules into a learnable, interpretable architecture.

- **Explainability Framework**
  - Grad-CAM for spatial reasoning  
  - Rule-weight interpretation  
  - Per-hypothesis evidence decomposition  

---

## Methodology

The framework follows a **four-stage pipeline**:

1. **Image Stream (CNN)**  
   DenseNet-121 extracts radiological findings.

2. **Text Stream (ClinicalBERT)**  
   Processes symptom descriptions into structured vectors.

3. **Symbolic Representation Layer**  
   Combines multimodal features into interpretable vectors.

4. **Neuro-Symbolic Reasoning Layer**  
   Applies learnable clinical rules for final diagnosis.

---

## Results

### 1. Confusion Matrix
*Classification performance across COVID-19, Pneumonia, and Normal classes*

![Confusion Matrix](https://github.com/user-attachments/assets/ec90bd9c-7ac0-46fc-bb94-4e8af1c4646c)

---

### 2. Training / Validation Performance
*Model convergence and generalization behavior*

![Training Graph](https://github.com/user-attachments/assets/d979c085-1fa3-47cc-af18-045700b058b8)

---

### 3. Grad-CAM Explainability Output
*Spatial visualization of regions influencing diagnostic predictions*

![GradCAM](https://github.com/user-attachments/assets/4f424c3e-0abd-45eb-9344-df264857ac11)

---

## Performance Summary

- **Test Accuracy:** 98.42%  
- **Macro F1-Score:** 0.9791  
- **Macro AUC:** ~0.80  

The system significantly outperforms unimodal baselines by effectively combining **radiological and clinical evidence**, as detailed in the project report :contentReference[oaicite:1]{index=1}.

---

## Explainability

This framework provides **two-level interpretability**:

### 1. Visual Explainability
- Grad-CAM highlights clinically relevant regions in X-rays

### 2. Symbolic Interpretability
- Learned rule weights reflect real clinical reasoning  
- Example:
  - COVID-19 → Dry cough + GGO  
  - Pneumonia → Productive cough + Consolidation  

