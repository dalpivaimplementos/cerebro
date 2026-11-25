---
tipo: sistema
status: ativo
responsavel: Diretoria
atualizado: 2026-11-25
fonte: "AGENTS.md e migração 0007_rls_por_perfil do repositório dalpivaimplementos/dalpiva"
relacionados: ["[[2026-11-25 Acesso por perfil nas tabelas]]", "[[Visão geral do sistema]]"]
---
# Perfis e acessos

## Perfis
| Perfil | Para quem | Grupo |
|---|---|---|
| admin | Administração do sistema | Produção + Financeiro |
| socio | Sócios (vira admin automaticamente) | Produção + Financeiro |
| producao | Chão de fábrica / produção | Produção |
| pcp | Planejamento (vira produção automaticamente) | Produção |
| gestor_producao | Gestor da fábrica (vira produção automaticamente) | Produção |
| financeiro | Escritório / financeiro | Financeiro |

## Quem vê o quê
| Assunto | Produção | Financeiro |
|---|---|---|
| Quadro, OS, equipamentos, orçamentos | ✅ | — |
| Notas fiscais, rateios, clientes | ✅ | ✅ |
| Fluxo de caixa, DRE, custos, fechamento | — | ✅ |
| Colaboradores, folha, contratações | — | ✅ |
| Apontamento de horas | PCP, gestor, admin | só leitura |

PCP e gestor veem o **custo/hora** do colaborador, mas não o salário.

## Cuidados
- Dar admin/sócio só para quem precisa. Uma migração antiga (30/09/2026) deu admin a todos os usuários da época. **Revisão pendente** na tela Usuários.
- Usuário sem perfil não vê nada.
