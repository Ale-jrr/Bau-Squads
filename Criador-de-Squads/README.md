# Nirvana Squad Creator
Gera squads AIOS otimizados a partir de linguagem natural — uma meta-ferramenta que cria outros squads completos.

## Comando de Instalação
```bash
npx squads add gutomec/squads-sh-aios/nirvana-squad-creator -y
```

## O que Faz
O **Nirvana Squad Creator** cobre um pipeline de 9 fases para produzir squads com:
- Agentes com personalidade (Archetypes).
- Tasks com contratos explícitos de Entrada/Saída.
- Workflows com seleção automática de patterns.
- READMEs em 6 idiomas.
- Publicação direta no marketplace `squads.sh`.

## Pipeline de 9 Fases
1. **Análise de Requisitos**: `squad-analyzer`
2. **Geração de Agentes**: `squad-agent-creator`
3. **Geração de Tasks**: `squad-task-creator`
4. **Geração de Workflows**: `squad-workflow-creator`
5. **Otimização**: `squad-optimizer`
6. **Validação**: `squad-validator`
7. **READMEs Multi-idioma**: `squad-readme-creator`
8. **Deploy**: Deploy automático.
9. **Publicação**: `squad-publisher`

## Workflows Principais
- `squad_generation_pipeline`: Do zero até a publicação.
- `squad_publish_flow`: Validação e publicação de squad existente.

## Comandos de Uso
- `/SQUADS:nsc:squad-analyzer`: Inicia a análise para um novo squad.
- `/SQUADS:nsc:squad-agent-creator`: Gera os agentes.
- *(E outros comandos para cada fase do pipeline)*

---
*Fonte: [SQUADS.sh](https://squads.sh/pt/gutomec/nirvana-squad-creator/nirvana-squad-creator)*
