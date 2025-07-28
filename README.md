# Fake News Detection

This repository contains code for evaluating and fine-tuning a fake news detector on an adversarial fake news dataset.

## Setup

To run the code:

1. Open the notebook in Google Colab.
2. Upload the `data` directory to the root folder of Google Colab.
3. Run all cells in the notebook.

## Modules

### 1. Data Preprocessing

- Load the full Kaggle dataset.
- Reduce the sample size and ensure real and fake examples are sampled from similar categories (e.g., politics).
- Preprocess the data by filtering out hinting words (such as "Routers," which appear mostly in true examples).
- Create adversarial data labels for each attack, combining original and adversarial labels for all adversarial techniques.

### 2. Fake News Detector Definition

- Define a fake news detector using Gaama3, an LLM model with a prompt tailored for detecting fake news.

### 3. Baseline Evaluation

- Evaluate results on the entire dataset, including both normal and adversarial examples.

### 4. Model Fine-Tuning

- Fine-tune the model on the adversarial examples.

### 5. Fine-Tuned Model Evaluation

- Evaluate the results on the fine-tuned model.
