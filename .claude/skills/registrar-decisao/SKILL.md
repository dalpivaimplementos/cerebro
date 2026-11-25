---
name: registrar-decisao
description: Registra uma decisão da empresa com contexto, alternativas e consequências, e atualiza as notas afetadas. Use quando disserem "decidimos", "ficou definido", "vamos fazer assim" ou pedirem para registrar uma decisão.
---

# Registrar decisão

1. Confirme com a pessoa, em uma frase, o que foi decidido e quem decidiu. A IA não decide nada sozinha.
2. Crie `06-Decisoes/AAAA-MM-DD Título curto.md` a partir de `Templates/Decisao.md`.
   - `status: ativo` se já vale; `proposta` se ainda vai ser aprovada.
3. Procure as notas que a decisão afeta (processos, áreas, sistema) e atualize cada uma, com link para a decisão.
4. Se a decisão substitui uma anterior, mude a antiga para `status: arquivado` e escreva no topo dela: "Substituída por [[nova decisão]]".
5. Atualize `index.md` e `log.md`.
