# Case: ENG Core v0.1 — first application

Date: 2026-10-15 · Core: core/eng-core.md v0.1
Session: live, one host, one assistant instance.

## Conditions

Compress a private working prompt (~260 words, RU) into a public English
core. Constraints: remove private infrastructure references, replace
machine-specific commands, preserve verification and problem-plane logic.

## Applied

- Verification: every claim about repository state was checked against
  the live repo before recording (commits c17b5e9, 0505c25, 99bdc5e).
  One claim (Pages build failure) was withdrawn after contradicting
  evidence; the correction is kept in the record.
- Problem planes: work ran on the zero-purchase path — existing GitHub
  account, GitHub Pages, no new tooling or subscriptions.
- Commands: reduced from 9 symbols to 4 (`+`, `++`, `sum`, `run`) after
  a real ambiguity surfaced in testing: "`+start` — prefix or literal
  wording?" The answer ("literal") exposed that the symbol table mixed
  user-side and model-side tokens; the split was removed rather than
  documented around.

## Result

Core: 1056 bytes, ~180 words, 3 sections; ~1.4x compaction with
verification and planning logic preserved. Command surface: 4 tokens.

## Limitations

- Single application, single session; no repeat runs.
- `sum` and `run` are defined but not yet observed in use.
- Effect on model output quality unmeasured; single model, single host.
- Source prompt is private, so the comparison baseline is not reproducible
  by third parties.
