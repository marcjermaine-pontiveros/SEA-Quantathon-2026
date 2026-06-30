# Scalable Photonic QCNN

**Team KTLJ_Quantum** · QC4SG 2026 — Quantum Hackathon in Vietnam · Track: **Economy & Technology** · Quandela MerLin

**Members:** Duc-Kha Vu · Minh Tam Nguyen · Marc Jermaine Pontiveros · Lê Quốc Long

**Mentors:** Samuel Horsch (Quandela — Technical) · Rossy Nhung Nguyen (VNQuantum — Business)

---

## Repository structure

```
team-asean-quantathon/
├── README.md                     ← you are here
└── external/
    └── distributed_qml_cc/       ← VENDORED reference (Quandela, MIT) — see its SOURCE.md
```

The team's own content (notebook, etc.) will be added once we decide what to push. 

## Reference baseline — `external/distributed_qml_cc/`

A runnable MerLin reproduction of **Hwang et al. (2024), "Distributed quantum machine learning via classical
communication"** ([arXiv:2408.16327](https://arxiv.org/abs/2408.16327)) — the paper our architecture builds on.
It implements our exact spectrum in MerLin (nc / cc / qc = no-comm / classical-comm / quantum-comm).

- **Not our work** — MIT © 2026 Quandela; author Jean Senellart et al. See `external/distributed_qml_cc/SOURCE.md`
  for provenance (upstream URL, branch, pinned commit) and `LICENSE`.

```bash
cd external/distributed_qml_cc
pip install -r requirements.txt
jupyter notebook notebook.ipynb
```

Note: Tested on merlinquantum==0.3.2 and torch==2.10

## License

Team-authored content: TBD (suggest MIT). Vendored code under `external/` retains its own upstream license.
