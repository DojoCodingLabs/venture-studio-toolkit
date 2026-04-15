# Changelog

All notable changes to `venture-studio-toolkit` documented in this file. Format follows
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/) + [Semantic Versioning](https://semver.org/).

## [1.0.0] — 2026-04-14

### Added — Complete initial scope (21 skills + 2 reference docs)

**Scaffolding**:
- Plugin manifest (`.claude-plugin/plugin.json`)
- License (Business Source License 1.1)
- README with full ecosystem context
- `.gitignore`

**Core skills (both modes — 10)**:
- `structure-decision` — 6 corporate structure patterns (Skip-CR, Single-LLC multi-brand, Delaware Tostada, Cayman Sandwich, Delaware C-Corp, Multi-LLC+Holding) with decision tree + migration roadmap + 3 canonical cases
- `structure-evolution-roadmap` — 6 migration routes with specific triggers (ARR, term sheet, geography, exit)
- `jurisdiction-matrix` (reference doc) — 16 jurisdictions across 4 families (LATAM 8 + US 3 + Offshore 3 + EU 2)
- `accelerator-launchpad` — catalog of 12+ external accelerators with fit-scoring algorithm + CIHUBS-style meta-broker
- `three-horizons` — Lean Enterprise cap. 2 portfolio allocation (H1/H2/H3) + 70/20/10 framework
- `explore-exploit` — Lean Enterprise cap. 2 Table 2-1 categorization with management implications
- `innovation-scorecard` — Lean Enterprise cap. 5 Figure 5-2 dashboard + AARRR cohort integration
- `cost-of-delay-cd3` — Lean Enterprise cap. 8 economic prioritization (CD / Duration) + power-law observation
- `sweat-equity-agreement` — vesting + cliff + 83(b) + clawback + FAST extension
- `improvement-kata` — Mike Rother's 5 daily questions + Target Condition + PDCA

**Studio mode skills (9)**:
- `studio-thesis` — Govclab 37-word template + 3-version iteration + validation exercise
- `studio-focus` — Stage × Geography × Industry triangulation (Govclab 5-step)
- `secret-sauce` — 6-metric ranking system (Govclab)
- `studio-archetype-selector` — In-house / External Partnership / Hybrid decision
- `vertical-charter` — mission/scope/success per vertical + Linear integration
- `shared-services-ledger` — transfer pricing compliance + allocation methodology
- `venture-spin-out-playbook` — 7-layer spin-out mechanics (IP, contracts, team, cap table)
- `attached-fund-structure` — Management Co + GP + LP layered per Govclab
- `mensarius-oath-adoption` — optional ethical code for fund managers

**Founder mode skills (3)**:
- `liability-contagion-analysis` — 8 risk dimensions + compatibility matrix
- `cap-table-per-venture` — cap table management with dilution scenarios + SAFE conversion modeling
- `when-to-become-studio` — 9-signal readiness assessment + transition roadmap

**Reference documents**:
- `dojocoding-labs-canonical-thesis.md` — canonical test case with 3 iterations

### Legal disclaimers

All skills touching legal/fiscal domains include explicit disclaimers:
- `structure-decision`, `structure-evolution-roadmap`, `jurisdiction-matrix`
- `sweat-equity-agreement`, `cap-table-per-venture`
- `attached-fund-structure`, `venture-spin-out-playbook`
- `shared-services-ledger`, `liability-contagion-analysis`

These skills generate structured preparation material, NOT legal advice. Users must
validate with specialized lawyers before acting on outputs.

### Based on

- *Lean Enterprise* (Humble, Molesky, O'Reilly — O'Reilly 2015) — chapters 2, 5, 6, 8, 13
- *Toyota Kata* (Mike Rother — McGraw-Hill 2010)
- *Principles of Product Development Flow* (Don Reinertsen — 2009)
- Govclab / VC Lab — venture studio formation + fund formation methodologies
- Latitud / Manzano Law / Carta / Cooley / ECGI — LATAM corporate structures
- Cake Equity / Orchestra / ClearTax — sweat equity + vesting
- CIHUBS (Costa Rica) — accelerator meta-broker pattern
- Dave McClure — Pirate Metrics (AARRR)

### Known limitations

- Bilingual output (es/en) framework defined in README; implementation per-skill pending
  actual dog-fooding (users will validate)
- No GitHub CI/CD yet (Greptile install pending DOJ-3192)
- No MCP integration (no external tool calls from skills yet)
- `vertical-charter` Linear integration is manual — no direct Linear MCP reads yet

### Stability note

v1.0.0 marks **feature-complete scope per the original SPIKE DOJ-3190 plan**, but is NOT
battle-tested. Breaking changes possible in v1.x as dog-fooding reveals issues. v2.0
will consolidate lessons learned.

## [0.1.0] — 2026-04-14 (superseded by 1.0.0 same day)

Initial scaffold — see commits for details. This version was the "scaffold + first 3
skills" milestone from SPIKE. Consolidated into 1.0.0 upon completion of the full scope.
