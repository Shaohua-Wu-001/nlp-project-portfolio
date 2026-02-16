# Project 02: Arithmetic as a Language

## 專案簡介

把算術運算當成字元序列生成任務：模型讀到 `=` 後開始生成答案，直到 `<eos>`。

## 內容檔案

- `arithmetic_sequence_model.py`
- `requirements.txt`
- `report.docx`

## 模型設計重點

- Character vocabulary + `<pad>` / `<eos>`
- `Embedding -> LSTM -> LSTM -> MLP`
- Cross-entropy 訓練 + gradient clipping
- 自回歸解碼做驗證

## Step-by-Step 自己嘗試

1. 先檢查字典建立是否涵蓋所有運算符號與數字。
2. 跑原始超參數，拿到初版 validation accuracy。
3. 調整 `embed_dim` / `hidden_dim` / `lr` 比較收斂曲線。
4. 檢查生成失敗樣本（長式子、負號、連續運算）。
5. 重新設定資料切分或長度分桶，看是否提升穩定度。

## 更深入可做

- 加入 teacher forcing ratio 控制。
- 試 Transformer decoder 與 LSTM 的性能比較。
- 增加 per-length/per-operator 的 error report。

