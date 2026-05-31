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

## Requirements
- General requirements as per .toml. 
- **Generation** requires a GPU with ≥20 GB VRAM (per 7–8B model), Hugging Face auth.
- Everything else: CPU is sufficient, you can even use our precomputed LAS/TPS tables.

---

## Getting started
- * Use the scripts directly, with the commands provided in COMMANDS.md.

---

## Licence

- **Code** (`src/`, `scripts/`): MIT No Attribution (MIT-0). See [`LICENSE`](./LICENSE). Use it freely, no attribution required.
- **Data and documentation** (`data/`, `*.md` files): CC0 1.0 Universal (public domain dedication). See [`LICENSE-DATA`](./LICENSE-DATA).

Note: the underlying PubMed abstracts used as prompts are included for research; the CC0 dedication covers only our derivatives (cleaned generations, POS tags, LAS/TPS tables, scripts), and the source abstract texts remain under their respective terms.

---

The included paper PDF remains under its own terms (CC BY 4.0; LREC 2026, ACL Anthology), separate from the code and data licences above.

## AI Assistance
- Programming included partial AI assistance (GPT-5 and GitHub Copilot).
- Repository polished with Claude Code.

---
