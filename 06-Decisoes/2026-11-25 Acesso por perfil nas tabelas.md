---
tipo: decisao
status: ativo
responsavel: Diretoria
atualizado: 2026-11-25
fonte: "PR #1 do repositório dalpivaimplementos/dalpiva (migração 0007_rls_por_perfil)"
relacionados: ["[[Perfis e acessos]]", "[[Sistema Central Dal Piva]]"]
---
# Acesso por perfil nas tabelas

## Contexto
Contratações (com dados pessoais de candidatos), fechamento mensal, notas fiscais, rateios, clientes e orçamentos podiam ser lidos e editados por qualquer usuário logado, mesmo sem acesso à tela. Problema de segurança e de LGPD.

## Decisão
Cada tabela passa a exigir o grupo de perfil que já usa a tela: contratações e fechamento só Financeiro; notas, rateios e clientes Produção + Financeiro; orçamentos só Produção. Aprovado e aplicado em 25/11/2026 (PR #1).

## Consequências
- Ninguém perdeu acesso a tela que já abria.
- Usuário sem perfil não vê nada.
- Ficou pendente revisar quem é admin (ver [[Perfis e acessos]]).

## Quando rever
Sempre que um módulo novo for criado ou um perfil novo surgir.
