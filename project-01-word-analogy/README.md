# Project 01: Word Analogy

## 專案簡介

這個專案聚焦在詞向量對 analogy 任務的表現，包含：

- 預訓練詞向量 baseline（GloVe）
- 自行訓練 Word2Vec
- 類比題 accuracy 分析（semantic / syntactic）
- t-SNE 視覺化

## 內容檔案

- `word_analogy_pipeline.py`
- `requirements.txt`
- `report.docx`

## Step-by-Step 自己嘗試

1. 先跑資料前處理，確認 `questions-words` 轉換正確。
2. 跑 GloVe baseline，記錄 semantic / syntactic accuracy。
3. 跑自訓練 Word2Vec 區塊，改不同 `vector_size`、`window`、`min_count`。
4. 比較 baseline 與自訓練模型結果差異。
5. 產生 t-SNE，觀察 family/royalty 等關係是否成群。

## 更深入可做

- 加入多 seed 重複實驗，輸出平均與標準差。
- 做 error taxonomy（OOV、詞形變化、語義偏移）。
- 把 notebook 風格腳本拆成可重跑的模組化 pipeline。

