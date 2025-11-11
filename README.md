# indobert-vs-mbert-for-indonesian-hoax-news-detection
Comparison of IndoBERT and mBERT performance for detecting political fake news in the Indonesian language using fine-tuning. IndoBERT achieved higher accuracy and AUC, proving its effectiveness in understanding Indonesian linguistic context.

## Comparison of IndoBERT and MBERT Performance for Political Fake News Detection in the Indonesian Language
# Description
This repository contains the implementation and analysis for the research titled “Comparison of IndoBERT and MBERT Performance for Political Fake News Detection in the Indonesian Language”, published in Jurnal Sains dan Teknologi (JST), Vol. 14, No. 1, 2025.
The study aims to evaluate and compare the performance of IndoBERT and Multilingual BERT (mBERT) models in detecting political fake news written in Indonesian. By applying the fine-tuning technique, the models were trained and tested on a labeled dataset of political news articles categorized as factual or hoax.

# Research Objectives
- To develop a fake news detection model for political content in Indonesian using Transformer-based architectures.
- To compare the classification performance of IndoBERT and mBERT on the same dataset.
- To evaluate both models based on accuracy, precision, recall, F1-score, and ROC-AUC metrics.

# Methodology
1. Dataset Preparation
The dataset consists of political news articles labeled as Factual and Hoax, collected from various online media sources.
It was divided into:
- Training set: Used for model learning.
- Validation set: Used to monitor model performance during fine-tuning.
- Test set: Used for final evaluation.

2. Preprocessing
- Lowercasing and text normalization
- Tokenization using the respective model tokenizer (IndoBERT/mBERT)
- Stopword removal and punctuation cleaning
- WordCloud visualization and frequency analysis were performed for both factual and hoax texts

3. Model Fine-Tuning
Both IndoBERT and mBERT were fine-tuned for binary text classification.
Key hyperparameters:
learning_rate = 1e-5
batch_size = 32
num_epochs = 5
weight_decay = 0.1

Early layers (0–8) of IndoBERT were frozen to prevent overfitting and reduce training time.
Fine-tuning was performed on the remaining layers and the classification head.

4. Evaluation Metrics
The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

Confusion matrices were generated to visualize classification performance on the test set.

# Experimental Results
INDOBERT Test set evaluation results:
- Accuracy: 95%
- AUC: 0.946
- Precision (Fact/Hoax): 0.96 / 0.94
- Recall (Fact/Hoax): 0.93 / 0.96
- F1-Score: 0.95

MBERT Test Set Evaluation:
- Accuracy: 92.6%
- Precision (Fact/Hoax): 0.93 / 0.92
- Recall (Fact/Hoax): 0.92 / 0.93
- F1-Score: 0.92
- AUC: 0.982

MBERT achieved good results overall, but slightly lower accuracy and F1-scores compared to IndoBERT, indicating less effectiveness in capturing Indonesian linguistic nuances.

# Conclusion
IndoBERT outperformed mBERT in detecting Indonesian political fake news, showing better adaptation to local linguistic patterns and producing higher accuracy and AUC values.

# Technologies Used
- Python 3.10
- PyTorch
- Hugging Face Transformers
- Scikit-learn
- Matplotlib & Seaborn
- WordCloud
