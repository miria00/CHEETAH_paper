# CHEETAH

Source for the CHEETAH paper: hardware-software co-design of LLM inference
accelerators as a single certified optimization program.

CHEETAH replaces the sequential map-then-fuse-then-size pipeline with one
program that decides hardware sizing, tiling, fusion, time-indexed memory
residency, rematerialization, and the serving-regime decisions together, and
returns a certified bound alongside every design.

## Building

```
pdflatex neurips_2026 && bibtex neurips_2026 && pdflatex neurips_2026 && pdflatex neurips_2026
```

Main file: `neurips_2026.tex`. Section sources are `\input` from the top level
and from `update/`.

## Layout

- `neurips_2026.tex` main document and preamble
- `1-introduction.tex` ... `6-conclusion.tex` main-body sections
- `update/` sections added during revision (solver, batch sensitivity,
  discussion, RTL and physical-design validation, TCO)
- appendix sources: theory, LP formulation details, audits, blueprints,
  coefficient provenance, shape aggregation, master program
- `figs/` figures
- `ref.bib` bibliography
