# Provenance & Attribution

**Vendored third-party code — not authored by Team KTLJ.** Included as a runnable reference.

- **Upstream repository:** https://github.com/merlinquantum/reproduced_papers
- **Path:** `papers/DQNN`
- **Commit pinned:** `77023a3398b3c98486eb65e035e16dba06696740`
- **License:** MIT © 2026 Quandela (see `LICENSE` in this folder — preserved as required)

## What it is
A MerLin reproduction of **Chen et al. (2025), "Distributed Quantum Neural Networks on Distributed Photonic
Quantum Computing"** ([arXiv:2505.08474](https://arxiv.org/abs/2505.08474)). It bundles a small `lib/torchmps`
(matrix-product-state) library. Use as a reference; do **not** present it as our own work.

## ⚠️ Run caveat (different from the other vendored folders)
This notebook (`dqnn.ipynb`) is **not** flat-runnable from `external/DQNN`. It uses repo-root-style imports:

```python
REPO_ROOT = Path.cwd().resolve().parents[1]      # expects the dir that contains papers/
sys.path.insert(0, str(REPO_ROOT))
from papers.DQNN.lib.model import ...             # hard-coded "papers.DQNN." package path
```

Flattened into `external/DQNN`, those `papers.DQNN.*` imports won't resolve. To run it, pick one:
- **Easiest:** run it from a clone of the upstream repo (`…/reproduced_papers/papers/DQNN/dqnn.ipynb`), where the
  `papers/DQNN/` layout exists.
- **Or adapt (your own copy):** in the setup cell, drop the `papers.DQNN.` prefixes (e.g.
  `from lib.model import ...`, `from utils.utils import ...`) and run with `external/DQNN` as the working dir.
  Do this in a *team-owned* copy, not by editing this vendored notebook.

It does **not** use `runtime_lib`.

## Run (after resolving the import layout above)
```bash
pip install -r requirements.txt
jupyter notebook dqnn.ipynb
```
`results/` holds precomputed reference outputs.
