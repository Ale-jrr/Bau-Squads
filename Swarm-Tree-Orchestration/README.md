# Swarm Tree Orchestration Squad

> **Fonte:** https://squads.sh/pt/Renat0z/squads/swarm-tree-orchestration  
> **Autor:** Renat0z · Criado por `nirvana-squads-creator-lite`  
> **Licença:** MIT  
> **Tags:** `orchestration` · `recursive-decomposition` · `task-tree` · `multi-agent` · `wbs` · `context-factory` · `wave-execution` · `circuit-breaker`

---

## O Problema com Tarefas Complexas

Você sabe o que acontece quando um agente tenta executar uma tarefa enorme diretamente.

Ele começa, perde o fio, produz código incompleto, ou simplesmente trava no meio.

A causa: Sem planejamento prévio, o agente não sabe o escopo real, não gerencia dependências entre sub-tarefas e desperdiça contexto.

O **Swarm Tree Orchestration Squad** resolve isso com uma regra simples:

> **Planejar a árvore COMPLETA antes de executar qualquer folha.**

---

## Como Funciona

```
┌────────────────────────────────────────────────┐
│              FASE 1 — PLANEJAMENTO             │
│                                                │
│  P0: Setup .swarm-tree/                        │
│  P1: TaskDecomposer → rawTree (recursivo)      │
│  P2: NodeScorer → UxIxR scoring + dep graph   │
│  P3: TreeOrchestrator → tree.json + context   │
│  P4: ContextComposer → prompts por nó          │
│  P5: TreeValidator → WBS + circuit breaker    │
│  P6: Apresentação para validação do usuário   │
└───────────────────────┬────────────────────────┘
                        │ usuário valida
                        ▼
┌────────────────────────────────────────────────┐
│               FASE 2 — EXECUÇÃO                │
│                                                │
│  WaveDispatcher → ondas paralelas via          │
│  TaskCreate (respeitando dependências)         │
│                                                │
│  │ Poll unificado + reactive dispatch          │
│                                                │
│  │ TreeIntegrator → valida artefatos +         │
│  corrige imports + gera relatório final        │
└────────────────────────────────────────────────┘
```

---

## Scoring UxIxR

O NodeScorer aplica um scoring tridimensional para priorizar nós da árvore:

- **U** — Urgência
- **x** — Impacto
- **R** — Reversibilidade

---

## Tasks

| Task | Descrição |
|------|-----------|
| `decomposeTask()` | Decompõe a tarefa principal em sub-tarefas recursivamente |
| `groupSubtasks()` | Agrupa sub-tarefas relacionadas |
| `scoreNodes()` | Aplica scoring UxIxR nos nós da árvore |
| `buildDependencyGraph()` | Constrói o grafo de dependências entre nós |
| `generateTreePlan()` | Gera o plano em `tree.json` |
| `composeContext()` | Compõe os prompts de contexto por nó |
| `validateCircuitBreaker()` | Valida violações da Golden Rule |
| `dispatchWave()` | Despacha ondas paralelas de execução |
| `integrateTree()` | Integra artefatos e valida imports |
| `analyzeTree()` | Analisa o estado atual da árvore |
| `resumeTree()` | Retoma execução a partir de checkpoint |

---

## Workflows

| Workflow | Descrição |
|----------|-----------|
| `tree_planning_flow` | Fluxo completo de planejamento (Fases P0–P6) |
| `tree_execution_flow` | Fluxo de execução em ondas paralelas |
| `tree_analysis_flow` | Análise do estado da árvore |
| `tree_resume_flow` | Retomada de execução interrompida |

---

## Comandos

| Comando | Descrição |
|---------|-----------|
| `/sto *orchestrate-tree TASK="..."` | Executa o fluxo completo (planejamento + execução) |
| `/sto *plan-tree TASK="..."` | Gera apenas a Fase 1 (árvore para revisão) |
| `/sto *resume-tree` | Retoma execução interrompida a partir do checkpoint |
| `/sto *analyze-tree` | Analisa o estado atual da árvore |

---

## Golden Rule

```
Nó com ≤2 sub-tarefas → executor (folha)
Nó com >2 sub-tarefas → coordenador (delega recursivamente)
```

> Toda folha tem no máximo 2 tarefas. O circuit breaker bloqueia qualquer violação.

---

## FAQ

### O squad funciona com qualquer tipo de tarefa?
Sim. O `TaskDecomposer` aceita qualquer descrição de tarefa e aplica a decomposição recursiva. Quanto mais específica a tarefa, mais precisa a árvore gerada.

### O que acontece se uma folha falhar?
O `WaveDispatcher` aplica **delta relaunch**: lê o checkpoint da folha, lista os arquivos já criados, e reexecuta com um prompt de continuação. Máximo 2 tentativas por folha.

### Posso inspecionar o plano antes da execução?
Sim. Use `*plan-tree` para gerar apenas a fase 1 e revisar `tree.json` antes de autorizar a execução.

### Como retomar uma execução interrompida?
Use `*resume-tree` com o caminho para `.swarm-tree/tree-plan/tree.json`. O squad identifica folhas completas, falhas e pendentes automaticamente.

---

## Estrutura de Arquivos

```
.swarm-tree/
└── tree-plan/
    └── tree.json    ← Plano gerado na Fase 1
```
