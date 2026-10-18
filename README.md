# Twitter Sentiment Analysis Using Machine Learning and Transformers


## Overview

This project focuses on classifying tweets into three sentiment categories: **positive, neutral, and negative**. It compares a traditional machine learning approach using TF-IDF features with a transformer-based RoBERTa model fine-tuned for sentiment classification.

The goal is to evaluate both approaches and understand how contextual language representations affect sentiment prediction.

## Objectives

- Perform three-class sentiment classification on Twitter data.
- Establish a baseline using TF-IDF features.
- Fine-tune a pretrained RoBERTa model.
- Compare model performance using accuracy and Macro F1-score.
- Explore the effects of different random seeds and class weighting.

## Dataset

The project uses the sentiment-analysis subset of TweetEval.

- **Dataset:** [TweetEval on Hugging Face](https://huggingface.co/datasets/cardiffnlp/tweet_eval)
- **Repository:** [Cardiff NLP TweetEval](https://github.com/cardiffnlp/tweeteval)

The dataset contains tweets labelled as positive, neutral, or negative. The original dataset splits should be preserved for fair evaluation.

## Methodology

### 1. Data Preparation
Tweets and sentiment labels are prepared for training and evaluation. Text is transformed into numerical features for the baseline model and tokenized for RoBERTa.

### 2. TF-IDF Baseline
TF-IDF converts text into numerical features based on word importance. These features are used with a traditional classification model to establish baseline performance.

### 3. RoBERTa Fine-Tuning
A pretrained RoBERTa transformer model is fine-tuned on labelled tweets to predict one of the three sentiment classes.

### 4. Experiments
The experiments compare:
- TF-IDF baseline
- RoBERTa with random seed 42
- RoBERTa with random seed 7
- RoBERTa with class weighting

## Evaluation Metrics

- **Accuracy:** The proportion of correctly classified tweets.
- **Macro F1-score:** The average F1-score across all classes, giving each class equal weight.

## Results

The following are the recorded results and should be verified against the final notebook outputs before publication.

| Model | Accuracy | Macro F1-score |
|---|---:|---:|
| TF-IDF baseline | 58.94% | 55.33% |
| RoBERTa (seed 42) | 70.99% | 71.09% |
| RoBERTa (seed 7) | 70.61% | 70.86% |
| RoBERTa (class weighted) | 69.12% | 69.24% |

RoBERTa with seed 42 achieved the highest recorded accuracy and Macro F1-score among the evaluated experiments.

## Technologies Used

- Python
- Natural Language Processing (NLP)
- TF-IDF
- Transformer models
- RoBERTa
- Hugging Face
- Scikit-learn
- Google Colab

## Project Notebook

[**Open the Google Colab Notebook**](https://colab.research.google.com/drive/1OIVEp7_8bi6g6E6V8BLNyv0WGp782GL_?usp=sharing)

## Limitations and Future Improvements

Sentiment classification can be challenging because of sarcasm, ambiguous expressions, slang, emojis, and class imbalance. Future improvements could include confusion-matrix analysis, more random-seed experiments, hyperparameter tuning, and testing on additional datasets.

## Conclusion

This project compares traditional text-based features with contextual transformer representations for Twitter sentiment analysis. In the recorded experiments, RoBERTa outperformed the TF-IDF baseline on both accuracy and Macro F1-score.

---

**Author:** Ashitha P   
**Date:** 19 October 2026
