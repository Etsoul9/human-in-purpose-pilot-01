# Project Status

## Current status

**Public Draft v0.1.1 — Open for Review, Not Yet Recruiting Participants.**

## Public name

**Human-in-Purpose / Камертон — Pilot 01**

## Term

**HPP = Human-in-Purpose Protocol.**

A proposed engineering and research framework for restricting AI actions to confirmed human intent, bounded delegation, explicit authorization, stop rights, and post-action traceability.

**HPP = Human-in-Purpose Protocol.**

Предлагаемый инженерно-исследовательский контур, который ограничивает действия ИИ явно подтверждённым человеческим намерением, границами делегирования, одноразовым подтверждением, правом остановки и последейственным следом.

## Language policy / Языковая политика

This repository is intentionally bilingual.

- **English** is used for precise technical, legal, and research-review terms.
- **Russian** preserves the original methodological and project context.
- Key concepts are repeated in both languages where needed.
- If a translation seems inaccurate or ambiguous, please open an issue. Do not assume full equivalence.

Этот репозиторий двуязычный.

- **Английский** используется для точных технических, юридических и исследовательских формулировок.
- **Русский** сохраняет исходный методологический и проектный контекст.
- Ключевые понятия дублируются там, где это важно для понимания.
- Если перевод кажется неточным или двусмысленным, пожалуйста, откройте Issue. Не предполагается полная эквивалентность формулировок.

## What is open for review

- research question;
- protocol draft;
- pilot design draft;
- mismatch taxonomy;
- draft scoring rubric, explicitly marked as non-final;
- privacy notes;
- security boundaries;
- invitation for technical, methodological, and premise critique.

## What is not ready

- participant recruitment;
- informed consent procedure;
- private data collection channel;
- tested engineering core;
- claim of effectiveness;
- claim of security;
- commercial product;
- SDK;
- certification;
- platform.

## Engineering core status

Engineering core: implementation under review; rc3.1 candidate patch not yet verified.

The repository may contain proposed code, schemas, tests, or design notes for the engineering core. These are not a verified release and must not be treated as a proven security mechanism.

Known issues discussed during internal review are documented as open engineering concerns, not as completed fixes.

## Research hypothesis status

The research hypothesis is:

> Does pre-formulating human goal, boundaries, and enoughness help a person notice divergence between their own intent and an AI-proposed action?

This is not yet tested with participants.

## Current methodological baseline

- A: ordinary approval;
- B: protected approval;
- C: protected approval + Intent Contract.

Open methodological question:

- Should condition B+ be added: protected approval + read-only task summary?

This is not finalized. It is an open question for HCI / UX research reviewers.

## Primary observable

The main observable is:

```text
detected_mismatch
