# Scalable Photonic QCNN

**Team KTLJ_Quantum** · QC4SG 2026 — Quantum Hackathon in Vietnam · Track: **Economy & Technology** · Quandela MerLin

**Members:** Duc-Kha Vu · Minh Tam Nguyen · Marc Jermaine Pontiveros · Lê Quốc Long

**Mentors:** Samuel Horsch (Quandela — Technical) · Rossy Nhung Nguyen (VNQuantum — Business)

---

## Repository structure

```
team-asean-quantathon/
├── README.md                  ← you are here
└── external/                  ← vendored references (Quandela, MIT) — see each folder's SOURCE.md
    ├── distributed_qml_cc/    ← Hwang et al. 2024 — distributed QML via classical communication
    ├── photonic_QCNN/         ← Monbroussou et al. — photonic QCNN with adaptive state injection
    ├── DQNN/                  ← Chen et al. 2025 — distributed QNN on photonic QC
    └── runtime_lib/           ← shared dependency for the above
```

The team's own content (notebook, etc.) will be added once we decide what to push.

## Reference reproductions — `external/`

Runnable MerLin reproductions from Quandela's
[`reproduced_papers`](https://github.com/merlinquantum/reproduced_papers). **Not our work** — MIT © 2026
Quandela; each folder keeps its `LICENSE` and a `SOURCE.md` with the upstream URL and pinned commit.

| Folder | Paper | arXiv |
|---|---|---|
| `distributed_qml_cc` | Hwang et al. (2024) — Distributed QML via classical communication | [2408.16327](https://arxiv.org/abs/2408.16327) |
| `photonic_QCNN` | Monbroussou et al. — Photonic QCNN with adaptive state injection | [2504.20989](https://arxiv.org/abs/2504.20989) |
| `DQNN` | Chen et al. (2025) — Distributed QNN on distributed photonic QC | [2505.08474](https://arxiv.org/abs/2505.08474) |

**Running them** (tested on `merlinquantum==0.3.2`, `torch==2.10`):
```bash
cd external/<folder>
pip install -r requirements.txt
jupyter notebook *.ipynb
```
- `distributed_qml_cc` and `photonic_QCNN` share `external/runtime_lib` (auto-resolved). Pin
  `merlinquantum>=0.3,<0.4` if you hit a `MeasurementStrategy` error.
- `DQNN` uses repo-root-style imports and isn't flat-runnable as-is — see `external/DQNN/SOURCE.md`.

## License

Team-authored content: TBD (suggest MIT). Vendored code under `external/` retains its own upstream license.
