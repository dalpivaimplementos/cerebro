---
tipo: processo
status: proposta
responsavel: Diretoria
atualizado: 2026-11-25
fonte: "[[Integração MaxiProd]]"
relacionados: ["[[Nota fiscal até o custo da OS]]", "[[2026-11-25 OS é o pedido de venda]]", "[[2026-11-25 MaxiProd como fonte única]]"]
---
# Configuração do MaxiProd

**Para que serve:** cadastrar no MaxiProd de um jeito que o sistema de gestão consiga ler tudo automaticamente, sem ninguém digitar duas vezes.
**Quando:** antes da primeira OP. Em 25/11/2026 o MaxiProd ainda está sem nenhum lançamento.

## As seis definições

1. **OS = pedido de venda.** Toda OS nasce de um pedido de venda, e a OP é gerada a partir do item do pedido. O sistema liga OS, cliente, valor e OP pelo ID, sem depender do texto "começa com 1545". Ver [[2026-11-25 OS é o pedido de venda]].
2. **Etapas da OP = colunas do quadro.** Os "estados configuráveis" da OP viram as colunas do quadro de produção (Em aguardo, Produzindo, A faturar…). Muda a etapa no MaxiProd e o cartão anda sozinho no sistema.
3. **Lote interno nas matérias-primas**, com o número da NF. Deixa o custo da OS rastreável até a nota.
4. **Toda NF de material baixada como insumo na OP.** Único lançamento, sem repetir no sistema.
5. **Centro de custos "Uso e consumo"** para combustível e afins.
6. **Apontamento de horas em um lugar só:** decidir se fica no sistema de gestão (já tem planilha e custo/hora) ou passa para o MaxiProd.

## Pendente
- Aprovar as seis definições com a diretoria.
- Escrever o passo a passo de cada tela do MaxiProd depois de configurado.
