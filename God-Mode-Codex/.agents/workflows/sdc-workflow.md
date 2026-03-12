---
description: Story Development Cycle (SDC) - O fluxo principal do God Mode
---

Este workflow descreve o ciclo principal de vida de uma Feature / Bugfix (Story) usando os agentes do God Mode no seu projeto. Execute os passos em ordem.

1. **(@sm) Planejamento / Draft:** Crie um rascunho da Story dentro da pasta `docs/stories/`. A história deve conter Título, Descrição e Critérios de Aceitação (AC).
// turbo
2. **(@po) Validação:** Valide se a Story criada no passo 1 tem clareza de escopo, dependências e valor de negócio. Se estiver confusa ou faltar detalhes, corrija a história antes de prosseguir.
3. **(@dev) Implementação:** Leia a Story validada. Analise a base de código do projeto atual e modifique os arquivos necessários para cumprir todos os Critérios de Aceitação. Trabalhe iterativamente e rode testes locais se necessário.
4. **(@qa) Quality Assurance (Review & Gate):** Assuma a postura rigorosa de QA. Revise o código gerado no Passo 3. Verifique unit tests (se houver), cumprimento dos ACs, regressões, segurança e documentação.
   - Se houver falha, pare este workflow e inicie o `qa-loop-workflow`.
   - Se passar sem ressalvas, altere o status da Story para "Done".
5. **(@devops) Deploy & Ship:** Somente execute isso se o Passo 4 for aprovado. Faça o commit das alterações informando o ID da Story na mensagem, e então realize um `git push`.
