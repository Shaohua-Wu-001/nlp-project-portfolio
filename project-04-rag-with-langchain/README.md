# Project 04: RAG with LangChain

## Overview

A complete Retrieval-Augmented Generation (RAG) pipeline for question answering, featuring hybrid retrieval with cross-encoder reranking and structured error analysis separating retrieval failures from generation failures.

## System Architecture

```
Query → Hybrid Retrieval (BM25 + Dense) → Cross-Encoder Reranking → LLM Generation → Answer
```

### Components

| Stage | Method |
|-------|--------|
| Sparse Retrieval | BM25 via LangChain |
| Dense Retrieval | Vector store with embedding model |
| Ensemble | Weighted combination of sparse + dense scores |
| Reranking | Cross-encoder contextual compression |
| Generation | LLM-based answer extraction from top passages |

### Evaluation Metrics

- **Recall@1** and **Recall@5** for retrieval quality
- **Exact Match (EM)** for end-to-end generation accuracy
- **Error taxonomy**: retrieval failure vs. generation failure

## Usage

```bash
pip install -r requirements.txt
export HF_TOKEN="<your_token>"
python rag_pipeline.py
```

## Files

| File | Description |
|------|-------------|
| `rag_pipeline.py` | End-to-end RAG pipeline implementation |
| `requirements.txt` | Python dependencies |
| `experiment_outputs.json` | Experimental results and metrics |
| `report.docx` | Detailed analysis and findings |

## Key Results

- Performance comparison: BM25-only vs. dense-only vs. hybrid retrieval
- Reranker impact on Recall@1 and Recall@5
- Root-cause analysis of failures (retrieval miss vs. generation hallucination)
