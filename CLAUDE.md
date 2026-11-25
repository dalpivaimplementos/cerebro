# Segundo Cérebro — Dal Piva Implementos

Este vault é a base de conhecimento da DAL PIVA IMPLEMENTOS: como a empresa funciona, por que as coisas são feitas de um jeito, e a documentação do sistema de gestão. Toda sessão começa lendo este arquivo. Escreva em português do Brasil.

## A empresa

Fabricante de caçambas roll on/off, caçambas estacionárias, peneiras e carretas em Toledo-PR. A produção é por encomenda: cada venda vira uma OS, que é produzida, faturada e entregue.

## Onde mora cada coisa (regra de ouro)

| Tipo de informação | Fonte da verdade | O vault guarda |
|---|---|---|
| Dados do dia a dia: OS, notas, contas, estoque | **MaxiProd** (ERP) | Nada. Só links e explicações |
| Dados do sistema próprio: horas, anotações, folha | **Sistema de gestão** (Supabase) | Nada. Só links e explicações |
| Conhecimento: processos, decisões, regras, aprendizados | **Este vault** | Tudo |

Nunca copie números do ERP para cá (valores de OS, saldos, salários). Eles ficam velhos no dia seguinte. Escreva o **processo** e o **porquê**, e aponte onde o número está.

## Estrutura

| Pasta | O que vai | Quem escreve |
|---|---|---|
| `00-Inbox/` | Tudo que chega sem organizar: transcrição de áudio, foto de quadro, ideia, e-mail colado | Qualquer pessoa |
| `01-Diario/` | Uma nota por dia: `AAAA-MM-DD.md` | Pessoas + IA (seção "Log da IA") |
| `02-Projetos/` | Uma nota por projeto com começo e fim | Responsável do projeto |
| `03-Areas/` | Responsabilidades contínuas: Produção, Comercial, Suprimentos, Financeiro, Pessoas | Responsável da área |
| `04-Processos/` | "Como fazemos X", passo a passo. Uma nota por processo | Quem executa + IA |
| `05-Sistema/` | Documentação do sistema de gestão e das integrações (MaxiProd) | IA + quem desenvolve |
| `06-Decisoes/` | Uma nota por decisão: `AAAA-MM-DD Título.md` | Quem decidiu |
| `07-Reunioes/` | Atas: `AAAA-MM-DD Assunto.md` | Quem conduziu |
| `08-Fontes/` | Material bruto original (PDFs, exportações, manuais). **Nunca editar** | Qualquer pessoa |
| `99-Arquivo/` | Projetos encerrados e notas que não valem mais | IA na auditoria |
| `_IA/` | Saídas da IA: `sessoes/` e rascunhos | Só a IA |
| `Templates/` | Modelos de nota | Não alterar sem combinar |

Não crie pastas novas no primeiro nível. Se algo não couber, pergunte.

## Frontmatter obrigatório

Toda nota fora de `00-Inbox/`, `08-Fontes/` e `_IA/` começa com:

```yaml
---
tipo: processo | decisao | reuniao | projeto | area | sistema | diario
status: ativo | proposta | em-revisao | arquivado
responsavel: Nome
atualizado: AAAA-MM-DD
fonte: "[[nota ou arquivo de onde veio]]"   # obrigatório em processo e sistema
relacionados: ["[[Nota A]]", "[[Nota B]]"]
---
```

## Links

- Use `[[Nome da Nota]]` para áreas, processos, decisões e projetos.
- Ligue só quando entender uma nota muda a forma de ler a outra. Duas a quatro ligações relevantes por nota valem mais que vinte genéricas.
- Pode ligar para nota que ainda não existe: vira lembrete de que falta escrever.
- **Não crie notas de pessoas físicas** (funcionários, candidatos, clientes pessoa física). Cite pelo primeiro nome no texto.

## Dados sensíveis (LGPD)

Nunca escreva neste vault: salários, CPF, dados de saúde, raça, filhos, documentos pessoais, senhas, tokens de API, dados bancários. Se aparecerem no Inbox, **não processe**: avise e sugira apagar.

## Protocolo de início de sessão

1. Ler `index.md`.
2. Ler as duas últimas notas de `_IA/sessoes/` e a nota de hoje em `01-Diario/` (crie a partir do template se não existir).
3. Ver se há algo em `00-Inbox/` e notas com `status: em-revisao`. Mencionar em uma linha.

## Protocolo de encerramento

1. Gravar `_IA/sessoes/AAAA-MM-DD-HHmm.md` (template `Templates/Sessao.md`).
2. Acrescentar uma linha em "Log da IA" na nota do dia.
3. Acrescentar uma linha em `log.md`.
4. Se criou ou moveu notas, atualizar `index.md`.

## Como responder

- Direto, em tópicos curtos. Sem enrolação.
- Toda afirmação sobre a empresa cita a nota de onde veio. Se não houver nota, diga "não encontrei no vault" em vez de supor.
- Separe **o que está escrito** do **que você está sugerindo**.
- Decisões importantes são das pessoas. A IA propõe, organiza e registra; não decide.

## Erros que já aconteceram (atualize esta lista)

- _(vazio por enquanto: quando a IA errar algo recorrente, registre aqui a regra que evita o erro)_
