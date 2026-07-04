# Perfil — Empreendedor Criativo

Perfil-base do aluno Trilha OS: designer, arquiteto, fotógrafo, produtor de conteúdo ou dono
de pequeno estúdio/agência em transição de criativo pra empreendedor. Opera sozinho ou com
equipe pequena. Trabalha com **imagem**, não com código. Gargalo comum: **tempo** — faz na mão
o que poderia operar com copiloto. Costuma **não pensar o próprio trabalho como empresa** — por
isso a estrutura de pastas serve também pra ensinar: cada pasta mostra onde mora cada pilar.

## Estrutura de pastas (mapeada aos 4 pilares)

```
_contexto/        ▸ GESTÃO     o cérebro do negócio (empresa, foco, preferências)
ideias/           ▸ GESTÃO     inbox: ideia crua entra aqui, vira pauta/projeto depois
tarefas.md        ▸ GESTÃO     o que precisa ser feito

conteudo/         ▸ MARKETING  carrosseis/ · posts/ · roteiros/
                               (pauta, legenda e carrossel moram aqui)

marca/            ▸ IMAGEM     design-guide + a tua identidade visual
referencias/      ▸ IMAGEM     moodboard: inspirações, paletas, prints que você guarda

clientes/         ▸ VENDAS     um por cliente → briefing → proposta → entrega
  _modelo/                     template (briefing.md + proposta.md)
precos/           ▸ VENDAS     precificação, o que você cobra (a dor do criativo)

projetos/         ▸ trabalhos maiores / portfólio (um por trabalho ou por peça)
dados/            ▸ análise    prints de métrica, planilhas — jogue aqui pra analisar
```

`ideias/`, `referencias/` e `dados/` já vêm no kit (cada uma com um README). O resto o `/setup`
cria conforme o gargalo do aluno.

## Ordem por gargalo
A sequência das pastas (e por onde a trilha começa) segue o **pilar que mais trava**:
- Trava em **Marketing** → `conteudo/` e `referencias/` no topo.
- Trava em **Vendas** → `clientes/` e `precos/` primeiro.
- Trava em **Gestão** → `_contexto/`, `ideias/`, `tarefas.md`, `/iniciar` e `/conselho`.
- Trava em **Imagem** → `marca/` e `referencias/`, com produção visual.

## Vocabulário (falar a língua do criativo)
No CLAUDE.md e nas perguntas do `/setup`, usar a linguagem de quem cria, não jargão corporativo:
"quantos **projetos** por mês", "quanto você **cobra** por trabalho / por hora", "quem são teus
**clientes**" — evitar MRR, CAC, faturamento, ticket. O aluno é criativo, não gestor de planilha.

## Ferramentas típicas
Claude.ai + Claude Code, Instagram, Canva/Figma, Cloudflare Pages (páginas grátis),
geração de imagem (Nano Banana / Gemini). Ver `templates/ferramentas/catalogo.md`.
