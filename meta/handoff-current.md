# meta/handoff-current.md
Текущий снимок передачи контекста.
Формат — по `meta/handoff-protocol.md` §7.
Обновлять перед паузой или сменой агента.

    HANDOFF PROTOCOL: v0.1
    PROJECT: karcas-dda
    REPOSITORY: https://github.com/shaenxxx-commits/karcas-dda
    CURRENT HEAD: [НЕИЗВЕСТНО — запросить git log -1 --oneline перед действиями]
    ACTIVE EXPERIMENT: нет
    STATUS: Active / наполнение каркаса
    LAST OPERATOR DECISION: D-20261012-01..03 (P0-исправления) + текущая серия наполнения
    MANDATORY FILES:
      - 00_ENTRY.md
      - INVARIANTS.md
      - CURRENT_STATE.md
      - DECISIONS.md
      - PROVENANCE.md
      - docs/KNOWLEDGE_STATES.md
      - meta/agent-rules.md
      - meta/handoff-protocol.md
      - records/README.md
    UNVERIFIED:
      - HEAD на момент последнего push (запросить перед действиями)
      - Применимость каркаса на реальном проекте — не проверялась
    OPEN QUESTIONS:
      - где остановиться в текущей серии наполнения (см. ниже)
    LAST RESPONSE NUMBER: MS 8

## Где мы сейчас

Идёт серия наполнения каркаса `karcas-dda` материалом, вынесенным из реальных проектов экосистемы (LAB, Envoy, MAIA).

## Что сделано в этой сессии

- P0-исправления по итогам трёх внешних аудитов (MS1–MS3): заполнены `CURRENT_STATE.md` и `PROVENANCE.md`, согласованы I2/I4 с двумерной моделью, ужесточён I8. Коммит `c7ff895`.
- Создан `meta/agent-rules.md` (правила работы LLM-агента, включая формат `MS N`, anti-patterns).
- Создан `meta/handoff-protocol.md` (иерархия источников, свежесть, маркировка, процедура старта, шаблон handoff).
- Создан `records/README.md` (формат первичной записи по образцу Envoy).

## Что осталось (по плану наполнения)

- `meta/handoff-current.md` — этот файл (в работе).
- `docs/METHOD.md` — наполнить: field cycle, two contours, run structure, git rule.
- `docs/KNOWLEDGE_STATES.md` — добавить компактные маркировки `[ФАКТ] / [ГИПОТЕЗА] / [НЕИЗВЕСТНО] / [МОЯ ПОЗИЦИЯ]`.
- `INVARIANTS.md` — добавить I9 (иерархия источников), I10 (свежесть), I11 (восстановление сырья).
- `00_ENTRY.md` — добавить ссылку на `meta/agent-rules.md` и `meta/handoff-protocol.md`.
- `DECISIONS.md` — записи `accepted` на все внесённые изменения (D-20261012-04 и далее).
- `README.md` — обновить структуру ядра (добавились meta-документы, records/README).
- Коммит и push.

## Открытые вопросы и блокеры

- Полномочия Архитектора (кто утверждает решения в форке) — не определено, замечание MS1/MS2/MS3, не закрыто.
- Fallback в `00_ENTRY.md` при работе без человека в цикле — не закрыто.
- `templates/` упомянута в README, но не создана — решить: создавать или убрать упоминание.
- Операционализация I7 (чек-лист самопроверки) — не сделано.
- Версионирование самого каркаса и правила миграции v1.1 → v1.2 — не сделано.

## Следующее конкретное действие

Завершить серию наполнения: `docs/METHOD.md` → `docs/KNOWLEDGE_STATES.md` → `INVARIANTS.md` (I9–I11) → `00_ENTRY.md` → `DECISIONS.md` → `README.md` → коммит и push.

## Ссылки

- `CURRENT_STATE.md` — живое состояние
- `DECISIONS.md` — журнал решений
- `meta/handoff-protocol.md` — протокол передачи
- `meta/agent-rules.md` — правила работы агента
