# Legacy scripts (unused)

These three files were inherited from the upstream Gemma pipeline
(`kelkarI/sycophancy-gemma`) when this repo was forked for the Qwen 3 32B
replication. They still reference `gemma-2-27b/` paths in
`lu-christina/assistant-axis-vectors` and are **not** part of the active
Qwen pipeline. They are kept here only for provenance.

- `00_setup.py` — Gemma-specific sanity-check script; loads gemma-2-27b-it
  and runs a 5-row probe.
- `fetch_external.py` — CLI helper that fetches the Gemma-flavoured role
  vectors from the HF dataset subdir `gemma-2-27b/`.
- `01_prepare_steering_vectors.py` — the Gemma vector-preparation pipeline.
  Superseded on Qwen by `scripts/build_vectors_from_official.py` (loads
  the `qwen-3-32b/` subdir of the same HF dataset at layer 32) and
  `scripts/extract_all_vectors.py --skip-personas` (CAA extraction on
  Qwen 3 32B).

Nothing in the live pipeline imports from this directory.
