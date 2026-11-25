---
tipo: sistema
status: ativo
responsavel: Diretoria
atualizado: 2026-11-25
fonte: "Base de conhecimento do sistema (25/11/2026) e repositório dalpivaimplementos/dalpiva"
relacionados: ["[[Integração MaxiProd]]", "[[Perfis e acessos]]", "[[Sistema Central Dal Piva]]"]
---
# Visão geral do sistema

Sistema web próprio que complementa o ERP: PCP, produção, financeiro auxiliar, notas fiscais e folha. Feito no Lovable, código no GitHub em `dalpivaimplementos/dalpiva`. As regras técnicas oficiais estão no `AGENTS.md` do repositório; esta nota explica o sistema para quem não programa.

## Módulos

| Menu | O que faz |
|---|---|
| **Comercial** | Orçamentos (com PDF), orçamentos de serviço, clientes com anexos |
| **PCP e Produção** | Quadro de OS (kanban), cronograma de entregas, apontamento de horas (planilha colaborador × OS), equipamentos, tarefas |
| **Suprimentos** | Pedidos de compra, notas fiscais (importação manual, em lote, pelo Gmail e pelo MaxiProd) |
| **Financeiro** | Fluxo de caixa (com PDF em calendário), DRE, custos, busca em notas, relatórios de pagamento, fechamento mensal |
| **Pessoas** | Colaboradores e folha mensal, contratações com checklist |
| **Configurações** | Usuários, tipos de equipamento, textos do orçamento, alçadas |

## Painel da OS
Indicadores de venda, material (NFs), mão de obra, terceiros, imposto, despesas, lucro e margem. Abas: resumo, horas, notas fiscais, compras, anexos, despesas, terceiros, histórico. A margem no cartão fica vermelha abaixo de 15%, âmbar até 30% e verde acima.

## Regras permanentes
1. Não mudar o comportamento do que já existe ao adicionar algo novo.
2. No banco, só adicionar; nunca apagar ou renomear.
3. Rotas antigas sempre funcionando.
4. Toda tabela nova com acesso por perfil.
5. Custo/hora calculado no servidor para o PCP não ver salários.
6. Módulos removidos não voltam: Terceirização, Fila de Produção, Aprovações, Solicitações de compra, avanço % na OS.

## Tecnologia (para quem desenvolve)
TanStack Start + React 19, Tailwind, Supabase (banco, login, arquivos), publicado no Cloudflare Workers. Mudanças grandes são feitas pelo Claude Code em branch separado e revisadas antes de entrar.
