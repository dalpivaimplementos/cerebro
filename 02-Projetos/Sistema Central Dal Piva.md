---
tipo: projeto
status: ativo
responsavel: Diretoria
atualizado: 2026-11-25
relacionados: ["[[Visão geral do sistema]]", "[[Integração MaxiProd]]", "[[2026-11-25 MaxiProd como fonte única]]"]
---
# Sistema Central Dal Piva

**Objetivo:** o sistema de gestão vira a central visual da empresa. O MaxiProd é o único lugar onde se lança OS, nota fiscal e contas; o sistema lê do MaxiProd, mostra de forma visual e inteligente, e guarda só o que o ERP não tem.
**Área:** todas.

## Etapas
- [x] Código do sistema no GitHub (`dalpivaimplementos/dalpiva`), sincronizado com o Lovable
- [x] Regras do projeto unificadas (`AGENTS.md` + `CLAUDE.md` no repositório)
- [x] Acesso por perfil nas tabelas que estavam abertas ([[2026-11-25 Acesso por perfil nas tabelas]])
- [ ] Revisar quem é admin na tela Usuários (com a diretoria)
- [ ] Configurar o MaxiProd para o sistema conseguir ler ([[Configuração do MaxiProd]])
- [ ] Lançar uma OS real completa no MaxiProd e testar a API
- [ ] Agendamento automático da sincronização (cron do Cloudflare): PR #2, conferir em produção depois do merge
- [ ] Sincronizar contas a pagar/receber → fluxo de caixa automático
- [ ] Sincronizar pedidos de venda e OPs → quadro de produção automático
- [ ] Custo da OS pelas baixas de estoque do MaxiProd
- [ ] Assistente de IA dentro do sistema
- [ ] Alertas: prazo em risco, OS sem apontamento, caixa negativo previsto

## Situação atual
25/11/2026: segurança corrigida e no ar (PR #1). MaxiProd ainda sem nenhum lançamento, então os testes da API esperam a primeira OS real. Próximo passo técnico: agendamento automático da sincronização.

## Decisões do projeto
- [[2026-11-25 MaxiProd como fonte única]]
- [[2026-11-25 Acesso por perfil nas tabelas]]
- [[2026-11-25 OS é o pedido de venda]] (proposta)
- [[2026-11-25 Hospedagem continua no Lovable]]

## Riscos e bloqueios
- A API do MaxiProd é só de leitura: o sistema não consegue gravar nada no ERP.
- O processo de dividir a NF entre OS ainda é feito duas vezes (ver [[Nota fiscal até o custo da OS]]).
- Falta definir se o MaxiProd substitui o Junsoft ou se os dois convivem.
