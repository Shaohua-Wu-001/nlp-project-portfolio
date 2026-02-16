# Assignment 4: Retrieval-Augmented Generation with LangChain

## Objective

Implement and evaluate a RAG system that combines hybrid retrieval, reranking, and short-form answer extraction.

## Deliverables

- `rag_pipeline.py`: end-to-end retrieval + generation + evaluation flow
- `requirements.txt`: dependency spec
- `experiment_outputs.json`: saved experiment artifact
- `report.docx`: assignment report

## Retrieval/Generation Stack

- Vector retrieval via Chroma + HuggingFace embeddings
- Lexical retrieval via BM25
- Ensemble retrieval (`BM25 + dense` weighted fusion)
- Cross-encoder reranking (`ms-marco-MiniLM-L-6-v2`)
- Local inference with Ollama (`llama3.2:1b` in source)

## Evaluation Logic

- Exact Match for final answer correctness
- Recall@1 and Recall@5 for retrieval quality
- Error partitioning into retrieval failures vs generation failures
- Detailed per-question comparison output

## Security Fix Applied

A hardcoded Hugging Face token from source was removed.

Use environment variable instead:

```bash
export HF_TOKEN="<your_huggingface_token>"
```

## Suggested Production Hardening

- Move prompt text and retriever weights into config files.
- Persist run metadata (model versions, seed, corpus hash) for auditability.
- Build automated eval harness for prompt/retriever ablations.

