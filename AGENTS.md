# am-i-drying

## Overview

A single agent skill, `dry-principle` (`SKILL.md` at the root), that applies the
Don't Repeat Yourself principle when writing and reviewing code. The repo has no
application code. The skill is the product.

## Layout

- `SKILL.md`: the skill being developed.
- `.claude/skills/`: helper skills installed for working on it (`harness-eval`,
  `skill-architect`, `docs-writer`). These are tooling, not the product.
- `RUNBOOK.md`: the order to use the helper skills in, written for humans.
- `docs/tasks/`: one log per task (see the global task-log rule).

## Build & test

There is no build or test runner. To verify a change:

- Run `/harness-eval` on `SKILL.md` and address what it flags.
- Run `npx harness-score` and compare it with the previous score.

## Conventions

- `SKILL.md` frontmatter must have `name` and `description`; the description
  says what the skill does and when to use it.
- Keep `SKILL.md` under 500 lines. Move long reference material into separate
  files next to it.
- Don't add instructions that point to files the repo doesn't contain.
- Edit the helper skills in `.claude/skills/` only by reinstalling them.
