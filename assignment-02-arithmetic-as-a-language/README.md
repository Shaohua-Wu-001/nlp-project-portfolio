# Assignment 2: Arithmetic as a Language

## Objective

Formulate arithmetic expression solving as a character-level sequence modeling task and train a recurrent model to generate the answer sequence after `=`.

## Deliverables

- `arithmetic_sequence_model.py`: dataset prep, model definition, training loop, validation loop
- `requirements.txt`: dependencies
- `report.docx`: assignment report

## Modeling Strategy

- Character vocabulary with special tokens: `<pad>`, `<eos>`
- Dual-layer LSTM decoder-style architecture (`Embedding -> LSTM -> LSTM -> MLP`)
- Teacher-forced sequence training with cross-entropy loss on padded labels
- Auto-regressive generation at evaluation time

## Training Configuration (from source)

- `batch_size=128`
- `epochs=10`
- `embed_dim=512`
- `hidden_dim=512`
- `lr=0.00075`
- Gradient clipping via `clip_grad_value_`

## Evaluation Pattern

Validation checks exact answer matching after parsing generated sequence tail (post-`=`).

## Engineering Observations

- This framing is simple and effective for deterministic symbolic tasks.
- The design is sensitive to tokenization and output formatting consistency.
- For scaling, a transformer decoder and curriculum by expression complexity are natural next upgrades.

## Suggested Production Hardening

- Separate data pipeline and model training into modules.
- Add deterministic seeding across dataloader/model/runtime.
- Track per-length and per-operator error slices for failure analysis.

