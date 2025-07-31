# Fake News Detection
## Overview

The project implements a comprehensive evaluation of fake news detection under adversarial conditions by preprocessing balanced datasets, implementing multiple adversarial attack techniques, evaluating baseline model performance, fine-tuning with LoRA adaptation, and comparing robustness improvements.

## Sections
### 1. Data Preprocessing

- Load and balance the Kaggle fake news dataset, sampling equal numbers of real and fake political news articles
- Remove identifying patterns (e.g., "Reuters" markers) to prevent dataset leakage
- Create adversarial variants using multiple attack techniques for comprehensive evaluation

## 2. Adversarial Attack Techniques
1. **Leetspeak Transformation**: Converting letters to numbers (e.g., "a" → "4", "e" → "3")
2. **Unicode Homoglyph Substitution**: Replacing Latin characters with visually similar Greek/Cyrillic characters  
3. **Please Attack**: Adding explicit prompts requesting classification as "real news"
4. **ASCII Smuggling**: Embedding hidden Unicode instructions to influence classification

### 3. Fake News Detector Definition  
- Implement a fake news detector using Google's Gemma-3-1b language model
- Design system prompts optimized for binary classification ("Real" or "Fake")
- Configure the model for sequence classification with appropriate tokenization

### 3. Baseline Evaluation
- Establish performance baseline for comparison with fine-tuned model

### 4. Model Fine-Tuning
- Apply LoRA (Low-Rank Adaptation) fine-tuning on adversarial examples
- Train the model to improve robustness against the implemented attack techniques

### 5. Fine-Tuned Model Evaluation
- Re-evaluate model performance on the same test sets post-fine-tuning
- Compare classification accuracy and robustness improvements
- Analyze the effectiveness of adversarial training for improving model resilience

## Setup
1. Open `main.ipynb` in Google Colab
2. Upload the `data/` directory containing `Fake.csv` and `True.csv`
3. Run all cells to reproduce the complete evaluation pipeline

