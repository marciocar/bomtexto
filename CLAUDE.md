# 🧅 bomtexto — Claude Code Rules

## 🎯 Identidade

**bomtexto** é um projeto orquestrado com o **Sistema Onion** (`role: standalone`, modo greenfield —
ver `.claude/.onion-version`). O propósito do projeto **ainda será descrito pelo dono**: a primeira
sessão aqui roda `/docs:build-business-docs` para gerar `docs/business-context/`.

- Papel **standalone**: uso direto num projeto individual — o ciclo de produto, engenharia e
  compliance, mais a meta-fábrica (`/meta:create-*`); **sem** adoção de outros repos nem federação.
- **KG primeiro:** estudos e decisões viram `.kg.yaml` (`git ls-files '*.kg.yaml'`); a semente da
  adoção já está no repo.

## 📚 Contextos (L1+ deste projeto)

`docs/business-context/` · `docs/technical-context/` · `docs/compliance-context/` — hoje vazios
(`status: pendente`). Gerar com `/docs:build-business-docs`, `/docs:build-tech-docs` e
`/docs:build-compliance-docs`. As meta-specs em `docs/meta-specs/` são o L0 do framework.

## 🔌 Task Manager

Antes de operar com tasks, carregue as variáveis de ambiente do projeto e leia
`TASK_MANAGER_PROVIDER` (`none` por padrão); para conferir sem expor segredos,
`bash .claude/utils/task-manager/env-check.sh`. Configure com `/meta:setup-integration`.
Detalhes: `.claude/utils/task-manager/`. Nunca versione segredos.

## 📝 Linguagem

Skill `language-standards`: prosa, docs e commits (assunto/corpo) em pt-BR; código, nomes de
arquivo e branches em inglês; prefixo Conventional Commits em inglês.

## 🚪 Entrada

`/warm-up` (carrega o contexto) → `/onion` (orquestrador).

## 🌿 Branches

`main` = integração e produção (trunk-based). Toda mudança entra por branch + PR. As atualizações do
Onion chegam pela `onion/vendor` (base comum do `--update`) e entram na `main` por PR com **merge
commit** (nunca rebase/squash).
