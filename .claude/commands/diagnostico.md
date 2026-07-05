---
name: diagnostico
description: >
  Faz o diagnóstico dos 4 pilares do negócio (Gestão, Marketing, Vendas, Imagem) numa entrevista
  curta e mostra um radar ao vivo, do lado, que preenche conforme a pessoa responde. No final
  devolve o arquétipo e a trilha de aulas personalizada. Dispara com /diagnostico, "fazer o
  diagnóstico", "onboarding", "por onde começar".
---

# /diagnostico — o mapa do teu negócio, ao vivo

Entrevista o usuário nos 4 pilares e vai desenhando um **radar ao vivo** num arquivo HTML aberto ao
lado. No fim entrega arquétipo + trilha personalizada. É o onboarding: descobrir por onde começar.

> Entrevista + radar ao vivo + resultado salvo no sistema. Ao final, o diagnóstico, a trilha e as
> respostas do aluno ficam gravados em `_contexto/diagnostico.md` (reordenar as pastas dos pilares
> pelo gargalo entra numa versão seguinte).

## Pré-requisito — o /setup primeiro (não pular etapa)

O diagnóstico só faz sentido depois que o sistema já te conhece. Antes de qualquer coisa, veja se
`_contexto/empresa.md` tem conteúdo real (não só o template).
- **Vazio ou só template:** NÃO comece. Diga: *"Antes do diagnóstico, roda o `/setup` pra eu te
  conhecer — assim a trilha sai calibrada pro teu negócio. Quando terminar, chama `/diagnostico` de
  novo."* E pare aqui.
- **Preenchido:** siga pro Passo 0. Aproveite o que o setup já sabe (nome, negócio, o que faz, pra
  quem) pra **pular as perguntas de identificação** e ir direto pras 12 de skill.

## Passo 0 — abre o radar ao lado (uma vez)

1. Copie o template pro diretório atual:
   `cp templates/diagnostico-radar.html diagnostico.html`
   (se `templates/diagnostico-radar.html` não existir, avise que o kit precisa estar instalado.)
2. Abra no navegador: Mac `open diagnostico.html` · Windows `start diagnostico.html` · Linux `xdg-open diagnostico.html`.
3. Diga ao usuário: *"Abri o teu radar numa aba do navegador. Deixa ela do lado — ele preenche sozinho conforme você responde aqui."*

O HTML se recarrega sozinho a cada ~1,3s enquanto não terminou (não precisa de extensão nem servidor).
Você só edita o bloco de dados; o radar redesenha.

## Como atualizar o radar

Depois de **cada resposta**, edite APENAS o bloco entre `/* DIAG-START */` e `/* DIAG-END */` no
`diagnostico.html`, reescrevendo o objeto `window.DIAG`. Nunca mexa no resto do arquivo.

Campos: `nome`, `negocio`, `total` (12), `feitas` (nº de perguntas de skill já respondidas),
`etapa` ("" enquanto responde, `"fim"` no final), `scores` {gestao, marketing, vendas, imagem} de
0 a 100, e no fim `nivel`, `arquetipo`, `leitura`, `trilha`.

**Faça o radar crescer a cada resposta:** o score de um pilar é a média das perguntas dele já
respondidas. Ex.: respondeu 2 das 3 de Gestão com 100 e 33 → `gestao: 67`. Atualize `feitas` e o
score do pilar da vez a cada resposta.

## A entrevista

Faça **uma pergunta por vez**, em conversa natural (não liste tudo). Ofereça responder por voz.
Tom: sócio, não guru. Sem emoji, sem "transforme sua vida".

### Identificação (não pontua — atualiza nome/negócio no radar)
1. Teu nome e o nome do negócio.
2. O que você faz e pra quem.
3. Faturamento hoje (pré-faturamento · até 10k · 10–30k · 30k+).
4. Maturidade em IA (nunca usei pra trabalhar=0 · ChatGPT solto às vezes=1 · uso direto sem método=2 · já tenho processo/agentes=3). Guarde como `ia_level`.

### Skill — 12 perguntas (3 por pilar). Opções em ordem crescente = 0 / 33 / 67 / 100.

**GESTÃO**
1. Quando o mês vem fraco, você sabe onde travou? [não sei de onde veio · acho que sei, no feeling · olho um setor ou outro · mapeio o funil e isolo o gargalo]
2. A operação — clientes, prazos, processos — mora onde? [tudo na minha cabeça · anotações e prints soltos · planilhas e apps que não conversam · um sistema central que eu alimento]
3. Sabe quanto custa trazer um cliente e quanto ele deixa no tempo? [não sei o que é · conheço mas não meço · meço um dos dois · acompanho os dois e decido por eles]

**MARKETING**
4. De onde vem teu próximo cliente? [é sorte · indicação que não controlo · posto e às vezes aparece · canal que traz com previsibilidade]
5. Teu conteúdo segue uma lógica (valor, autoridade, conexão, conversão)? [posto quando lembro · posto sem critério · tento variar os temas · linha editorial com pilar e função por post]
6. Como é tua relação com tráfego pago? [nunca rodei · impulsionei sem ler nada · rodo e olho curtida/alcance · rodo lendo CPA e ROAS e ajusto]

