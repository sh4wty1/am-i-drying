# Remover referência quebrada ao arquivo de memória no SKILL.md

**Por quê:** a seção `## Memory Protocol (MANDATORY)` mandava rodar `cat .claude/context/memory/learnings.md`, arquivo que não existe; o passo falhava sempre e violava a regra do `AGENTS.md` de não apontar para arquivos ausentes. Achado da auditoria `2026-10-16-full` (os 4 juízes; o Track A não pegou por ignorar blocos cercados).
**O quê:** seção inteira removida, incluindo a linha "ASSUME INTERRUPTION". Nada mais foi alterado no `SKILL.md`.
**Como:** edição única em `SKILL.md` (fim do arquivo). Optou-se por remover em vez de criar o arquivo, pois nada no repo grava aprendizados.
**Verificação:** `grep` por `context/memory|Memory Protocol|ASSUME INTERRUPTION` sem resultados; Track A re-executado (run `2026-10-16-fix-a`): 0 broken.
**Pendências:** demais cortes do plano Mixed (`.harness-eval/runs/2026-10-16-full/11-mixed-apply.md`) ainda não aplicados.
