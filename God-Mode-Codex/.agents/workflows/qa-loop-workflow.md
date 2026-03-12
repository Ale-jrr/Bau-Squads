---
description: QA Loop - Workflow iterativo de revisão do Quality Assurance
---

Acionado apenas se o Quality Gate (Passo 4 do workflow SDC) falhar, ou seja, se o agente `@qa` encontrar problemas no código desenvolvido pelo `@dev`. O Loop tem um **máximo de 5 iterações**.

1. **(@qa) Review & Report:** Liste todos os problemas encontrados no código com clareza na resposta (arquivos e linhas afetadas, regras de negócio feridas, vulnerabilidades).
2. **(@dev) Correção (Fix):** Leia o relatório do passo 1. Modifique os arquivos necessários para sanar **todos** os problemas apontados pelo QA de uma só vez.
3. **(@qa) Re-Review:** Revise novamente as alterações feitas no passo 2.
   - Se aprovado (PASS), encerre este workflow e retorne ao passo 5 do workflow SDC (`@devops push`).
   - Se falhar (FAIL), volte ao Passo 1 deste workflow, reduzindo o número restante de iterações permitidas.
   - Se exceder 5 iterações sem sucesso, sinalize "ESCALATED" e avise o Usuário Humano para intervir manualmente.
