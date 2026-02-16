# Assignment 1: Word Analogy

## Objective

Build and evaluate embedding-based analogy solvers on the Google analogy benchmark, then train a custom Word2Vec model on sampled Wikipedia data.

## Deliverables

- `word_analogy_pipeline.py`: end-to-end Colab-style workflow
- `requirements.txt`: environment dependencies
- `report.docx`: assignment report

## Pipeline Architecture

1. Parse `questions-words.txt` into a structured dataframe (`semantic` vs `syntactic` categories).
2. Evaluate a pretrained embedding baseline (`glove-wiki-gigaword-100`).
3. Train a custom Word2Vec model with memory-aware preprocessing and vocabulary filtering.
4. Compare analogy performance by category and subcategory.
5. Visualize embedding neighborhoods with t-SNE.

## Key Engineering Choices

- Memory-aware corpus processing with frequency thresholds and callback logging.
- Controlled random sampling for reproducibility.
- OOV-aware analogy prediction flow to avoid noisy false positives.

## How to Run

Because this script is notebook-exported, the easiest route is Colab/Jupyter execution.

For local execution, expected refactors:

- Replace `!` shell commands with `subprocess` or setup scripts.
- Remove hardcoded Colab-specific paths and `drive.mount`.
- Split long script into modules (`preprocess`, `train`, `evaluate`, `visualize`).

## Suggested Production Hardening

- Add `argparse` for data/model/output paths.
- Emit metrics as JSON for CI-friendly regression checks.
- Add unit tests for tokenizer/preprocess/analogy scoring helpers.

