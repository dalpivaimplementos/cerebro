---
name: auditar-vault
description: Faz a manutenção do vault — links quebrados, notas órfãs, duplicadas, sem frontmatter, sem fonte, desatualizadas ou com dados sensíveis. Use uma vez por mês ou quando pedirem auditoria ou limpeza.
---

# Auditar o vault

Verifique e liste em `_IA/auditoria-AAAA-MM.md`:

1. **Dados sensíveis**: salários, CPF, tokens, senhas, dados de saúde. Prioridade máxima: reporte primeiro.
2. **Links quebrados**: `[[...]]` que apontam para nota inexistente (separe os que são lembretes intencionais).
3. **Notas órfãs**: sem nenhum link entrando nem saindo.
4. **Duplicadas**: duas notas sobre o mesmo processo ou assunto.
5. **Frontmatter**: faltando, incompleto ou com valores fora do padrão do CLAUDE.md.
6. **Sem fonte**: notas `processo` ou `sistema` sem `fonte:`.
7. **Desatualizadas**: `atualizado` há mais de 90 dias em notas `ativo`.
8. **Projetos encerrados** fora de `99-Arquivo/`.
9. **Índice**: notas que não aparecem em `index.md`.

Não corrija nada sozinho. Mostre a lista com a ação sugerida para cada item e espere a pessoa aprovar. Depois de aprovado, corrija, atualize `index.md` e registre em `log.md`.
