---
tipo: decisao
status: ativo
responsavel: Diretoria
atualizado: 2026-11-25
fonte: "Conversa de planejamento de 25/11/2026"
relacionados: ["[[Integração MaxiProd]]", "[[Sistema Central Dal Piva]]", "[[Nota fiscal até o custo da OS]]"]
---
# MaxiProd como fonte única

## Contexto
Notas fiscais, divisão de custos por OS e contas eram lançadas no ERP e de novo no sistema de gestão. Isso gera retrabalho e diferenças entre os dois.

## Decisão
Tudo que o MaxiProd faz (OS/pedido de venda, OP, notas fiscais, contas a pagar e a receber, estoque) é lançado **só no MaxiProd**. O sistema de gestão lê pela API e mostra de forma visual; guarda só o que o ERP não tem (anotações, posição/observações do quadro, folha, contratações, simulações e alertas).

## Alternativas consideradas
- Manter o sistema de gestão como lugar principal e importar no ERP: descartado, a API do MaxiProd não aceita gravação.
- Continuar com os dois em paralelo: descartado, é a dupla digitação que se quer eliminar.

## Consequências
- Mudar etapa de OS, lançar nota ou baixar contas é sempre no MaxiProd; o sistema reflete alguns minutos depois.
- Cadastro do MaxiProd precisa seguir [[Configuração do MaxiProd]].
- Partes manuais do sistema (lançamentos de NF na OS, importação de boletos) serão desligadas quando a sincronização estiver confirmada.

## Quando rever
Depois da primeira OS real lançada e sincronizada.
