# Comece aqui

Guia rápido para quem vai usar o segundo cérebro da Dal Piva.

## Instalar (uma vez)
1. Baixe o Obsidian em obsidian.md e instale.
2. Descompacte esta pasta (`dalpiva-cerebro`) em um lugar fixo do computador.
3. No Obsidian: **Open folder as vault** → escolha a pasta.
4. Em Configurações → Plugins principais, ative **Templates** e aponte a pasta de templates para `Templates`. Ative também **Daily notes** com a pasta `01-Diario` e o template `Templates/Diaria`.
5. Plugins da comunidade que ajudam (opcionais): **Dataview** (painéis tipo tabela), **Tasks** (tarefas espalhadas pelas notas), **Obsidian Git** (sincronizar com o GitHub).

## Usar com o Claude Code
Abra o terminal na pasta do vault e digite `claude`. Ele lê o `CLAUDE.md` sozinho e sabe como o vault funciona. Comandos prontos:

| Diga | O que acontece |
|---|---|
| "processa o inbox" | organiza tudo que está em `00-Inbox/` |
| "faz a ata dessa reunião: …" | cria a ata com decisões e tarefas |
| "registra a decisão: …" | cria a nota de decisão e atualiza o que ela afeta |
| "revisão da semana" | rascunho da revisão semanal |
| "audita o vault" | lista links quebrados, notas órfãs, dados sensíveis |
| "encerra a sessão" | salva o que foi feito para a próxima vez continuar |

## As 5 regras
1. Na dúvida, jogue no **Inbox**. Organizar é trabalho do Claude.
2. Número (valor, saldo, salário) fica no MaxiProd ou no sistema. Aqui fica o **processo** e o **porquê**.
3. Toda decisão importante vira nota em `06-Decisoes/`.
4. Nada de dados pessoais no vault.
5. Revise o que a IA escreve: ela organiza, quem decide são as pessoas.

## Por onde começar
1. Leia `index.md`.
2. Revise as notas marcadas como **proposta**: [[Configuração do MaxiProd]] e [[2026-11-25 OS é o pedido de venda]].
3. Nas notas de área, os links "a escrever" são os processos que faltam. Escolha um por semana e dite como é feito; o Claude transforma em nota.
