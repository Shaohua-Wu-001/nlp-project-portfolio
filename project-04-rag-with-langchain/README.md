# Project 04: RAG with LangChain

## 專案簡介

這個專案實作一套完整的 RAG QA 流程：

- Dense + sparse hybrid retrieval
- Cross-encoder reranking
- LLM 回答抽取
- Retrieval / generation 分開評估

## 內容檔案

- `rag_pipeline.py`
- `requirements.txt`
- `experiment_outputs.json`
- `report.docx`

## 系統重點

- Ensemble Retriever：BM25 + vector retriever
- Contextual compression：cross-encoder reranker
- 評估指標：`Recall@1`、`Recall@5`、`Exact Match`
- Error split：retrieval failure vs generation failure

## Step-by-Step 自己嘗試

1. 先建立 retrieval corpus，驗證 chunk 與向量索引可用。
2. 固定 prompt，先比較 pure BM25 vs dense retrieval。
3. 開 reranker 後再測一次，記錄 Recall 變化。
4. 調 prompt 與 top-k，觀察 EM 與 hallucination 變化。
5. 對失敗題做 root-cause 分析（檢索不到 / 生成提取失敗）。

## 安全與執行注意

- 不使用硬編碼 Hugging Face token。
- 需自行設定 `HF_TOKEN`：

```bash
export HF_TOKEN="<your_token>"
```

