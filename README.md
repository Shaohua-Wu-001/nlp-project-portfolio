# NLP Project Portfolio

This repository packages five independent NLP mini-projects as a clean engineering portfolio.

## Projects

| Project | Topic | Main Deliverables |
| --- | --- | --- |
| `assignment-01-word-analogy` | Assignment 1: Word Analogy | Python pipeline, requirements, report |
| `assignment-02-arithmetic-as-a-language` | Assignment 2: Arithmetic as a Language | PyTorch char-level sequence model, requirements, report |
| `assignment-03-multi-output-learning` | Assignment 3: Multi-output Learning | BERT multi-task training script, requirements, report, specification |
| `assignment-04-rag-with-langchain` | Assignment 4: Retrieval-Augmented Generation with LangChain | RAG pipeline, requirements, experiment outputs, report |
| `project-05-wattbot-term-project` | Term Project: NLP_WattBot 2025_AttentionPlease | Final report |

## Course Outcome Snapshot

- Assignment 1: `100 / 100`
- Assignment 2: `96 / 100`
- Assignment 3: score not included in source folder
- Assignment 4: score not included in source folder
- Term Project: grade metadata not included in source folder

## Engineering Principles Used in This Packaging

- `Source-of-truth first`: files were rebuilt only from `/Users/chengpeici/Desktop/NLP`.
- `Anonymized artifact naming`: no school name, student ID, or homework-style labels in repository paths.
- `Credential safety`: hardcoded Hugging Face token was removed from the RAG script and replaced by `HF_TOKEN` env usage.
- `Reproducibility-friendly structure`: each project has an isolated README and dependency file.

## Repository Layout

```text
.
├── assignment-01-word-analogy
├── assignment-02-arithmetic-as-a-language
├── assignment-03-multi-output-learning
├── assignment-04-rag-with-langchain
└── project-05-wattbot-term-project
```

## Notes

- Most scripts are Colab-exported and still contain notebook shell commands (`!pip`, `!wget`, `drive.mount`, etc.).
- For production-grade local execution, convert notebook-magics into CLI/bootstrap scripts.
