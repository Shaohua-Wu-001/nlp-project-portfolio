# Project 01: Word Analogy and Embedding Analysis

## Overview

This project evaluates word embedding models on the standard word analogy task. We compare pretrained GloVe vectors against a custom-trained Word2Vec model, analyzing performance on both semantic and syntactic analogy categories with t-SNE visualizations of learned representations.

## Methodology

1. **Baseline** — Pretrained GloVe embeddings evaluated on the `questions-words` analogy dataset
2. **Custom Training** — Word2Vec (Skip-gram) trained with configurable `vector_size`, `window`, and `min_count`
3. **Evaluation** — Per-category accuracy breakdown across semantic and syntactic analogy types
4. **Visualization** — t-SNE projections of embedding clusters (family, royalty, etc.)

## Usage

```bash
pip install -r requirements.txt
python word_analogy_pipeline.py
```

## Files

| File | Description |
|------|-------------|
| `word_analogy_pipeline.py` | Full pipeline: data loading, training, evaluation, visualization |
| `requirements.txt` | Python dependencies |
| `report.docx` | Detailed analysis and results |

## Key Results

- Semantic vs. syntactic accuracy comparison between GloVe and custom Word2Vec
- t-SNE clusters showing meaningful groupings (e.g., family relations, verb tenses)
- Analysis of failure modes: OOV tokens, morphological variation, semantic drift
