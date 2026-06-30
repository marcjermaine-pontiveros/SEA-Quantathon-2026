# Provenance & Attribution

This folder is **vendored third-party code**, not authored by Team KTLJ. It is included as a runnable
reference because our Quandela technical mentor (Samuel Horsch) shared it as the canonical reproduction of the
paper our architecture builds on.

- **Upstream repository:** https://github.com/jsenellart/reproduced_papers
- **Branch:** `distributed_qml_cc`
- **Path:** `papers/distributed_qml_cc`
- **Commit pinned:** `75a3a852fdb5bbac3d7b9dfea24f969a6676171f`
- **License:** MIT © 2026 Quandela (see `LICENSE` in this folder — preserved as required)
- **Author:** Jean Senellart (Quandela) et al.

## What it is
A reduced, runnable MerLin reproduction of **Hwang et al. (2024), "Distributed quantum machine learning via
classical communication"** ([arXiv:2408.16327](https://arxiv.org/abs/2408.16327)) — the paper underpinning our
project. It benchmarks four schemes that map directly onto our distribution spectrum:

| Upstream scheme | Our spectrum regime |
|---|---|
| QC-DQML (quantum-communication feedforward) | **Q** — quantum communication (reference only) |
| CC-DQML (classical-communication feedforward) | **B** — classical communication (our DP-QCNN) |
| NC-DQML (no inter-QPU operations) | **C-adjacent** — no communication |
| non-DQML (single QPU) | **A** — monolithic reference |

## How we use it
Reference + comparison baseline for **Regime B**. Our contribution is the *photonic* + *spectrum trade-off*
extension, not this code. Do **not** present this as our own work; cite it as Quandela's reproduction.

## Dependencies (also vendored)
This folder's `lib/__init__.py` imports the upstream repo's shared package **`runtime_lib`** (same repo, same
MIT license). It is vendored alongside this folder at **`../runtime_lib`** (i.e. `external/runtime_lib`). The
folder's `lib/__init__.py` adds its parent (`external/`) to `sys.path`, so `from runtime_lib import config`
resolves to that copy. Don't move either folder independently.

## Run
```bash
pip install -r requirements.txt   # torch, numpy, matplotlib, merlinquantum, pytest
# from this folder:
jupyter notebook notebook.ipynb   # or open in Colab
```
See `README.md` (upstream) for full instructions; `results/` holds precomputed reference outputs.
