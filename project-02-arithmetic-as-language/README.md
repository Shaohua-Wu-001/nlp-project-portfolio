# Project 02: Arithmetic as a Language

## Overview

This project frames arithmetic computation as a character-level sequence generation task. The model reads an arithmetic expression up to the `=` sign and autoregressively generates the result character by character until producing an `<eos>` token.

## Architecture

```
Input: "123+456="  →  Embedding  →  LSTM  →  LSTM  →  MLP  →  Output: "579<eos>"
```

- **Vocabulary**: All digits, operators, `=`, `<pad>`, `<eos>`
- **Encoder**: Character embedding layer
- **Decoder**: Stacked 2-layer LSTM with MLP output head
- **Training**: Cross-entropy loss with gradient clipping
- **Inference**: Autoregressive decoding with greedy search

## Usage

```bash
pip install -r requirements.txt
python arithmetic_sequence_model.py
```

## Files

| File | Description |
|------|-------------|
| `arithmetic_sequence_model.py` | Model definition, training loop, and evaluation |
| `requirements.txt` | Python dependencies |
| `report.docx` | Detailed analysis of model behavior and failure cases |

## Key Results

- Validation accuracy across varying expression lengths and operator types
- Error analysis on failure cases: long expressions, negative results, chained operations
- Convergence comparison across different `embed_dim`, `hidden_dim`, and learning rate configurations
