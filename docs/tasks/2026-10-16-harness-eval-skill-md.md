# Auditar SKILL.md com harness-eval (Tracks A+B+C)

**Por quê:** passo 1 do `RUNBOOK.md`: auditar a skill `dry-principle` antes do retrabalho com `/skill-architect`.
**O quê:** run `2026-10-16-full` completa em `.harness-eval/runs/2026-10-16-full/`. Track A: 0 BROKEN. Track B: trap PASS, 9 Ship (C001–C007, C009, C010), 7 Review, 2 Hold (C008, C012). Track C: trap PASS, fan-in PASS, `SKILL.md` = Mixed (plano em `11-mixed-apply.md`). Nenhuma edição em `SKILL.md` (só relatórios).
**Como:** `inventory_extract.py --seed SKILL.md` (o arquivo fica na raiz, fora das árvores de skill), `track_a_correctness.py`, 4 juízes em paralelo (claude-opus-5-5), `merge_agreement.py`, `surfaces_extract.py`, `merge_usefulness.py`.
**Verificação:** os dois merges reportaram trap PASS; os juízes de C usaram o mesmo modelo.
**Pendências:** Track A não detecta o path quebrado `.claude/context/memory/learnings.md` (`SKILL.md:76`, dentro de bloco cercado); o extrator de claims ignora a tabela Anti-Patterns; `AGENTS.md` ficou fora do escopo por causa do `--seed`; aplicar o plano Mixed em outra sessão; reavaliar C com um segundo modelo antes de cortes grandes.
