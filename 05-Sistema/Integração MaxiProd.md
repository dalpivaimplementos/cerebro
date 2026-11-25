---
tipo: sistema
status: ativo
responsavel: Diretoria
atualizado: 2026-11-25
fonte: "Schema GraphQL da API MaxiProd exportado em 25/11/2026 (api.maxiprod.com.br/graphql)"
relacionados: ["[[2026-11-25 MaxiProd como fonte única]]", "[[Configuração do MaxiProd]]", "[[Nota fiscal até o custo da OS]]"]
---
# Integração MaxiProd

## O que a API é
- GraphQL em `api.maxiprod.com.br/graphql`, autenticação `Authorization: Basic <token>`.
- **Só leitura:** 70 consultas, nenhuma de gravação. O sistema lê do MaxiProd, mas não escreve nada lá.
- Toda entidade principal pode ser filtrada por `ultimaAlteracaoData`, então a sincronização busca só o que mudou.
- O token fica guardado no servidor como `MAXIPROD_TOKEN`. **Nunca colar o token em print, nota ou conversa.** Se vazar, gerar outro no MaxiProd.

## O que cada tela do sistema vai puxar

| Tela do sistema | Consulta da API | Campos principais |
|---|---|---|
| Quadro de produção | `ordensDeProducao` | número, estado, estado configurável, emissão, necessidade (prazo), dias de atraso |
| Cliente e valor da OS | OP → `itemDoPedidoDeVenda` → `pedidoDeVenda` | cliente, valor total |
| Custo de material | `custoTotalDasMovimentacoes` da OP; detalhe em `estoqueMovimentacoes` com `destinoOrdemDeProducaoId` | valor de cada baixa, lote, item |
| Custo de mão de obra | `maoDeObraCusto`, horas previstas/realizadas, `apontamentos` | se o apontamento for feito no MaxiProd |
| A faturar | `pedidosDeVenda` | valor faturado, valor a faturar |
| Fluxo de caixa | `contaAPagar`, `contaAReceber` | vencimento, valor em aberto, estado (pago/recebido), liquidação |
| Notas fiscais | `notasFiscais`, `itensDasNotasFiscais` | já sincroniza hoje (botão "Sincronizar MAXIPROD") |
| Compras e terceirização | `pedidosDeCompra`, `solicitacoesDeCompra`, envio/retorno de terceirização | disponível |
| DRE | `balanceteContabil`, `lancamentosContabeis` | só se a contabilidade for lançada no MaxiProd |

Estados da OP: `SUGERIDA`, `A_PRODUZIR`, `FECHADA`, `CANCELADA`, `SUSPENSA_SUGERIDA`, mais os estados configuráveis da empresa.
Estados de contas: `DIGITACAO`, `EMITIDO`, `PAGO`/`RECEBIDO`, `PARCELADO`, `AGRUPADO`, `COMPENSADO`, `CANCELADO`.

## Rastrear qual NF foi para qual OP
A movimentação de estoque tem `notaFiscalItemId` (preenchido na entrada da nota), `loteInterno` e `origemLoteId`. Com lote nas matérias-primas, dá para seguir saída → lote → entrada → NF com exatidão. Sem lote, só por item + data (aproximado para itens recorrentes).

## O que ainda falta testar
- Em 25/11/2026 o MaxiProd está vazio; as consultas de OP devolveram erro 500 sem dados.
- Testar com a primeira OS real: as três consultas de teste (OPs, movimentações de uma OP, contas a pagar).
