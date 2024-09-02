# Question Similarity Detection Using Sentence Transformer

## Project Overview

The goal of this project is to develop a model that accurately identifies the similarity between pairs of questions. This is particularly useful in applications like duplicate question detection, where the objective is to determine if two questions are essentially asking the same thing.

## Objective

To train a Sentence Transformer model that calculates the semantic similarity between two questions. The model is trained on a labeled dataset where each pair of questions is annotated with a binary label:

- **1:** The questions are similar or duplicates.
- **0:** The questions are not similar.

## Approach

1. **Data Preparation:**
   - The dataset consists of pairs of questions, with each pair labeled as either similar (1) or not similar (0).
   - The questions are preprocessed to clean the text, including steps like removing stop words, punctuation, and any unnecessary characters.
2. **Model Selection:**

   - A pre-trained Sentence Transformer model ("msmarco-distilbert-base-tas-b") is used as the base. This model is fine-tuned on the prepared dataset to learn the nuances of question similarity specific to the data.

3. **Training:**

   - The model is trained to minimize the difference between the predicted similarity score and the actual label (1 or 0).
   - Various training techniques are employed to optimize performance.

4. **Evaluation:**

   - The model’s performance was evaluated using both Pearson and Spearman correlation metrics:
     - **Pearson Correlation:** 0.6809
     - **Spearman Correlation:** 0.7165
   - These metrics indicate a strong correlation between the predicted and actual similarity scores, demonstrating the model's effectiveness.

## Expected Outcomes

- A robust Sentence Transformer model capable of accurately predicting the similarity between two questions.
- The model’s strong correlation scores indicate it reliably captures semantic similarity, making it a valuable tool for various NLP tasks.

This project leverages the power of Sentence Transformers to address a common problem in natural language processing, providing a scalable and effective solution for question similarity detection.
