# Security Boundaries

## Verification status

The engineering core described in this repository is **not yet verified**.

Internal review identified several implementation concerns, including:

- stop / resume behavior and epoch binding;
- action authorization lifecycle and single-use enforcement;
- payload integrity checks (recomputation from actual data, not stored hashes alone);
- contract schema strictness;
- audit completeness (every denial logged);
- mock execution boundary;
- race between stop and execute.

These are documented as **open engineering risks and proposed remediations**. They are **not** confirmed fixes until tests are written, executed, and independently reviewed.

The rc3.1 work exists as a **candidate patch**, not as a verified release.

## What this is

This is an experimental research draft and mock-only engineering prototype.

It is **not**:

- production security software;
- a certified safety mechanism;
- a replacement for security audit;
- a replacement for legal or compliance review;
- a guarantee of human agency;
- a biometric verification system.

## MVP threat model

Assumptions:

- the Python process running the core is trusted in the test environment;
- the SQLite database is trusted in the test environment;
- LLM output is untrusted;
- user free-text input is untrusted until validated;
- external real-world actions are disabled;
- only mock tools are allowed.

## Important limitation

If an attacker has full control over the trusted database or the gateway process, local hashes and triggers do **not** provide independent guarantees.

For MVP this limitation is explicitly accepted. Production use would require external append-only transparency logs, signed checkpoints, separated processes, and possibly hardware-backed attestation. None of that is present here.

## What the engineering core aims to enforce

**If implemented and tested correctly**, the contour is designed so that:

1. no confirmed contract → no execution;
2. no valid single-use authorization → no execution;
3. LLM cannot modify contract;
4. denied tool cannot execute;
5. payload swap after confirmation is denied;
6. authorization reuse is denied;
7. stop blocks future actions;
8. already executed action is not falsely claimed as cancelled;
9. expired TTL blocks execution;
10. hash mismatch blocks execution.

These are design goals under test, not verified properties.

## What it does not guarantee

It does **not** guarantee:

- that the user psychologically understood the action;
- that the user was attentive;
- that the user did not confirm mechanically;
- that semantic content is safe or appropriate;
- that external systems support cancellation after commit;
- that the system is protected from full compromise of the trusted DB or gateway code;
- that Intent Contract improves human control.

The last point is the subject of the experiment, not an assumption of the architecture.

## Relation to the research hypothesis

Engineering verification and research validation are separate.

- Passing adversarial tests would support the **engineering hypothesis** only.
- It would **not** prove the **research hypothesis** (that explicit intent helps users notice divergence).
- A working guardrail can still be useless UX. That is exactly what the pilot is meant to test.

---

## Кратко по-русски

Инженерное ядро в этом репозитории **не проверено**. Внутренний ревью выявил несколько открытых проблем (stop/resume, жизненный цикл авторизации, пересчёт хешей из фактических данных, строгость схемы контракта, полнота аудита, граница mock-исполнения, гонка stop/execute). Они задокументированы как открытые риски и Proposed remediations, а не как исправленные гарантии. Работа rc3.1 существует как **candidate patch**, не как подтверждённый релиз.

Это экспериментальный черновик и mock-only прототип. Это не production-безопасность, не сертификация, не замена security/legal/compliance, не гарантия человеческой агентности, не биометрия.

В MVP-модели угроз доверяются процесс Python и SQLite в тестовой среде; LLM и пользовательский ввод до валидации — недоверенные; реальные внешние действия отключены; разрешены только mock-инструменты.

Важное ограничение: если атакующий получает полный контроль над доверенной БД или кодом Gateway, локальные хеши и триггеры не дают независимой гарантии. Для MVP это явно принято.

При корректной реализации и тестировании контур *стремится* обеспечить 10 свойств (нет контракта — нет исполнения; нет валидной одноразовой авторизации — нет исполнения; LLM не меняет контракт; запрещённый инструмент не исполняется; подмена payload после подтверждения блокируется; повторное использование авторизации блокируется; stop блокирует будущие действия; уже исполненное не объявляется отменённым ложно; истёкший TTL блокирует исполнение; несоответствие хеша блокирует исполнение). Это цели под тестом, а не проверенные свойства.

Контур **не** гарантирует, что человек понял действие, был внимателен, не подтвердил механически, что семантика текста безопасна, что внешние системы поддержат отмену после commit, что система защищена от полной компрометации, и что Intent Contract улучшает контроль. Последнее — предмет эксперимента, а не допущение архитектуры.

Проверка инженерии и проверка исследования — разные вещи. Зелёные adversarial-тесты поддержат только инженерную гипотезу. Они не докажут исследовательскую. Работающий guardrail всё ещё может быть бесполезным UX — именно это и должен проверить пилот.
