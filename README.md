# NLP Project Portfolio

[![Python 3.9+](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)](https://pytorch.org)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat&logo=huggingface&logoColor=black)](https://huggingface.co)
[![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)](https://langchain.com)

Five independent NLP projects spanning core topics in natural language processing — from classical word embeddings to modern retrieval-augmented generation. Each project includes a complete implementation, reproducible pipeline, and written report.

---

## Projects

| # | Project | Methods | Key Topics |
|---|---------|---------|------------|
| 01 | [Word Analogy](project-01-word-analogy/) | GloVe, Word2Vec, t-SNE | Word embeddings, analogy evaluation |
| 02 | [Arithmetic as Language](project-02-arithmetic-as-language/) | LSTM seq2seq, autoregressive decoding | Character-level modeling, sequence generation |
| 03 | [Multi-Output Learning](project-03-multi-output-learning/) | BERT, multi-task learning | Shared encoders, dual-head architectures |
| 04 | [RAG with LangChain](project-04-rag-with-langchain/) | BM25, dense retrieval, cross-encoder | Hybrid retrieval, reranking, RAG |
| 05 | [WattBot](project-05-wattbot/) | End-to-end QA system | Capstone project, full system design |

## Repository Structure

```
.
├── project-01-word-analogy/
│   ├── word_analogy_pipeline.py
│   ├── requirements.txt
│   └── report.docx
├── project-02-arithmetic-as-language/
│   ├── arithmetic_sequence_model.py
│   ├── requirements.txt
│   └── report.docx
├── project-03-multi-output-learning/
│   ├── multi_output_bert.py
│   ├── requirements.txt
│   ├── specification.pdf
│   └── report.docx
├── project-04-rag-with-langchain/
│   ├── rag_pipeline.py
│   ├── requirements.txt
│   ├── experiment_outputs.json
│   └── report.docx
└── project-05-wattbot/
    └── report.pdf
```

## Getting Started

Each project is self-contained. Navigate to any project directory, install dependencies, and run the pipeline:

```bash
cd project-<number>-<name>
pip install -r requirements.txt
python <main_script>.py
```

Refer to the individual project READMEs for detailed instructions and expected outputs.

## License

MIT
