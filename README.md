# Monolingual vs Multilingual BERTa for Question Answering

## Project Overview
This project compares the performance of Monolingual BERTa and Multilingual BERTa on Question Answering (QA) tasks using English and Nepali datasets. It explores how these models perform on high-resource and low-resource languages.

## Motivation
- Evaluate the effectiveness of transformer models in multilingual contexts.
- Understand limitations of Multilingual models in low-resource settings.
- Practical applications: Government, Education, Banking, NLP tasks like NER, Summarization, QA.

## Datasets Used
- **English QA:** [SQuAD](https://rajpurkar.github.io/SQuAD-explorer/)
- **Nepali QA:** Custom created using translation (Google Translate, MarianMT, Ai4Bharat) and manual effort, formatted like SQuAD.

## Workflow
1. Load and format datasets
2. Fine-tune Multilingual BERTa on English and Nepali
3. Fine-tune Monolingual BERTa on English and Nepali
4. Evaluate using F1-score
5. Compare results

## Results Summary

| Language | Monolingual BERTa | Multilingual BERTa |
|----------|-------------------|--------------------|
| English  | **0.088**        | 0.046             |
| Nepali   | 0.0055            | **0.0556**         |

- Monolingual BERTa performs better in English (high-resource).
- Multilingual BERTa performs better in Nepali (low-resource) due to cross-lingual transfer.

## Requirements
See [`requirements.yml`](requirements.yml) for all dependencies.

## Future Work
- Evaluate Hindi dataset.
- Use MultiBlimp for multilingual probing.
- Explore advanced cross-lingual transfer techniques.

## Run Instructions

```bash
git clone https://github.com/your-username/bert-mono-vs-multi.git
cd bert-mono-vs-multi
conda env create -f requirements.yml
conda activate bert-nlp
jupyter notebook NLP_Project.ipynb
