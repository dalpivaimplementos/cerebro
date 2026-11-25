---
tipo: decisao
status: ativo
responsavel: Vinicios
atualizado: 2026-11-25
fonte: "Conversa de planejamento de 25/11/2026"
relacionados: ["[[Sistema Central Dal Piva]]", "[[Visão geral do sistema]]"]
---
# Hospedagem continua no Lovable

## Contexto
O código do sistema agora é escrito pelo Claude Code e revisado no GitHub. O Lovable continua publicando o site e guardando o banco de dados (com todos os dados e logins). Sair do Lovable daria controle total (por exemplo, garantir o agendamento automático), mas exige migrar o banco.

## Decisão
Por enquanto o Lovable fica **só como hospedagem**: publica o site e guarda o banco. Todo o desenvolvimento passa pelo Claude Code + GitHub, com revisão antes do merge.

## Alternativas consideradas
- Migrar já para Cloudflare e Supabase próprios: mais controle e sem assinatura do Lovable, mas com risco de parar a empresa durante a migração do banco.

## Consequências
- Não dá para garantir daqui que o Lovable publica configurações como o agendamento (cron); cada uma precisa ser conferida depois do merge.
- Migrações do banco são aplicadas pelo Lovable.

## Quando rever
Quando o sistema estiver estável com o MaxiProd alimentando os dados, ou se o Lovable bloquear algo importante (como o agendamento). Aí planejar a migração para contas próprias num fim de semana, com cópia completa do banco antes.