**VENDAS**
7. Sabe por que te contratam em vez do concorrente, fora o preço? [não sei · acho que é o preço · argumentos soltos · posicionamento e diferencial claros]
8. Quando chega um lead novo, você... [atende todo mundo igual · responde no improviso · tem um jeito de conduzir · qualifica fit/no-fit com processo]
9. Como chega no preço de um trabalho? [chuto/copio concorrente · custo + um pouco · calculo sem margem clara · modelo com margem e cenário de volume]

**IMAGEM**
10. Reconhecem um trabalho como teu sem ver a assinatura? [não, faço no estilo do cliente · raramente · tenho estilo mas não sei explicar · DNA definido que sei aplicar]
11. Você escolhe teus clientes ou aceita o que aparece? [pego qualquer trabalho · queria escolher mas não dá · recuso alguns por instinto · ICP claro que filtra e define preço]
12. Transformar teu trabalho em conteúdo é... [não faço · sofro do zero toda vez · consigo mas demora · tenho processo e referências que aceleram]

> A pessoa responde com o texto dela — encaixe a resposta na opção mais próxima e pontue. Não leia
> as notas em voz alta.

## Fechamento — calcule e preencha o resultado

Quando as 12 estiverem respondidas:

- **Score de cada pilar** = média das 3 perguntas.
- **Nível geral** = média dos 4 pilares → `< 30` **Explorador** · `30–59` **Em Ascensão** · `≥ 60` **Avançado**.
- **Arquétipo** (escolha o que melhor descreve o perfil):
  - **Técnico Silencioso** — Imagem alta, Marketing e Vendas baixos. Cria bem, não se mostra nem vende.
  - **Criativo com Medo** — scores médios/baixos espalhados e `ia_level` 0. Sabe que precisa, trava na ferramenta.
  - **Designer Reativo** — Gestão baixa, sem processo, vive de demanda e sem previsibilidade.
  - **Entusiasta em Transição** — `ia_level ≥ 2`, scores subindo, ainda sem sistema. Já testa IA, falta método.
  - **Solitário Visionário** — alto em 2–3 pilares, Gestão é o gargalo. Visão grande, operação presa nele.
- **Leitura** — 2 a 3 frases no tom Trilha: onde ele está forte, qual o **gargalo principal**, o que atacar primeiro. Sem enrolar.

### Montar a trilha

Ordem: **abertura fixa** → pilares do **menor score pro maior** (ataca o gargalo primeiro; empate: Gestão > Vendas > Marketing > Imagem). Se `ia_level ≤ 1`, mantenha a base conceitual antes do ferramental.

Use como `head` o nome do bloco (ex.: `"Vendas · teu gargalo"`, `"Imagem · teu forte"`) e marque
`soon: true` nas aulas ainda não gravadas. Cardápio por pilar (⏳ = em breve):

- **Gestão:** Design Importa · O Funil TD · Organizando a operação no Claude ⏳ · Precificação do Produto
- **Marketing:** Marketing de Atração · Defina seu Cliente (ICP) · Editoria e narrativa · Análise de tráfego com Claude ⏳
- **Vendas:** Design de Valor (posicionamento) · Funil de qualificação com Claude ⏳ · Simulação de margem e preço ⏳
- **Imagem:** Construa sua Identidade · Mapa de oportunidades com Claude · Auditoria de perfil com Claude ⏳

Abertura fixa de toda trilha (bloco `head: "Começo (todos)"`): Introdução Conceitual · Onboarding · Overview do Sistema Operacional.

Pega ~3 aulas do pilar-gargalo e 1–2 dos outros — trilha enxuta e legível, não despeje tudo.

### Último update do radar

Reescreva o `DIAG` com `etapa: "fim"`, os 4 scores finais, `nivel`, `arquetipo`, `leitura` e
`trilha` (array com `head` e itens `{nome, soon}`). Aí o radar para de recarregar e mostra o card
de resultado.

### Salve o resultado no sistema (importante)

Depois do resultado na tela, **grave tudo em `_contexto/diagnostico.md`** (crie/sobrescreva o
arquivo) — é o que faz o diagnóstico virar parte do sistema do aluno, não só uma tela que some.
Estrutura do arquivo:

```markdown
# Diagnóstico — [nome] · [data]

## Notas por pilar
- Gestão: NN · Marketing: NN · Vendas: NN · Imagem: NN
- Nível geral: [Explorador/Em Ascensão/Avançado] · Arquétipo: [nome]

## Leitura
[o gargalo principal e o que atacar primeiro — 2-3 frases]

## Minha trilha (por onde seguir)
1. [aula]  ·  ... marque as "(em breve)"
[na ordem: abertura fixa → pilar-gargalo → demais]

## Respostas (registro)
- Gestão: [resumo das 3 respostas]
- Marketing: [...]
- Vendas: [...]
- Imagem: [...]
```

Peça a data ao aluno ou deixe o campo `[data]` (não invente data). Ao terminar, avise:
*"Salvei teu diagnóstico e a tua trilha em `_contexto/diagnostico.md`. Toda vez que você rodar
`/iniciar`, eu já começo sabendo teu gargalo e o que vem primeiro."* Feche resumindo em voz o
gargalo e a primeira aula do caminho.
