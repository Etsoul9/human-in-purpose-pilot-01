# Changelog

All notable changes to this public review package are documented here.
This project follows a simple draft-versioning scheme. Newer versions are listed first.

Все заметные изменения этого публичного пакета ревью задокументированы здесь.
Более новые версии перечислены первыми.

---

## Public Draft v0.1.1 — editorial / process patch

Purpose: incorporate pre-publication critique without reopening the core concept.
Conceptual scope remains frozen pending external review.

### Changed

- Renamed engineering status from "rc3.1 hotfix" to **"rc3.1 candidate patch"** everywhere.
  Rationale: nothing was verified by executed tests, so "hotfix" implied a completed fix.
- Added explicit separation of **engineering hypothesis** and **research hypothesis** in README.
  Rationale: success of the engineering core must not be read as proof of the research claim.
- Added positive definition of the project: "a research pilot; output is knowledge, not a product."
- Added language policy: English for precise technical/legal/research terms, Russian for methodological context.
- Expanded HPP = Human-in-Purpose Protocol at the top of README and STATUS.

### Added

- **External review fallback** in STATUS: if fewer than 3 substantive critiques arrive in 4–6 weeks, run internal red-team review instead of waiting indefinitely.
- **Public critique channel** with low-barrier async review: one sharp sentence counts; no call required.
- **Maintainer response process** and **comment triage** rules in CONTRIBUTING.
- Invitation to critique the **seam** between engineering and research, and the **premise itself** (real pain vs friction tax).
- **Mismatch taxonomy** in PILOT_DESIGN: explicit boundary violation vs subtle goal divergence.
- **Draft scoring rubric** for `detected_mismatch`, explicitly marked DRAFT / NOT FINAL.
- **Open methodological question** about condition B+ (protected approval + read-only task summary).
- **Construct validity limit**: detected mismatch is not identical to human agency.
- **Intent text sensitivity** section in PRIVACY, because user-stated goals can reveal sensitive context.
- **Information controls** so condition C does not win merely by showing more text.
- Relationship-to-broader-project note: this pilot is a narrow slice, not the whole framework.

### Not changed

- Core research question and A/B/C baseline (B+ left as an open question, not a decision).
- Decision not to recruit participants yet.
- Decision not to claim the engineering core is verified.

---

## Public Draft v0.1 — initial public review package

First structured public package, separating documents from unverified code.

### Added

- README with problem framing and two hypotheses (initial form).
- STATUS with "Open for Review, Not Yet Recruiting Participants".
- PROTOCOL draft (minimal loop: Intent Contract → Proposal → Authorization → Stop/Execute → Echo).
- PILOT_DESIGN draft (conditions A/B/C, primary metric detected_mismatch, safety metric).
- PRIVACY notes (no participant data via public Issues).
- SECURITY_BOUNDARIES notes (mock-only, unverified core).
- CONTRIBUTING guide (critique, not endorsement).
- Issue templates for critique, technical review, methodology review, product scenario.
- Three opening Issues: technical risks, methodology, known limitations.

### Known at this stage

- Engineering core existed only as proposed changes, not as tested code.
- No scoring rubric for mismatch detection yet.
- No fallback for indefinite review waiting yet.
- Intent-text privacy risk not yet addressed.

---

## Pre-public internal iterations (summary)

Before v0.1 the project went through internal architecture rounds (HPP v0.1-rc2, rc3).
These identified real engineering concerns (hash recomputation, authentication of confirmation,
strict tool schemas, stop/resume semantics, audit completeness, mock execution).
They are recorded here only as provenance, not as verified results.
The rc3.1 work is referenced throughout as a **candidate patch**, not a release.
