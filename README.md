# Enhanced Malicious URL Detection Using Multi-Level Feature Attention and Pretrained Language Models

## Project Overview
This research introduces an advanced approach for detecting malicious URLs using CharBERT, a model that captures both subword and character-level representations. The project incorporates three key modules to enhance detection accuracy:
  - Hierarchical Feature Extraction
  - Layer-Aware Attention
  - Spatial Pyramid Pooling

**Dataset**

The project utilizes multiple datasets for training and evaluation:

  - Kaggle Binary Dataset: 632,503 samples (50% malicious, 50% benign)
  - GramBeddings Dataset: 800,000 samples (50% malicious, 50% benign)
  - Mendeley Dataset: 1,561,934 samples (2.2% malicious, 97.8% benign)

**Features Extracted**

| Feature | Description |
| ------- | ----------- |
| input_ids | Tokenized input sequences |
| input_types | Segment IDs for token types |
| input_masks | Attention masks |
| label | 0 for benign, 1 for malicious |
| urltype | URL classification (benign/malicious) |
| start_ids, end_ids, char_ids | CharBERT-specific embeddings |

**Experiments**

**Hyperparameters**

| Parameter | Value |
| --------- | ----- |
| Hidden Size | 768 |
| Attention Heads | 12 |
| Hidden Layers | 12 |
| Dropout Rate | 0.1 |
| Optimizer | AdamW |
| Learning Rate | 2e-5 |
| Batch Size | 64 |
| Epochs | 3 |

## Results on BERT model

**Binary Classification (Kaggle Dataset)**

| Epoch | Accuracy | Precision | Recall | F1-Score |
| ----- | -------- | --------- | ------ | -------- |
| 1 | 49.78% | 49.79% | 7.23% | 12.63% |
| 2 | 50.02% | 50.15% | 72.22% | 59.19% |
| 3 | 50.13% | 50.19% | 84.63% | 63.01% | 

**Multi-Class Classification (Kaggle Dataset)**

| Epoch | Accuracy | Precision | Recall | F1-Score |
| ----- | -------- | --------- | ------ | -------- |
| 1 | 50.12% | 50.16% | 55.84% | 52.85% |
| 2 | 50.05% | 50.08% | 76.37% | 60.49% |
| 3 | 50.09% | 50.05% | 80.37% | 64.89% |

**Testing on Different Datasets**

| Dataset | Accuracy | Precision | Recall | F1-Score |
| ------- | -------- | --------- | ------ | -------- |
| GramBeddings | 45.48% | 47.25% | 77.71% | 58.77% |
| Mendeley | 13.33% | 2.23% | 88.34% | 4.34% |
| Kaggle Binary | 48.92% | 49.36% | 83.37% | 62.01% |

**CharBERT Performance on GramBeddings Dataset**
| Epoch | Accuracy | Precision | Recall | F1-Score |
| ----- | -------- | --------- | ------ | -------- |
| 1 | 97.24% | 97.50% | 96.97% | 97.23% |
| 2 | 97.94% | 98.49% | 97.37% | 97.93% |
| 3 | 98.13% | 99.42% | 96.82% | 98.11% |
| 4 | 98.61% | 98.85% | 98.36% | 98.61% |
| 5 | 98.86% | 99.24% | 98.48% | 98.86% |

**References**

  - W. Ma, Y. Cui, C. Si, T. Liu, S. Wang, and G. Hu, “CharBERT: Character-Aware Pre-Trained Language Model”, arXiv:2011.01513, 2020.
  - R. Liu, Y. Wang, H. Xu, Z. Qin, Y. Liu, Z. Cao, “Malicious URL Detection via Pretrained Language Model Guided Multi-Level Feature Attention Network”, arXiv:2311.12372.

**code credit**
[Github](https://github.com/Alixyvtte/Malicious-URL-Detection-PMANet)
  
