# resume-screener-squad
Squad especialista em triagem de currículos para recrutamento — parsing automatizado de CVs, matching de skills com requisitos da vaga, auditoria de vieses, ranking de candidatos e geração de resumos executivos para hiring managers.

## Comando de Instalação
```bash
npx squads add gutomec/squads-sh-aios/resume-screener-squad -y
```

## Visão Geral
O **resume-screener-squad** é um squad completo que cobre todo o pipeline de triagem de currículos:
1. **Parsing de Currículos**: Extração automatizada de dados estruturados (PDF, DOCX, texto).
2. **Matching de Skills**: Fit score ponderado e identificação de skills transferíveis.
3. **Auditoria de Vieses**: Detecção de vieses de gênero, idade, etnia, etc.
4. **Ranking de Candidatos**: Ranking transparente com justificativas.
5. **Resumos Executivos**: Briefs para hiring managers com pontos fortes e perguntas de entrevista.

## Agentes
- `resume-parser`
- `skills-matcher`
- `bias-auditor`
- `shortlist-ranker`
- `candidate-summary-agent`

## Workflows
- `*triage-full`
- `*quick-match`

## Comandos Principais
- `*parse-resumes`: Apenas parsing de CVs.
- `*match-skills`: Matching de habilidades.
- `*audit-bias`: Auditoria de viés.
- `*rank-candidates`: Ranking de candidatos.
- `*candidate-summary`: Geração de resumo individual.

---
*Fonte: [SQUADS.sh](https://squads.sh/pt/gutomec/squads-sh-aios/resume-screener-squad)*
