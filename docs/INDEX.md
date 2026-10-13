# 📚 Índice da documentação — bomtexto

> Hub de navegação. As contagens vêm de `docs/onion/inventory.md` (gerado por
> `.claude/validation/inventory.sh`); regenere este índice com `/docs:build-index`.

## Contextos do projeto (L1+)

| Seção | Estado | Como gerar |
|---|---|---|
| [business-context](business-context/README.md) | pendente | `/docs:build-business-docs` |
| [technical-context](technical-context/README.md) | pendente | `/docs:build-tech-docs` |
| [compliance-context](compliance-context/README.md) | pendente | `/docs:build-compliance-docs` |

## Framework Onion (vendorizado, papel standalone)

| Seção | Conteúdo |
|---|---|
| [meta-specs](meta-specs/index.md) | constituição L0 do framework |
| [knowledge-base](knowledge-base/index.md) | 111 knowledge bases |
| [sdaal](sdaal/sdaal.md) | padrão SDAAL |
| [onion/inventory.md](onion/inventory.md) | 104 comandos · 51 agentes · 12 skills |
| [onion/graph.md](onion/graph.md) | grafo de dependências dos artefatos |
| [evolution](evolution/) | canais de co-evolução e semente de pesquisa |

## Grafo de conhecimento

- `onion/graph/onion-adoption.kg.yaml` — semente da adoção (leia com `bash .claude/validation/kg-radar.sh`).
