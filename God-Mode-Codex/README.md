# God Mode for Codex / Ralph
Uma adaptação do [AIOS God Mode Template](https://github.com/gutomec/aios-god-mode-template) otimizada para ser usada como instruções e workflows no **Codex / Ralph** ou outras CLIs de agentes.

## Como Usar
No God Mode original, a CLI do Claude lê autonomamente a pasta `.claude`. No Codex/Ralph, nós adaptamos essa lógica para a sua engenharia de prompts.

1. **Copie o arquivo `instructions.md`** e cole o conteúdo no prompt de sistema ou arquivo raiz de contexto do seu agente (ex: `.agents/prompts` ou `.agents/rules.md`).
2. **Copie os arquivos da pasta `workflows/`** para a sua pasta `.agents/workflows/`. Assim o Ralph saberá como executar cada etapa do desenvolvimento (como o Ciclo SDC e o QA Loop).

## Agentes Disponíveis
- `@pm` (Morgan): Produto, Requisitos, Epics.
- `@po` (Pax): Product Owner, validação de tarefas.
- `@sm` (River): Scrum Master, divisão e criação de stories.
- `@dev` (Dex): Desenvolvedor, implementação técnica.
- `@qa` (Quinn): Quality Assurance, revisão de código e testes.
- `@devops` (Gage): Integrações, Git, Servidores MCP e Deploy.
- `@architect` (Aria): Decisões de arquitetura e tecnologia.

## Workflows Disponíveis
- `sdc-workflow.md`: O fluxo principal de desenvolvimento de uma Story (Draft -> Validate -> Implement -> QA -> Ship).
- `qa-loop.md`: Ciclo de revisão interativo quando o QA encontra problemas.

Se precisar adicionar mais workflows, você pode usar os prompts contidos no template original como base e adaptar para a sintaxe Markdown do Ralph (com as regras numéricas de passo a passo).
