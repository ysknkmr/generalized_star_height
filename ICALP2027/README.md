# ICALP 2027 Track B: An Infinite Star-Height Hierarchy for KA with Complement

Source: `../rsub_star_height_hierarchy_summary_20261007.md`.
Template/macros copied from `../CSL2025` (LIPIcs v2021); old CSL sections are kept in `old/` (not built).

Build: `make` (latexmk), `make check` (fails on any warning/overfull/undefined knowledge), `make arxiv` (source tarball `arxiv.tar.gz` with `main.bbl`).
Set `\setboolean{final}{true}` in `main.tex` for camera-ready (no line numbers / knowledge colors).

| path | content |
|---|---|
| `main.tex` | driver (LIPIcs, `thm-restate`) |
| `abstract.tex` | abstract (no custom macros / kl) |
| `header/` | packages, palette, knowledge config, macros (`\knowledgenewrobustcmd` + `\cmdkl`) |
| `kl/` | knowledge definitions (`kl-paper.tex`, abbreviations) |
| `sec/` | sections and appendices |
| `fig/` | figure (chain model) and table (invariants) |

Section ↔ summary: §2 = summary §1, §8 (locality); §3 = §2–4 (witness now uses z = same-phase window relation); §4 = §5–6 (unified over Z and Z_N); §5 = §7. REL part: finite cyclic models Z_N × [m] (not in the summary).

Currently non-anonymous (arXiv version). For a double-blind ICALP submission add the `anonymous` option.
TODO: page limit check, DOIs of new bib entries.
