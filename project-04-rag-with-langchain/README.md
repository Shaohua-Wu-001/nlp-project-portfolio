# Project 04: RAG with LangChain

## Overview

This project builds a Retrieval-Augmented Generation pipeline with:

- Hybrid retrieval (`BM25` + embedding retriever)
- Cross-encoder reranking
- Local LLM inference flow via Ollama
- Evaluation using Exact Match and retrieval recall metrics

## Highlights

- Knowledge base ingestion from plain-text facts
- Ensemble retrieval and contextual compression
- Prompt-controlled short-answer extraction
- End-to-end evaluation and JSON result export

## Files

- `rag_langchain_pipeline.py`: Main Colab-style pipeline
- `requirements.txt`: Dependency list
- `knowledge_base.txt`: Retrieval corpus
- `eval_questions_answers.txt`: Evaluation prompts and answers
- `rag_results.json`: Stored output artifact
- `report.docx`: Project report

## Security Update Applied

The original hardcoded Hugging Face token was removed.

Use:

```bash
export HF_TOKEN="<your_token>"
```

before running login-required cells.

