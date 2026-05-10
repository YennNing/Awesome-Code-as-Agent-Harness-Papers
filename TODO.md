# TODO — Release Checklist

This file tracks the remaining work before publishing the *Awesome Code as Agent Harness Papers* repository. Items are grouped by priority.

---

## 🔴 Blocking (Must Fix Before Public Release)

These are placeholders currently embedded in `README.md`. Search for `XXXX`, `TBD`, or `placeholder` to find them quickly.

### Survey-Dependent Placeholders (fill in once the arXiv preprint is posted)

| # | Location | Current | Replace With |
| --- | --- | --- | --- |
| 1 | `README.md` line 4 — arXiv badge | `[![arXiv](https://img.shields.io/badge/arXiv-XXXX.XXXXX-b31b1b.svg)](#)` | Real arXiv ID and link |
| 2 | `README.md` line 12 — "Based on the survey" tagline | `(arXiv link coming soon — placeholder)` | Real arXiv URL |
| 3 | `README.md` line 18 — News section | `**[TBD]** 🚀 We will release a comprehensive survey on ***Code as Agent Harness***. The arXiv preprint, slides, and project page links will be added here once available.` | Real release announcement with date + arXiv link |
| 4 | `README.md` lines 82-87 — BibTeX | `journal = {arXiv preprint arXiv:XXXX.XXXXX},  % TODO: replace once posted` | Real arXiv ID. Also verify the cite key `ning2026codeasharness` matches what the paper uses. |

### Author / Maintainer Info

| # | Location | Current | Replace With |
| --- | --- | --- | --- |
| 5 | `README.md` line 73 — Contributing section | `Email us at: *(placeholder — corresponding-author email goes here)*` | Real corresponding-author email(s) (Hanghang Tong / Jingrui He, per `main.tex`) |
| 6 | `CONTRIBUTING.md` last paragraph | Maintainer list is generic | Add named maintainers + emails |

### Repository Identity

| # | Location | Current | Notes |
| --- | --- | --- | --- |
| 7 | `README.md` lines 7-8 — Last Commit & Visitor badges | Hard-coded `YennNing/Awesome-Code-as-Agent-Harness-Papers` | Verify the final GitHub org/path before publishing. If the repo will live under a different account or use the underscored name (`Awesome-Code-as-Agent_Harness_Papers`), update both badge URLs. |

---

## 🟠 Important (Recommended Before Public Release)

### Lab-Mate Audit — Venue / arXiv Errors

A separate review pass is needed to fix mistakes introduced during the manual venue-tagging round. Known issues:

**Wrong venue tags (need correction):**
- `ChemCrow` — currently `Nature 2023`; should be `Nature Machine Intelligence 2024` (the arXiv preprint is 2023, but the formal Nature MI publication is 2024). ✅ Already fixed by me.
- `MathCoder` — currently `ICLR 2023`; should be `ICLR 2024`. ✅ Already fixed.
- `ResearchAgent` — currently `NAACL 2024`; should be `NAACL 2025`. ⚠️ Fix did not apply on this row — re-verify URL and re-apply.
- `SWE-bench` (the `arxiv.org/abs/2310.06770` row in **Code-Grounded Evaluation Environments** and **From Patch Generation to Software Lifecycle Participation**) — labeled `ICLR 2023`; should be `ICLR 2024` (and ideally switched to the OpenReview link).

**Wrong arXiv IDs (need verification — these PDFs do not match the cited papers):**
- `AutoSafeCoder` — uses `2402.04486`; correct ID is `2409.10737` ✅ Verified and fix reference.bib.
- `CodeCoR` — uses `2501.05678`; correct ID is `2501.07811` ✅ Verified and fix reference.bib.
- `Cogito` — uses `2501.03456`; correct ID is `2501.18653` ✅ Verified and fix reference.bib.
- `HyperAgent` — uses `2406.11915`; correct ID is `2409.16299` ✅ Verified and fix reference.bib.
- `Hallucination to Consensus (CANDOR)` — uses `2501.11223`; correct ID is `2506.02943` ✅ Verified and fix reference.bib.

### Remaining Bare-Year Rows

~155 paper rows still display only a bare year (e.g. `| 2025 |`) in the Year column. Most are recent 2025/2026 preprints that genuinely have no peer-reviewed venue yet, but some may have been accepted at venues that have not been searched for. Recommended:

- Re-scan the bare-year list every 1-2 months as venues announce new acceptances (ICLR / NeurIPS / ICML / ACL / etc.) and upgrade the tag + link.

### Section Cleanup / Deduplication

- Several papers (notably **SWE-bench**, **AgentCoder**, **AutoSafeCoder**, **MAGE**, **HyperAgent**, **MARCO**, **QualityFlow**, **CANDOR**, **SoA**, **Codepori**) appear in multiple sections. This is acceptable for an awesome list, but worth a final dedup decision: keep each paper in its most canonical section only, or accept duplicates.

---

## 🟡 Nice-to-Have

### Visuals
- `figs/overview.png` is the raw render from the LaTeX taxonomy figure. May want a GitHub-optimized version with better aspect ratio / readable text.

### Repo Engineering
- Add a CI job to detect broken links (e.g. `lychee` GitHub Action) once the repo is public.
- Add a CONTRIBUTING workflow / PR template aligned with the table format.

### Awesome Ecosystem
- After publishing, submit the repo to the main [awesome.re](https://awesome.re) list. The `[Awesome](https://awesome.re/badge.svg)` badge is currently aspirational.

### Discoverability
- Consider adding a "Citing Format" snippet showing the BibTeX for individual papers, not just the survey.
- Consider grouping papers within each subsection by year (newest first) for easier scanning.

---

## ✅ Already Done in This Repo

For reference, the following items have been completed:

- Repo skeleton (`LICENSE`, `CONTRIBUTING.md`, `.gitignore`, `figs/overview.png`)
- Initial paper inventory generated strictly from `reference.bib` (no hallucinated citations)
- `MISSING_URLS.md` resolved (all 98 papers originally lacking URLs in the bib have been searched on arXiv / proceedings sites and inserted into the README)
- "Year" column normalization — removed `arXiv` / `CoRR` / `Web/Blog` / `Preprints` prefixes (170+ rows)
- Venue tagging pass — upgraded ~40 rows from bare year to peer-reviewed venue (`ICLR/NeurIPS/ICML/ACL/EMNLP/ICSE/FSE/CoRL/ICRA/CVPR/Nature/Science/...`)
- Removed the **Agent Personalization (Recommender Systems)** section per editorial decision (TOC entry, section body, and intro mentions all cleaned up)
- Fixed long venue names (`VL/HCC`, `ICSME`, `FLLM`)
- Recovered a section that was truncated mid-row in a write operation (Scientific Discovery → Acknowledgements)

---

## 📋 Per-Bib-Entry TODO

The 15 cite keys that appear in the LaTeX source but have **no entry** in `reference.bib` (mostly Anthropic / OpenAI / Cursor engineering blogs) are listed at the bottom of `MISSING_URLS.md`. These need:

1. Proper bib entries added to `reference.bib`
2. URLs (most are public blog posts and should be easy to source)
3. Insertion into the README once they have valid entries

---

*Last updated: see `git log` for this file's history.*
