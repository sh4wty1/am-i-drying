# Aplicar o plano Mixed da auditoria no SKILL.md

**Por quê:** a auditoria `2026-10-16-full` classificou `SKILL.md` como Mixed: núcleo útil (Iron Laws) cercado de persona genérica, bloco `<instructions>` que contradizia as leis 1/3/4, tabela Anti-Patterns duplicada e frontmatter sem efeito. A `description` também não dizia quando usar a skill, como exige o `AGENTS.md`.
**O quê:** `SKILL.md` reduzido de 82 para 17 linhas: frontmatter só com `name` + `description` (agora com gatilhos de uso), uma linha de tese, Iron Laws 1–5 sem alteração e a lei 6 (setup de testes autocontido, vinda da linha 5 da tabela). Removidos `<identity>`, `<capabilities>`, `<instructions>`, `<examples>`, a tabela Anti-Patterns e as chaves extras do frontmatter (inclusive `model: sonnet`). Decisões dos Holds do Track B: C008 mantido como tese de uma linha; C012 (lei 2) mantido.
**Como:** reescrita de `SKILL.md` seguindo o KEEP/CUT de `.harness-eval/runs/2026-10-16-full/11-mixed-apply.md`, mais as decisões do usuário (cortar todas as chaves extras e reescrever a description).
**Verificação:** run `2026-10-16-post-apply`: Track A 0 broken; Track C trap PASS, fan-in PASS, `SKILL.md` = Keep-core nos dois juízes (claude-opus-5-5). `npx harness-score`: L1, 38/105, igual ao anterior (mudança só de conteúdo).
**Pendências:** README com `/docs-writer`; auditoria do `AGENTS.md`; nada commitado.
