# Project 03: Multi-Output Learning with BERT

## Overview

This project implements multi-task learning using a shared BERT backbone with two output heads: a regression head for semantic textual similarity (relatedness scoring) and a classification head for natural language inference (entailment judgment).

## Architecture

```
                    ┌─── Regression Head ──→ Relatedness Score (Pearson)
Input → BERT ──────┤
                    └─── Classification Head ──→ Entailment Label (Accuracy)
```

- **Shared Encoder**: Pretrained BERT with fine-tuning
- **Loss Function**: `L = MSE(regression) + CrossEntropy(classification)`
- **Checkpoint Selection**: Best combined score across both tasks

## Usage

```bash
pip install -r requirements.txt
python multi_output_bert.py
```

## Files

| File | Description |
|------|-------------|
| `multi_output_bert.py` | Multi-task model, training loop, evaluation |
| `requirements.txt` | Python dependencies |
| `specification.pdf` | Task specification and requirements |
| `report.docx` | Experimental results and analysis |

## Key Results

- Per-epoch Pearson correlation (regression) and accuracy (classification)
- Loss weight sensitivity analysis (e.g., 0.7/0.3 vs. 0.5/0.5) and task interference effects
- Impact of batch size and learning rate on combined score
