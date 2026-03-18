# lhf-lex -- Lexical Alignment & Preference-Stage Shifts (LAS/TPS)
_Companion code for the paper: **Fully Automated Identification of Lexical Alignment and Preference-Stage Shifts in Large Language Models**._

**Paper:** [lexical_alignment_shifts.pdf](./lexical_alignment_shifts.pdf)

[Commands](./COMMANDS.md)

---

## Overview
We provide an end-to-end, **deterministic** pipeline to quantify lexical alignment (LAS) and preference-stage shifts (TPS) in model continuations:
**prompts → generation (Base/Instruct) → deletion-only cleaning → POS → LAS/TPS discover & eval**.

- **Purpose:** test whether preference tuning causally shifts lexical choice distributions.
- **Outputs:** word-level weights, sentence/document/corpus-level scores, and batch scripts for model families.
- **Repro path:** fixed decoding; deletion-only cleaning; UD POS → CoNLL-U.

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
- Programming included partial AI assistance (GPT5 and GitHub Copilot).

---

## License

This repository is released under the **<tbd>** license.
