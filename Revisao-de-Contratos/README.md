# Contract Review Squad
Squad especialista em revisão automatizada de contratos legais — extração de cláusulas, análise de riscos e conformidade com playbooks.

## Comando de Instalação
```bash
npx squads add gutomec/squads-sh-aios/contract-review-squad -y
```

## O que Faz
O **Contract Review Squad** automatiza o pipeline de revisão de contratos, reduzindo drasticamente o tempo de análise manual:
1. **Extração**: Parsing de contratos (PDF, DOCX, texto) e identificação de cláusulas e obrigações.
2. **Análise de Riscos**: Identificação de termos desfavoráveis e proteções ausentes.
3. **Conformidade**: Verificação contra playbook corporativo (Approved/Fallback/Dealbreaker).
4. **Redlines**: Sugestão de linguagem alternativa com justificativas.
5. **Relatório**: Geração de sumário executivo e matriz de decisão.

## Agentes
- `clause-extractor`: Extração de cláusulas e dados.
- `risk-flagger`: Identificação e pontuação de riscos.
- `playbook-enforcer`: Verificação de conformidade com regras corporativas.
- `redline-drafter`: Redação de alterações sugeridas.
- `summary-reporter`: Orquestração e geração de relatórios.

## Workflows Principais
- `*review-contract`: Revisão completa de um contrato ponta a ponta.
- `*quick-review`: Avaliação rápida de riscos.

## Comandos Principais
- `*full-review`: Inicia a revisão detalhada.
- `*check-compliance`: Verifica o contrato contra seu Playbook YAML.
- `*suggest-changes`: Solicita sugestões de redline.
- `*create-report`: Gera o relatório final para stakeholders.

---
*Fonte: [SQUADS.sh](https://squads.sh/pt/gutomec/squads-sh-aios/contract-review-squad)*
