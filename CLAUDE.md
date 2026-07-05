# Meu Trilha OS

> Este é o teu sistema operacional. O Claude lê este arquivo toda vez que você fala com ele —
> é o mapa do teu negócio e das tuas pastas. Quanto mais você alimenta, mais ele trabalha por você.

## O que é isso

Esta pasta é o teu **Trilha OS**: o lugar onde você opera o teu negócio com o Claude de sócio.
Não é uma ferramenta que você liga pra usar e fecha — é onde o trabalho acontece. Conteúdo,
estratégia, vendas, gestão e imagem, tudo num lugar só, com a inteligência do teu negócio junto.

Você ainda **não tem tudo aqui** — e isso é de propósito. O kit vem enxuto pra não te travar.
Ao longo das aulas a gente entrega novas skills e habilidades pra você ir acrescentando conforme
precisa. Comece operando com o que tem; o resto chega na hora certa.

## Como o Claude deve te tratar

No começo de toda conversa, ler (se existirem):
1. `_contexto/empresa.md` — quem você é, o que faz, como funciona o negócio
2. `_contexto/preferencias.md` — teu tom de voz, estilo, o que evitar
3. `_contexto/estrategia.md` — teu foco atual, prioridades, prazos

Usar isso como base pra qualquer resposta. Pra tarefa visual (carrossel, post, slide, página),
consultar `marca/design-guide.md`. Não precisa anunciar que leu — só usar o contexto naturalmente.

## Os 4 pilares (vocabulário da Trilha OS)

Você opera o negócio em torno de quatro pilares. Cada um ganha skills próprias ao longo do curso:

- **Gestão** — organizar a operação, decidir com clareza, liberar teu tempo
- **Marketing** — atrair com previsibilidade (posicionamento, conteúdo, tráfego)
- **Vendas** — qualificar, precificar, fechar com margem
- **Imagem** — identidade visual, narrativa e produção de conteúdo com voz autoral

## As tuas pastas (cada uma é um pilar)

O sistema é organizado pra você enxergar onde mora cada parte do negócio. Não precisa decorar —
o Claude usa isso sozinho. Mas quando bater a dúvida "onde eu ponho isso?", é aqui:

| Pasta | Pilar | O que vai dentro |
|---|---|---|
| `_contexto/` | Gestão | o cérebro: quem você é, foco, preferências |
| `ideias/` | Gestão | inbox de ideias cruas (vira pauta/projeto depois) |
| `conteudo/` | Marketing | carrosséis, posts, roteiros |
| `marca/` | Imagem | teu design-guide e identidade |
| `referencias/` | Imagem | moodboard: inspirações, paletas, prints que você guarda |
| `clientes/` | Vendas | um por cliente: briefing → proposta → entrega |
| `precos/` | Vendas | precificação, o que você cobra |
| `projetos/` | — | trabalhos maiores / portfólio |
| `dados/` | análise | prints de métrica, planilhas — pra o Claude analisar |

`ideias/`, `referencias/` e `dados/` já vêm prontas (com um README). As outras o `/setup` cria
conforme o teu gargalo — você não começa com pasta vazia sem sentido.

## O que já vem instalado (núcleo)

**Comandos** (em `.claude/commands/`):
- `/setup` — configura o sistema pro teu negócio (te entrevista e gera teu contexto)
- `/diagnostico` — o onboarding: te entrevista nos 4 pilares e desenha um radar ao vivo do lado, com teu arquétipo e a trilha de aulas por onde começar
- `/iniciar` — carrega o contexto no começo de cada sessão (rode antes de trabalhar)
- `/mapear` — transforma um processo repetitivo teu numa skill
- `/novo-projeto` — cria pasta + contexto pra um projeto ou cliente novo
- `/atualizar` — sincroniza o contexto quando algo mudou
- `/syncar` — salva teu trabalho no GitHub (backup)

**Skills** (em `.claude/skills/`):
- `carrossel` — cria carrossel de Instagram/LinkedIn com tua identidade
- `legenda` — escreve legenda de post com hook e CTA
- `pauta` — transforma uma ideia/tema em pauta de conteúdo pronta pra produzir
- `conselho` — teu conselho de 6 cadeiras (visão, marketing, vendas, operação, criativo, financeiro)
  pra estressar uma decisão antes de tomar

**Roadmap de skills** (o que chega por aula): `templates/skills/catalogo.md`.

## Fluxo de trabalho

Antes de executar qualquer tarefa, ver se existe skill/comando relevante em `.claude/`. Se existir,
seguir a skill. Se não, executar normalmente.

Ao terminar algo que parece repetível (você provavelmente vai pedir de novo), perguntar:
> "Isso pode virar uma skill pra próxima vez. Quer que eu crie?"

## Aprender com você

Quando você corrigir algo ou der uma instrução que parece permanente ("prefiro assim", "não faça
mais isso", "sempre que..."), perguntar:
> "Quer que eu salve isso pra não precisar repetir?"

Se sim, salvar no lugar certo: negócio → `_contexto/empresa.md` · preferências → `_contexto/preferencias.md`
· foco/prioridade → `_contexto/estrategia.md` · regra desta pasta → este `CLAUDE.md`.
Salvar só a linha nova, sem reformatar o arquivo inteiro.

## Mentalidade (o jeito Trilha OS)

- IA é **copiloto, não protagonista** — no fim, o sistema é teu, construído com o que você sabe.
- Conceito antes de ferramenta. Contexto antes de prompt.
- Comece enxuto. Adicione skill só quando o processo se repetir de verdade.
