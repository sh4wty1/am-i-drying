# am-i-drying

`dry-principle` is an agent skill that applies the Don't Repeat Yourself (DRY)
principle when an agent writes or reviews code, without over-abstracting. The
whole skill is one file: [`SKILL.md`](SKILL.md).

## What the skill does

Most agents read "don't repeat yourself" as "never write the same thing twice."
That habit produces premature, wrong abstractions. This skill gives the agent
six concrete rules (its Iron Laws) that set when to remove duplication and when
to leave it alone. For example:

- Wait for three concrete instances before you extract shared logic.
- Don't merge code that only looks similar but serves different purposes.
- Prefer readable duplication over an abstraction that hides what code does.

The rules live only in [`SKILL.md`](SKILL.md), so they have a single source of
truth.

## When the agent uses it

The agent loads the skill when you:

- Write or review code that duplicates logic, constants, or config.
- Decide whether to extract a shared helper.
- Ask for a DRY review, for example "Review this code for DRY compliance."

## Install

To use the skill in Claude Code, copy `SKILL.md` into a skills directory under
a folder named after the skill:

1. Choose where to install it:
   - For one project: `.claude/skills/dry-principle/` in that project.
   - For all your projects: `~/.claude/skills/dry-principle/`.
2. Copy the file into that folder:

   ```bash
   mkdir -p ~/.claude/skills/dry-principle
   cp SKILL.md ~/.claude/skills/dry-principle/SKILL.md
   ```

3. Start a new Claude Code session so the skill is discovered.

## Develop the skill

This repo contains only the skill and the tooling to evaluate it. There's no
application code, build, or test runner. To change the skill, follow the steps
in [`RUNBOOK.md`](RUNBOOK.md). Contributor conventions are in
[`AGENTS.md`](AGENTS.md).

## License

This project is licensed under the MIT License. See [`LICENSE`](LICENSE).
