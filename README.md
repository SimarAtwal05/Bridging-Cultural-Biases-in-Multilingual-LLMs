# Bridging Cultural Biases in Multilingual LLMs
## Disagreement-Aware Fine-Tuning and Preference Optimization for Culturally Aware Multilingual Language Models

This repository contains the Google Colab notebooks and experimental results for the research project **"Bridging Cultural Biases in Multilingual LLMs through Disagreement-Aware Fine-Tuning and Preference Optimization."**

The project presents a six-stage framework for investigating cultural inconsistencies in multilingual Large Language Models (LLMs). It combines cultural annotation, multilingual translation, semantic evaluation, supervised fine-tuning, cross-validation, and preference optimization to improve cross-lingual semantic consistency while preserving meaningful cultural differences.

---

## 🔬 Research Overview

Multilingual LLMs can generate responses in multiple languages but may produce different interpretations of culturally sensitive prompts across languages. 

This research investigates whether alignment techniques can improve cross-lingual semantic consistency without treating every cultural difference as an error. The framework uses culturally annotated prompts, multilingual response generation, Sentence-BERT-based semantic evaluation, supervised fine-tuning, and PPO-based preference optimization.

---

## 🚀 Key Highlights

* Developed a six-stage framework for culturally aware multilingual LLM alignment.
* Created a dataset of 300 culturally sensitive prompts covering five cultural domains.
* Translated prompts into six Indic languages using NLLB-200.
* Evaluated multilingual models including mT5, BLOOM, and IndicBART.
* Used Sentence-BERT embeddings and cosine similarity to measure cross-lingual semantic consistency.
* Applied supervised fine-tuning to improve multilingual response consistency.
* Implemented grouped 5-fold cross-validation to evaluate generalization across unseen prompt groups.
* Constructed 252 preference pairs for reward model training and PPO-based preference optimization.
* Investigated disagreement-aware alignment to distinguish undesirable semantic divergence from meaningful cultural differences.

---

## 🌍 Languages Covered

The research covers the following languages:
* English
* Hindi
* Tamil
* Telugu
* Malayalam
* Punjabi
* Nepali

---

## 🔬 Research Pipeline

The project is organized into six stages:

| Stage | Description |
| :--- | :--- |
| **Stage 1** | Cultural prompt dataset construction and human annotation |
| **Stage 2** | Translation of culturally annotated prompts into six Indic languages using NLLB-200 |
| **Stage 3** | Multilingual response generation using mT5, BLOOM, and IndicBART |
| **Stage 4** | Cross-lingual semantic evaluation using Sentence-BERT and cosine similarity |
| **Stage 5** | Supervised fine-tuning of mT5-base and grouped 5-fold cross-validation |
| **Stage 6** | Preference pair construction, reward model training, and PPO-based preference optimization |

---

## 📊 Experimental Results

The framework was evaluated progressively using cross-lingual semantic similarity.

### Baseline Model Comparison
| Model | Average Semantic Similarity |
| :--- | :--- |
| IndicBART | 0.14 |
| BLOOM | 0.26 |
| mT5 | 0.49 |

### Alignment Performance
| Model Configuration | Average Semantic Similarity |
| :--- | :--- |
| mT5 Baseline | 0.49 |
| Supervised Fine-Tuning | 0.74 |
| Grouped 5-Fold Cross-Validation | $0.7398 \pm 0.0420$ |
| Preference Optimization (PPO-based RLHF) | 0.91 |

### Additional Findings
* Cultural annotation achieved a Cohen's Kappa of **0.79021**.
* A total of **252** chosen–rejected preference pairs were constructed.
* The average preference margin was **0.3564**.
* Fine-tuning improved semantic consistency across most evaluated languages, although improvements varied by language.

> ⚠️ **Interpretation:** The reported improvements reflect increased semantic consistency according to the evaluation framework. Higher semantic similarity does not necessarily indicate greater cultural correctness. The objective is to reduce undesirable semantic divergence while preserving valid cultural differences.

---

## 🛠️ Technologies Used

* Python
* Google Colab
* PyTorch
* Hugging Face Transformers
* **NLLB-200** — Multilingual prompt translation
* **mT5, BLOOM, and IndicBART** — Multilingual language models
* **Sentence-BERT** — Cross-lingual semantic evaluation
* **Pandas** — Data processing and analysis
* **Proximal Policy Optimization (PPO)** — Preference-based policy optimization

---

## ⚙️ Experimental Configuration

| Component | Configuration |
| :--- | :--- |
| Fine-tuning model | `mT5-base` |
| Fine-tuning epochs | 3 |
| Fine-tuning batch size | 4 |
| Maximum input and target length | 128 tokens |
| Cross-validation | Grouped 5-fold cross-validation |
| Preference pairs | 252 |
| Reward model optimizer | AdamW |
| PPO learning rate | $5 \times 10^{-6}$ |
| PPO clipping range | 0.2 |
| KL penalty coefficient | 0.05 |

---

## 📈 Evaluation Methodology

1. **Cohen's Kappa:** Used to measure agreement between human annotators during cultural prompt annotation.
2. **Sentence-BERT Semantic Similarity:** Multilingual Sentence-BERT embeddings are used to compare responses generated across different languages.
3. **Cosine Similarity:** Used to measure cross-lingual semantic consistency between response embeddings.
4. **Grouped 5-Fold Cross-Validation:** Prompts originating from the same base question are grouped together to prevent related samples from appearing in both training and validation sets.
5. **Preference Margin:** Used to measure the difference in semantic similarity between selected and rejected responses during preference pair construction.

---

## 🎯 Research Objectives

* Investigate cultural inconsistencies in multilingual LLM responses.
* Evaluate cross-lingual semantic consistency across Indic languages.
* Develop a culturally contextualized evaluation framework.
* Improve multilingual response behavior through supervised fine-tuning.
* Explore disagreement-aware preference optimization for cultural alignment.
* Distinguish undesirable semantic divergence from meaningful cultural differences.

---

## ⚠️ Reproducibility and Data Availability

The notebooks in this repository were developed using Google Colab. Some experiments may require:
* GPU resources.
* Access to pretrained models through Hugging Face.
* Appropriate computational resources for fine-tuning and PPO-based optimization.

The repository contains the research notebooks and experimental results organized by stage. Dataset and model availability may depend on the licensing conditions of the respective resources. Before running the notebooks, review the dataset paths and required dependencies.

---

