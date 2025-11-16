# Dementia Risk Prediction Using Non-Medical Self-Reported Factors  
**Team IronHide**  
**November 16, 2025**  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)  
[![Python 3.11](https://img.shields.io/badge/python-3.11-blue.svg)](https://www.python.org/downloads/)  
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.5-orange)](https://scikit-learn.org/)  

---

## Overview

This repository contains the **complete pipeline** for predicting **dementia risk** using **only non-medical, self-reported information** that individuals typically know about themselves.

**No cognitive tests. No brain scans. No lab results.**  
Just **age, education, lifestyle, family history, and simple diagnoses** like *"I had a stroke"* or *"I have diabetes"*.

---

## Key Results

| Metric | Value |
|-------|--------|
| **Model** | Random Forest Classifier |
| **Accuracy** | **94.2%** |
| **ROC-AUC** | **0.962** |
| **Top Risk Factors** | `AGE`, `EDUC`, `DIABETES`, `CBSTROKE`, `HYPERTEN` |
| **Risk Output** | **0–100% personalized risk score** |

---

## Data Source

> **NACC Uniform Data Set (UDS)** – Version 3.0, March 2015  
> *National Alzheimer’s Coordinating Center*  
> [https://naccdata.org](https://naccdata.org)

- **Dataset**: `Dimentia Prediction Dataset.xlsx` (not included in repo due to size >1GB)  
- **Data Dictionary**: `docs/NACC_UDS_Data_Dictionary_v3.0.pdf` (included)

> **Access**: Request data access via [NACC Data Request Portal](https://naccdata.org/requesting-data)


---

## Features Used (All Self-Knowable)

| Category | Features |
|--------|----------|
| **Demographics** | `AGE`, `SEX`, `HISPANIC`, `RACE`, `EDUC`, `MARISTAT`, `INDEPEND`, `RESIDENC`, `HANDED` |
| **Lifestyle** | `TOBAC30`, `TOBAC100`, `SMOKYRS`, `PACKSPER`, `QUITSMOK`, `ALCOCCAS`, `ALCFREQ` |
| **Social** | `NACCLIVS`, `INLIVWTH`, `INVISITS`, `INCALLS`, `INRELY` |
| **Family History** | `NACCFAM`, `NACCMOM`, `NACCDAD` |
| **Health History** | `CVHATT`, `CBSTROKE`, `DIABETES`, `HYPERTEN`, `PD`, `TBI`, `APNEA`, ... |
| **Physical** | `HEIGHT`, `WEIGHT`, `VISION`, `HEARING` |

> **68 features** → ~200 after one-hot encoding  
> **Derived**: `AGE = VISITYR - BIRTHYR`

---

<img width="662" height="343" alt="Screenshot 2025-11-16 222344" src="https://github.com/user-attachments/assets/c0fa344d-6ef0-42c8-940a-52b387222405" />


Model Files (Not in Repo)

File: models/dementia_risk_rf_best.pkl

Size: ~1.2 GB

Reason for exclusion: Exceeds GitHub file size limit (100 MB)

Link to the model: [https://drive.google.com/drive/u/0/folders/1vbvxt_gLQZdfCpfUOUpoB98UqNAxOQYZ](https://drive.google.com/drive/u/0/folders/1vbvxt_gLQZdfCpfUOUpoB98UqNAxOQYZ)
