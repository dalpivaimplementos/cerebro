---
tipo: sistema
status: ativo
responsavel: IA
atualizado: 2026-11-25
---
# Índice do Segundo Cérebro

Ponto de entrada de toda consulta. Atualizado a cada nota criada, movida ou arquivada.

## Áreas
- [[Produção]]: quadro de OS, PCP, apontamento de horas, equipamentos
- [[Comercial]]: orçamentos, clientes, pedidos de venda
- [[Suprimentos]]: compras, notas fiscais de entrada, estoque
- [[Financeiro]]: fluxo de caixa, contas a pagar/receber, custos, DRE, fechamento
- [[Pessoas]]: colaboradores, contratações, folha (só processos, sem dados pessoais)

## Projetos ativos
- [[Sistema Central Dal Piva]]: transformar o sistema de gestão na central da empresa, com o MaxiProd como fonte única

## Processos
- [[Nota fiscal até o custo da OS]]: hoje (com dupla digitação) e proposta
- [[Prospecção de peneiras]]: como usar o CRM de prospecção (proposta)
- [[Configuração do MaxiProd]]: como cadastrar para o sistema conseguir ler (proposta)

## Sistema
- [[Visão geral do sistema]]: módulos, stack, regras permanentes
- [[Integração MaxiProd]]: o que a API oferece e o que cada tela vai puxar
- [[Perfis e acessos]]: quem vê o quê

## Decisões
- [[2026-11-25 MaxiProd como fonte única]]
- [[2026-11-25 Acesso por perfil nas tabelas]]
- [[2026-11-25 OS é o pedido de venda]] (proposta)
- [[2026-11-25 Hospedagem continua no Lovable]]

## Rotinas
- Diária: nota do dia em `01-Diario/`, processar o Inbox (skill `processar-inbox`)
- Semanal: skill `revisao-semanal`
- Mensal: skill `auditar-vault`
