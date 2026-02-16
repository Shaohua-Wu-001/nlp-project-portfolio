# Project 01: Analogy and Embeddings

## Overview

This project explores lexical analogy solving with two approaches:

- Pretrained embeddings (`glove-wiki-gigaword-100` via Gensim)
- A custom Word2Vec model trained on sampled Wikipedia text

The workflow covers preprocessing, benchmarking by category/subcategory, and embedding visualization.

## Highlights

- Parses Google analogy benchmark into a structured dataframe
- Evaluates semantic vs syntactic analogy accuracy
- Trains a memory-optimized Word2Vec pipeline (frequency filters, phrase handling, callback-based monitoring)
- Visualizes selected semantic neighborhoods using t-SNE

## Files

- `analogy_embeddings_pipeline.py`: Main Colab-style pipeline script
- `requirements.txt`: Dependency set for training and evaluation
- `report.docx`: Project report

## Run Notes

This script was exported from Colab and includes notebook shell cells (e.g., `!pip`, `!wget`).

For practical execution:

1. Use Colab/Jupyter directly, or
2. Refactor shell-magics into standard Python/subprocess commands for local execution.

