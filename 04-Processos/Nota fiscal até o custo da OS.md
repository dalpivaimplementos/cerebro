---
tipo: processo
status: em-revisao
responsavel: Suprimentos
atualizado: 2026-11-25
fonte: "Descrição do processo atual enviada pela diretoria em 25/11/2026"
relacionados: ["[[Configuração do MaxiProd]]", "[[Integração MaxiProd]]", "[[Suprimentos]]"]
---
# Nota fiscal até o custo da OS

**Para que serve:** levar o custo do material comprado para a OS em que ele foi usado.
**Quem executa:** Suprimentos · **Quando:** a cada nota de material recebida.

## Como é hoje

O caminho é **NF → estoque → OP**. Não existe ligação direta da nota com a OP.

1. **A nota entra no MaxiProd.** A NF-e é importada da SEFAZ para "Notas fiscais recebidas". Item que não existe no cadastro é criado na hora (grupo 02 – Matérias Primas), com código interno e referência ao código do fornecedor.
2. **A nota é "Recebida".** Os itens entram no estoque com o valor da nota e o contas a pagar é gerado.
3. **A divisão por OS é decidida no sistema de gestão** (campo "Lançamentos" da nota). Ex.: "OS 1545 · Alibra – 100%".
4. **O item é baixado na OP do MaxiProd.** Entra como insumo (operação 0 – Padrão) com a quantidade definida no passo 3, e "Salvar e baixar". Essa baixa gera a saída de estoque ligada à OP, e é ela que leva o custo.
5. **Fechamento:** no sistema de gestão a nota é marcada como "Lançado no Junsoft".

A OS do sistema corresponde à OP cujo campo "Item do pedido/OP" começa com o número da OS. Ex.: OS 1545 → OP 1546, "1545 #1 (8) – Alibra".

## Pontos de atenção

- **A divisão é digitada duas vezes** (passo 3 no sistema e passo 4 no MaxiProd). É a dupla digitação que o projeto [[Sistema Central Dal Piva]] quer eliminar.
- **O custo vem da baixa, não da nota.** Com custo médio, o valor baixado pode ser diferente do valor da NF quando o item já tinha saldo de compras anteriores. Até agora os itens eram novos, então bateu.
- **A origem (qual NF) não fica na OP.** Só dá para rastrear pelo item e pelas movimentações, ou por lote.
- Nota dividida entre duas OS = duas baixas, uma em cada OP.
- Notas de uso e consumo (combustível etc.) não vão para OP. Fluxo ainda não definido. Centro de custos não é usado.

## Proposta (ainda não aprovada)

1. A divisão passa a ser feita **só no MaxiProd** (passo 4). O sistema lê as baixas e monta o custo da OS sozinho; o campo "Lançamentos" vira só conferência e depois some.
2. O sistema avisa diferenças: "NF planejada para a OS 1545 mas ainda não baixada na OP".
3. Lote interno = número da NF nas matérias-primas, para rastrear cada baixa até a nota de origem.
4. Centro de custos "Uso e consumo" para notas que não vão para OP.

Ver [[Configuração do MaxiProd]].
