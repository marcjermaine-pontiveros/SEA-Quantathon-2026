# Provenance & Attribution

**Vendored third-party code — not authored by Team KTLJ.** Included as a runnable reference.

- **Upstream repository:** https://github.com/merlinquantum/reproduced_papers
- **Path:** `papers/photonic_QCNN`
- **Commit pinned:** `77023a3398b3c98486eb65e035e16dba06696740`
- **License:** MIT © 2026 Quandela (see `LICENSE` in this folder — preserved as required)

## What it is
A MerLin reproduction of **Monbroussou et al., "Photonic QCNN with Adaptive State Injection"**
([arXiv:2504.20989](https://arxiv.org/abs/2504.20989)) — the photonic quantum convolutional neural network our
work builds on. Use as a reference implementation; do **not** present it as our own work.

## Dependency
Like `distributed_qml_cc`, this folder's `lib/__init__.py` imports the shared **`runtime_lib`** package via a
`sys.path` hack (`parents[2]`). It is vendored alongside at **`../runtime_lib`** (`external/runtime_lib`, same
MIT repo, identical copy). Don't move either folder independently.

## Run
```bash
pip install -r requirements.txt          # tested elsewhere on merlinquantum>=0.3,<0.4
jupyter notebook notebook.ipynb
```
`results/` holds precomputed reference outputs. (If you hit a `MeasurementStrategy`/version error, pin
`merlinquantum>=0.3,<0.4` — same fix as `distributed_qml_cc`.)
