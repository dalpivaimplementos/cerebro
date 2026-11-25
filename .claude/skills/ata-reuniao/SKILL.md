---
name: ata-reuniao
description: Transforma transcrição, áudio transcrito ou anotações soltas de uma reunião em ata padronizada, com decisões e tarefas. Use quando pedirem ata, resumo de reunião ou "registra essa reunião".
---

# Ata de reunião

1. Pergunte (se não estiver no texto): data, assunto e participantes.
2. Crie `07-Reunioes/AAAA-MM-DD Assunto.md` a partir de `Templates/Reuniao.md`.
3. Preencha:
   - **Assuntos:** tópicos discutidos, em frases curtas.
   - **Decisões:** só o que foi de fato decidido. Opinião ou ideia não é decisão.
   - **Tarefas:** tabela O quê / Quem / Até. Se não houver responsável ou prazo, escreva "definir".
4. Para cada decisão relevante (muda processo, custo, cliente, sistema), crie também uma nota em `06-Decisoes/` e ligue as duas.
5. Se a reunião falou de uma OS, cliente ou projeto, acrescente uma linha com link na nota da área ou projeto correspondente.
6. Não registre na ata: salários, problemas de saúde, conflitos pessoais. Se aparecerem, omita e avise.
7. Atualize `index.md` (se criou decisão) e `log.md`.
8. Mostre a ata pronta e destaque o que ficou incerto.
