# Project 03: Multi-output Learning

## 專案簡介

使用單一 BERT backbone 同時做兩個任務：

- Regression：relatedness score
- Classification：entailment judgment

## 內容檔案

- `multi_output_bert.py`
- `requirements.txt`
- `report.docx`
- `specification.pdf`

## 訓練與評估

- Shared encoder + dual heads
- Loss = `MSE + CrossEntropy`
- 指標：Pearson（回歸）+ Accuracy（分類）
- 以 combined score 保存最佳 checkpoint

## Step-by-Step 自己嘗試

1. 先確認 dataloader 的 tokenization 與 label mapping 正確。
2. 跑基準訓練，記錄每個 epoch 的 pearson / accuracy。
3. 改變 loss 權重（例如 0.7/0.3, 0.5/0.5）觀察任務干擾。
4. 比較不同 batch size / lr 對 combined score 的影響。
5. 用最佳模型做 test，整理 failure case。

## 更深入可做

- Dynamic loss weighting（uncertainty weighting / GradNorm）。
- 增加 calibration 或 per-class F1 指標。
- 補上可追蹤的 config + experiment logging。

