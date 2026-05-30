# lhf-lex -- Lexical Alignment & Preference-Stage Shifts (LAS/TPS)
_Companion code for the paper: **Fully Automated Identification of Lexical Alignment and Preference-Stage Shifts in Large Language Models**._

**Paper:** [lexical_alignment_shifts.pdf](./lexical_alignment_shifts.pdf)

**Authors:** Thomas Stephan Juzek (tjuzek@fsu.edu), Xiaoyang Ming (xm24b@fsu.edu), Jose A. Hernandez (jah22q@fsu.edu) — Florida State University

[Commands](./COMMANDS.md)

---

## Overview
We provide an end-to-end, **deterministic** pipeline to quantify lexical alignment (LAS) and preference-stage shifts (TPS) in model continuations:
**prompts → generation (Base/Instruct) → deletion-only cleaning → POS → LAS/TPS discover & eval**.

- **Purpose:** test whether preference tuning causally shifts lexical choice distributions.
- **Outputs:** word-level weights, sentence/document/corpus-level scores, and batch scripts for model families.
- **Repro path:** fixed decoding; deletion-only cleaning; UD POS → CoNLL-U.

The paper's two headline figures are reproduced in [`out/figures/`](./out/figures/): `clas_barplot.png` (cLAS by model family) and `ctps_ratios.png` (cTPS ratios, base vs instruct).

---

## Requirements
- General requirements as per .toml. 
- **Generation** requires a GPU with ≥20 GB VRAM (per 7–8B model), Hugging Face auth.
- Everything else: CPU is sufficient, you can even use our precomputed LAS/TPS tables.

---

## Getting started
- * Use the scripts directly, with the commands provided in COMMANDS.md.

---

## AI usage
- Programming included partial AI assistance (GPT-5 and GitHub Copilot).

---

## License

The **code** in this repository (`src/`, `scripts/`) is licensed under **GPL-3.0-or-later** — see [`LICENSE`](./LICENSE).

The **data and documentation** (`data/`, `*.md` files) are licensed under **CC-BY-SA-4.0** — see [`LICENSE-DATA`](./LICENSE-DATA).

Note: the underlying PubMed abstracts used as prompts are works of the U.S. federal government and are in the public domain; any licence on this repository covers only our derivatives (cleaned generations, POS tags, LAS/TPS tables, scripts).

---

## Citation

If you use this code or data, a citation is appreciated (though not required; see the licence).

```bibtex
@inproceedings{juzek-etal-2026-fully,
  title     = {Fully Automated Identification of Lexical Alignment and Preference-Stage Shifts in Large Language Models},
  author    = {Juzek, Thomas Stephan and Ming, Xiaoyang and Hernandez, Jose A.},
  booktitle = {Proceedings of the Fifteenth Language Resources and Evaluation Conference (LREC 2026)},
  publisher = {European Language Resources Association (ELRA)},
  year      = {2026},
  pages     = {6116--6131},
  doi       = {10.63317/4ut7ammh7z3h}
}
```
