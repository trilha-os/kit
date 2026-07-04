# Trilha OS — Kit de boas-vindas

O teu sistema operacional pra rodar o negócio com o Claude de sócio. Pastas + skills + contexto,
prontos pra você começar a operar — não um curso de ferramenta, um jeito de trabalhar.

## Instalar (do jeito fácil)

Você não precisa saber nada de terminal. Abra o Claude Code numa pasta nova e cole este prompt:

```
Instala pra mim o repositório https://github.com/notkerstens1/trilha-os-kit nesta pasta,
abre a pasta e roda /setup.
```

O Claude clona o kit, abre tudo e começa a te entrevistar pra configurar o sistema pro teu negócio.

## Instalar (manual, se preferir)

1. Tenha o **Claude Code** e o **VS Code** instalados (a aula 01.1 mostra o passo a passo).
2. Numa pasta nova, abra o Claude Code.
3. Rode:
   ```
   git clone https://github.com/notkerstens1/trilha-os-kit.git .
   ```
4. No Claude Code, rode `/setup` e responda as perguntas.

## Primeiros passos depois de instalar

1. **`/setup`** — configura o sistema pro teu negócio (te entrevista, gera teu contexto e tuas pastas).
2. **`/iniciar`** — carrega teu contexto no começo de cada sessão de trabalho.
3. **`/mapear`** — pega um processo repetitivo teu e vira uma skill.
4. **`/syncar`** — conecta no GitHub pra nunca perder teu trabalho.

## O que vem aqui dentro

- `CLAUDE.md` — o cérebro: o Claude lê isso toda vez que você fala com ele.
- `.claude/commands/` — comandos do dia a dia (`/setup`, `/iniciar`, `/mapear`, `/novo-projeto`, `/atualizar`, `/syncar`).
- `.claude/skills/` — núcleo de skills (carrossel, legenda, pauta, conselho).
- `_contexto/` — quem você é, tuas preferências, teu foco (preenchido no `/setup`).
- `marca/design-guide.md` — tua identidade visual (o Claude usa em tudo que é visual).
- `ideias/` — inbox pra ideia crua não se perder (vira pauta/projeto depois).
- `referencias/` — teu moodboard: inspirações, paletas, prints que você guarda.
- `dados/` — jogue aqui print de métrica, planilha, PDF pro Claude analisar.
- `templates/` — perfis, catálogo de ferramentas e o roadmap das skills que chegam por aula.

As pastas de trabalho (`conteudo/`, `clientes/`, `precos/`, `projetos/`) o `/setup` cria pra
você, na ordem do teu gargalo. Cada pasta é um dos 4 pilares — ver o mapa no `CLAUDE.md`.

> **Importante:** o kit é enxuto de propósito. A gente entrega novas skills ao longo das aulas pra
> você ir acrescentando — instale só o que for usar. Ver `templates/skills/catalogo.md`.

## Segurança

Chaves de API vão sempre num arquivo `.env` (já protegido pelo `.gitignore`, nunca sobe pro GitHub).
Use o `.env.example` como modelo.
