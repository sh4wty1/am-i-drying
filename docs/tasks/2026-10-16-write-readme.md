# Escrever o README

**Por quê:** passo 3 do `RUNBOOK.md`; o `README.md` tinha só o título.
**O quê:** README com o que a skill faz (resumo das Iron Laws, sem copiá-las), quando o agente a carrega, instalação no Claude Code (projeto ou `~/.claude/skills/dry-principle/`), como desenvolver (aponta para `RUNBOOK.md` e `AGENTS.md`) e licença.
**Como:** `/docs-writer` seguindo `references/style-guide.md` (inglês US, segunda pessoa, linhas ≤ 80, sentence case). Só `README.md` alterado. As regras ficam só no `SKILL.md`, para não ter duas fontes da verdade.
**Verificação:** nenhuma linha passa de 80 colunas; os 4 links locais existem. `npx harness-score`: L1, 38/105, sem mudança: o README não pesa no Context.
**Pendências:** o Context (45%) só sobe com rules com escopo (CTX-03 a CTX-06), workflows (SKL-03) e subagentes (AGT-01/02), não com o README. A instalação não foi testada numa sessão nova.
