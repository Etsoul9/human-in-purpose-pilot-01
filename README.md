# Human-in-Purpose / Камертон — Pilot 01

**HPP = Human-in-Purpose Protocol.**

A proposed engineering and research framework for restricting AI actions to confirmed human intent, bounded delegation, explicit authorization, stop rights, and post-action traceability.

**HPP = Human-in-Purpose Protocol.**

Предлагаемый инженерно-исследовательский контур, который ограничивает действия ИИ явно подтверждённым человеческим намерением, границами делегирования, одноразовым подтверждением, правом остановки и последейственным следом.

---

**Public Draft v0.1.1**
**Status: Open for Review, Not Yet Recruiting Participants.**
**Engineering core: implementation under review; rc3.1 candidate patch not yet verified.**

English short summary:

> This is an open research pilot about human intent in AI-mediated actions.
> We are checking whether pre-formulating a person's goal, boundaries, and "enough" criterion helps them notice when an AI proposal diverges from their own intent.
> This is not a product, not a security guarantee, not therapy, and not a recruitment campaign yet.

---

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

---

## What this is

This is a research pilot.

Its output is knowledge, not a product.
Its success is measured in external critique, reproducible findings, and clearer experimental design, not in user acquisition.

Это исследовательский пилот.

Его результат — знание, а не продукт.
Его успех измеряется внешней критикой, воспроизводимыми находками и уточнением экспериментального дизайна, а не количеством пользователей.

---

## Проблема

ИИ всё чаще может действовать от имени человека:

- отправить сообщение;
- изменить данные;
- удалить файл;
- опубликовать текст;
- назначить встречу;
- запустить цепочку действий;
- подготовить документ, который затем уходит дальше.

Обычное подтверждение вида:

```text
Черновик готов. Отправить?
[Да] [Нет]
