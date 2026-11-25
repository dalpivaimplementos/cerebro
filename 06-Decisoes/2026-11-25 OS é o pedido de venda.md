---
tipo: decisao
status: proposta
responsavel: Diretoria
atualizado: 2026-11-25
fonte: "Conversa de planejamento de 25/11/2026"
relacionados: ["[[Configuração do MaxiProd]]", "[[Integração MaxiProd]]"]
---
# OS é o pedido de venda

## Contexto
No processo atual, a OS do sistema é ligada à OP do MaxiProd pelo texto do campo "Item do pedido/OP" (ex.: "1545 #1 (8) – Alibra" para a OS 1545). Ligação por texto quebra fácil.

## Decisão (proposta)
A OS passa a ser o **pedido de venda** do MaxiProd. A OP é gerada a partir do item do pedido, e o sistema liga OS → cliente → valor → OP pelos IDs da API.

## Alternativas consideradas
- Continuar ligando pelo texto: frágil, depende de digitação.
- Usar campo adicional da OP com o número da OS: possível, mas é mais uma coisa para digitar.

## Consequências
- Toda produção precisa começar por um pedido de venda no MaxiProd.
- O número da OS passa a ser o número do pedido.

## Quando rever
Aprovar antes da primeira OP no MaxiProd.
