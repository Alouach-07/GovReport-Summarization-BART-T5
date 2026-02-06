# GovReport-Summarization: BART vs T5

This repository contains Jupyter notebooks implementing sequence-to-sequence models for abstractive summarization of government reports. The project focuses on the **GovReport** dataset, specifically filtered for urban, transport, and infrastructure themes.

## Project Overview

The goal of this project is to evaluate and compare two state-of-the-art Transformer architectures—**BART** and **T5**—on the task of condensing long-form legislative and policy documents into concise, informative summaries.

## Dataset

The notebooks use the `govreport-urban-data` hosted on Kaggle. 
- **Train set:** ~3,100 reports
- **Validation set:** ~360 reports
- **Test set:** ~360 reports
- **Characteristics:** High compression ratio (~8-9%) with an average report length of over 5,000 words.

## Models Implemented

1. **BART (Bidirectional and Auto-Regressive Transformers):**
   - Fine-tuned using `facebook/bart-base`.
   - Optimized for denoising and reconstruction tasks.
   
2. **T5 (Text-to-Text Transfer Transformer):**
   - Fine-tuned using `t5-base`.
   - Utilizes a unified text-to-text framework for conditional generation.

## Key Features

- **Preprocessing:** Tokenization and handling of long sequences using truncation and padding.
- **Evaluation:** Implementation of ROUGE metrics to assess summary quality.
- **Analysis:** Comparative statistics on document lengths and topic distribution (Transport, Housing, Finance, etc.).

## Requirements

- Python 3.10+
- Transformers (Hugging Face)
- PyTorch
- Pandas / NumPy
- Rouge-score

## Usage

Each notebook is self-contained. You can run them on Kaggle or locally by adjusting the data paths:
1. `govreport_BART.ipynb`: Training and evaluation of the BART model.
2. `govreport_T5-base.ipynb`: Training and evaluation of the T5 model.

---
**Author:** ALOUACH Abdennour
