# AIOS God Mode Template
Gera um sistema completo de desenvolvimento orquestrado por IA em segundos com 10 agentes de IA, 22 skills e 3 servidores MCP instalados em um único comando.

## Comando de Instalação
```bash
npx create-aios-god-mode meu-projeto
```

## O que Faz
Este template é o "God Mode" para Synkra AIOS. Ele fornece orquestração completa com uma estrutura de projeto pronta contendo:
- **10 Personas de IA Especializadas**, cada uma com comandos dedicados e handoff integrado que preserva o contexto.
- **Desenvolvimento Orientado a Stories**: Trabalho flui por etapas claras (`draft` -> `validate` -> `develop` -> `gate`).
- **Sistema de Squads**: Squads multi-agente pré-configurados.
- **Ecossistema de Skills**: 22 skills da comunidade instaladas automaticamente (frontend, SEO, pagamentos, geração com IA).
- **Integração MCP**: 3 servidores MCP pré-configurados para imagens, docs e UI component.
- **Proteção do Framework**: deny rules determinísticas e arquivos base imutáveis para estabilidade.

## Workflows Principais
- **Story Development Cycle (SDC)**: Workflow principal para implementação.
  `@sm *draft` → `@po *validate` → `@dev *develop` → `@qa *gate` → `@devops *push`
- **QA Loop**: Revisão iterativa e correção com máximo de 5 iterações.
  `@qa review` → veredito → `@dev corrige` → re-review
- **Spec Pipeline**: Transforma requisitos informais em specs executáveis.
- **Brownfield Discovery**: Avaliação de projeto legado e débito técnico em 10 fases com múltiplos agentes.

## Agentes Principais e Comandos
- **@dev**: `*develop`, `*build-autonomous`, `*run-tests`, `*self-critique`
- **@qa**: `*review`, `*gate`, `*security-check`, `*test-design`
- **@architect**: `*design-system`, `*tech-selection`, `*api-design`
- **@pm**: `*create-prd`, `*create-epic`, `*execute-epic`, `*write-spec`
- **@po**: `*validate-story-draft`, `*close-story`, `*backlog-review`
- **@sm**: `*draft`, `*story-checklist`
- **@analyst**: `*research`, `*feasibility-study`, `*user-research`
- **Outros**: `@data-engineer`, `@ux-design-expert`, `@devops`, `@aios-master`

---
*Fonte: [GitHub - gutomec/aios-god-mode-template](https://github.com/gutomec/aios-god-mode-template)*
