---
name: setup
description: >
  Configura o teu Trilha OS pro teu negócio. Te entrevista sobre quem você é, o que faz e como
  trabalha, e gera CLAUDE.md, contexto, estrutura de pastas e identidade visual.
  Use quando o usuário chamar /setup, quando _contexto/empresa.md estiver vazio, ou disser
  "configurar o sistema", "primeira vez", "setup".
---

# /setup — Configuração do teu Trilha OS

## Verificação inicial

Veja se `_contexto/empresa.md` já tem conteúdo real (não só o template).
- **Vazio/template:** começa o onboarding abaixo.
- **Já preenchido:** avisa que o setup já foi feito e pergunta se quer refazer ou só atualizar algo.

---

## Onboarding (primeira vez)

Mensagem curta de boas-vindas:

> "Boa, [vamos configurar o teu sistema]. Vou te fazer algumas perguntas pra deixar o Claude
> sabendo do teu negócio — quanto mais específico você for, mais ele trabalha por você. Sem pressa."

Faça as perguntas **uma por vez, em conversa natural**. Não liste todas de uma vez. Espere a
resposta antes da próxima.

### Pergunta 1 — Quem é você
"Qual é o teu nome e o nome do teu negócio (ou projeto)?"

### Pergunta 2 — Histórico / importar contexto
"É a primeira vez que você usa o Claude assim, ou já usa ChatGPT/Claude/Gemini no dia a dia?"

**Se já usa outro assistente:** ofereça importar o contexto pra não responder tudo do zero —
mostre este prompt pra ela colar no assistente que usa e trazer a resposta:

```
Preciso exportar o contexto do meu negócio das nossas conversas pra configurar uma ferramenta nova.
Responda com o que você sabe sobre mim — deixe em branco o que não souber:
NOME: / NEGÓCIO: / O QUE FAÇO E PRA QUEM: / O QUE MAIS PRODUZO: / ATENDO CLIENTES?: /
EQUIPE: / FERRAMENTAS QUE USO: / IDENTIDADE VISUAL (cores/fontes/estilo): / TOM DE VOZ: /
O QUE ME INCOMODA EM TEXTO DE IA: / OUTROS DETALHES:
```

Com o que vier, monte um resumo, confirme com a pessoa, e **pule as perguntas já respondidas**.

### Pergunta 3 — O que você faz
"O que você mais produz/entrega no dia a dia? E pra que tipo de cliente?"

### Pergunta 4 — Momento do negócio
"Como tá o negócio hoje — faturamento aproximado, sozinho ou com equipe, há quanto tempo?"
*(Sem julgamento; só pra calibrar o sistema.)*

### Pergunta 5 — O gargalo (os 4 pilares)
"Dos quatro pilares, qual mais te trava hoje? **Gestão** (operação/tempo/decisão), **Marketing**
(atrair gente), **Vendas** (fechar/precificar) ou **Imagem** (identidade e conteúdo)?"

Anote o gargalo — ele define a ordem das pastas e o que priorizar.

### Pergunta 6 — Nível de IA
"Hoje você usa IA mais como? (1) quase não uso · (2) pergunto coisas no chat de vez em quando ·
(3) já uso bastante no trabalho · (4) já automatizo coisas."
*(Calibra o quão básico começar.)*

### Pergunta 7 — Ferramentas
"Quais ferramentas você usa hoje no trabalho? Cita as principais."

### Pergunta 8 — Identidade visual
"Tua marca tem identidade visual? Pode mandar o link do site, jogar uns prints na pasta `dados/`
e me dizer os nomes, descrever em texto (cores, fontes, estilo), ou dizer que ainda não tem."

- **URL:** buscar com WebFetch, detectar cores/tipografia/estilo, confirmar antes de preencher.
- **Imagens:** ler os arquivos, analisar, confirmar.
- **Texto:** usar direto.
- **Não tem:** preencher `marca/design-guide.md` com campos em branco e avisar que o Claude usa
  visual neutro até ela preencher.
- Logo: perguntar se tem PNG/SVG pra `marca/`.

### Pergunta 9 — Tom de voz
"Como você quer que o Claude escreva pra você? O que mais te incomoda em texto de IA?"

---

## Camada Diagnóstico (opcional, recomendada)

Depois das perguntas, ofereça:

> "Quer um diagnóstico mais fundo dos teus 4 pilares? Roda em ~6 min aqui:
> https://trilha-os-diagnostico.pages.dev — no fim, cola o resultado aqui que eu uso pra calibrar
> a tua trilha. Se preferir, seguimos só com o que você já me contou."

Se a pessoa colar o resultado, use pra refinar o gargalo, o nível e a ordem de prioridade.

---

## O que gerar (de uma vez, no final)

1. **`CLAUDE.md`** — atualizar a partir do template do kit com os dados reais: o que é o negócio,
   o que produz, os 4 pilares (marcando o gargalo), tom de voz, ferramentas. Manter as seções de
   fluxo, "aprender com você" e a regra "skills chegam ao longo das aulas".
2. **`_contexto/empresa.md`** — nome, negócio, o que faz, perfil, equipe, ferramentas, estado nos
   4 pilares, gargalo.
3. **`_contexto/estrategia.md`** — fase, prioridade principal, o que pode esperar, prazos.
4. **`_contexto/preferencias.md`** — tom de voz, o que evitar, estilo.
5. **`marca/design-guide.md`** — preenchido (ou em branco com orientação).
6. **Estrutura de pastas** — usar `templates/perfis/empreendedor-criativo.md` como base; mostrar a
   sugestão e deixar a pessoa ajustar; ordenar pelo pilar do gargalo. Criar as pastas.
7. **Ferramentas/MCPs** — cruzar a Pergunta 7 com `templates/ferramentas/catalogo.md`; sugerir
   conectar só o essencial agora; anotar o resto em `tarefas.md` pra depois.

---

## Mensagem final

> "[Nome], teu Trilha OS tá configurado.
>
> Criei: CLAUDE.md (o Claude agora sabe quem você é), _contexto/ (negócio, foco e preferências),
> marca/design-guide.md e a estrutura de pastas pro teu perfil. Teu gargalo hoje é **[pilar]** —
> é por aí que a gente vai atacar primeiro.
>
> Duas coisas antes de seguir:
> 1. Chaves de API vão sempre num arquivo `.env` (já protegido, nunca sobe pro GitHub).
> 2. Roda `/syncar` pra conectar no GitHub e nunca perder teu trabalho.
>
> Próximo passo: roda `/mapear` pra eu pegar um processo teu e transformar na primeira skill.
> E lembra: o sistema vem enxuto — vou te entregando novas skills ao longo das aulas, instala só
> o que for usar."

---

## Regras
- Tom direto e humano, sem excesso de entusiasmo, sem emoji de foguete.
- Perguntas em conversa, não em lista. Resposta vaga → uma pergunta de acompanhamento.
- Gera todos os arquivos de uma vez no final, não um a um.
- IA é copiloto: a pessoa sai sentindo que o sistema é dela.
