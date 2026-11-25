---
name: processar-inbox
description: Organiza o que está em 00-Inbox — classifica cada item, cria ou atualiza notas nas pastas certas, extrai tarefas e decisões. Use quando pedirem para processar, organizar ou limpar o inbox.
---

# Processar o Inbox

1. Liste os arquivos de `00-Inbox/`, ignorando o `LEIA-ME.md`. Se não houver mais nada, diga isso e pare.
2. Para cada item, **antes de qualquer coisa**, verifique dados sensíveis (salário, CPF, saúde, documentos, senhas, tokens). Se tiver: não processe, avise a pessoa e sugira apagar.
3. Classifique o item:
   - reunião → nova nota em `07-Reunioes/` (template `Reuniao`)
   - decisão → nova nota em `06-Decisoes/` (template `Decisao`)
   - "como fazemos X" → criar ou **atualizar** a nota em `04-Processos/`
   - informação sobre uma área ou projeto → acrescentar na nota existente da área/projeto
   - material bruto (PDF, exportação) → mover para `08-Fontes/` e criar a nota que resume, com `fonte:` apontando para ele
4. Antes de criar nota nova, procure se já existe uma sobre o assunto. **Prefira atualizar a duplicar.**
5. Extraia tarefas (com responsável e prazo, se houver) para a nota do dia em `01-Diario/`.
6. Ligue cada nota nova a 2–4 notas relevantes que já existem.
7. Apague do Inbox só o que foi processado com sucesso.
8. Atualize `index.md` e `log.md`.
9. Responda com uma tabela: item → para onde foi → o que precisa de revisão humana.

Se não tiver certeza da classificação, deixe o item no Inbox e pergunte. Não invente contexto.
