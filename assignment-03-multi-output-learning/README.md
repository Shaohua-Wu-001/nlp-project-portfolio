# Assignment 3: Multi-output Learning

## Objective

Train a single BERT backbone to solve two tasks jointly on SemEval 2014 Task 1:

- Regression: semantic relatedness score
- Classification: entailment judgment

## Deliverables

- `multi_output_bert.py`: full training/validation/test workflow
- `requirements.txt`: dependency spec
- `report.docx`: assignment report
- `specification.pdf`: assignment spec

## Architecture

- Backbone: `bert-base-uncased`
- Shared pooled representation (`pooler_output`)
- Task heads:
  - Regression head (`Linear -> 1`)
  - Classification head (`Linear -> 3`)
- Loss: `MSELoss + CrossEntropyLoss` (equal weighting)

## Training Setup (from source)

- `lr=4e-5`
- `epochs=15`
- `train_batch_size=32`
- `validation_batch_size=32`
- Best checkpoint selected by `pearson + accuracy`

## Evaluation

- Regression metric: Pearson correlation
- Classification metric: Accuracy
- Combined score: `pearson + accuracy`

## Engineering Notes

- Joint optimization encourages representation sharing but can cause task interference.
- Loss balancing is currently static; dynamic weighting (e.g., uncertainty weighting) is a high-value improvement.
- Gradient clipping and checkpointing are already in place for stable training.

## Suggested Production Hardening

- Add experiment config files (YAML/TOML) for hyperparameter sweeps.
- Persist full evaluation artifacts (confusion matrix, residual plots, per-class breakdown).
- Add mixed-precision training for faster iteration.

