---
name: revisao-semanal
description: Gera o rascunho da revisão semanal da empresa a partir das notas diárias, atas, decisões e projetos da semana. Use toda sexta ou quando pedirem revisão ou resumo da semana.
---

# Revisão semanal

1. Leia as notas de `01-Diario/`, `07-Reunioes/` e `06-Decisoes/` dos últimos 7 dias, e todos os projetos ativos de `02-Projetos/`.
2. Escreva `_IA/revisao-AAAA-SS.md` (SS = número da semana) com:
   1. **O que foi feito**: por área.
   2. **Decisões da semana**: com links.
   3. **Tarefas em aberto**: das atas e notas diárias, com responsável e prazo. Destaque as atrasadas.
   4. **Projetos parados**: sem atualização na "Situação atual" há 7 dias ou mais.
   5. **Inbox**: quantos itens estão esperando.
   6. **Sugestão de prioridades** para a próxima semana (marcado como sugestão da IA).
3. Números de produção e financeiro **não** saem do vault: se a pessoa quiser, consulte o sistema de gestão/MaxiProd e diga a fonte.
4. Mostre o rascunho. A pessoa edita; não trate como final.
5. Registre em `log.md`.
