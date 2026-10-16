# Instalar skills do fassi-skills

**Por quê:** preparar o repositório (uma skill `dry-principle` em `SKILL.md`) com skills de apoio para criar, auditar e documentar skills.
**O quê:** instaladas `skill-architect`, `harness-eval` e `docs-writer` (conjunto recomendado) para Claude Code, e criado `RUNBOOK.md` com a ordem de uso para humanos.
**Como:** `npx --yes @tech-leads-club/agent-skills install -s <skill> -a claude-code` na raiz; arquivos em `.claude/skills/<skill>/SKILL.md`.
**Verificação:** confirmada a existência de `.claude/skills/{skill-architect,harness-eval,docs-writer}/SKILL.md`.
**Pendências:** nenhum workflow (matt-pocock/tlc) instalado, pois o projeto não tem trabalho de feature. Ordem de uso registrada em `RUNBOOK.md`.
