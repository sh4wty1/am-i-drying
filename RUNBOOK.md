# Runbook

Run each step from the repo root, in Claude Code.

1. **Audit** — `/harness-eval` on `SKILL.md`.
   Flags broken references and noise. Read the report before changing anything.

2. **Rework** — `/skill-architect`.
   Fix the skill using what the audit found.

3. **Document** — `/docs-writer`.
   Turn the one-line README into a real one.

4. **Score** — `npx harness-score` in a terminal.
   Run it now for a baseline, then again after each milestone.
