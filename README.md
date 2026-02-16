# NLP Independent Project Portfolio

這個 repository 整理了 5 個彼此獨立的 NLP 專案。

## Projects

| Folder | Project Focus | Deliverables |
| --- | --- | --- |
| `project-01-word-analogy` | Word Analogy and Embedding Analysis | pipeline code, requirements, report |
| `project-02-arithmetic-as-language` | Arithmetic as a Language (character-level sequence modeling) | model code, requirements, report |
| `project-03-multi-output-learning` | Multi-output Learning with shared BERT backbone | training code, requirements, report, specification |
| `project-04-rag-with-langchain` | Retrieval-Augmented Generation QA system | RAG code, requirements, experiment outputs, report |
| `project-05-wattbot` | WattBot final project package | final report |

## How To Read This Repo

1. 先進入任一專案資料夾。
2. 打開該專案的 `README.md`，裡面有更詳細的背景、方法、工程拆解。
3. 依照 README 的 step-by-step 試做流程，自己一步一步重跑與調整。

## Engineering Notes

- 檔案來源以本機最新資料夾 `/Users/chengpeici/Desktop/NLP` 為準。
- 專案路徑與公開敘述已做去識別化，不使用學校與學號標記。
- `project-04-rag-with-langchain/rag_pipeline.py` 已移除硬編碼 Hugging Face token，改成讀取 `HF_TOKEN` 環境變數。
- 多數腳本仍保留 Colab 風格命令（例如 `!pip`），若要本地化建議再拆成 CLI + module。

## Layout

```text
.
├── project-01-word-analogy
├── project-02-arithmetic-as-language
├── project-03-multi-output-learning
├── project-04-rag-with-langchain
└── project-05-wattbot
```

