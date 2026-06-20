---
name: mapear
description: >
  Transforma um processo repetitivo do teu dia a dia numa skill do Claude.
  Use quando o usuário chamar /mapear, disser "isso eu faço toda semana",
  "queria automatizar isso", "cria uma skill pra isso".
---

# /mapear — Transformar processo em skill

Objetivo: pegar algo que você repete e ensinar o Claude a fazer do teu jeito, virando uma skill.

## Fase 1 — Descobrir

Leia primeiro `_contexto/empresa.md` e `_contexto/preferencias.md` pra entender o negócio.

Pergunte, em conversa (uma de cada vez):
> "Me conta uma coisa que você faz toda semana ou todo mês que toma teu tempo e parece que dava
> pra automatizar. Pode ser produzir conteúdo, mandar proposta, organizar algo — qualquer coisa."

Se a pessoa listar várias, ajude a priorizar pela que mais dói / mais repete.

Pra o processo escolhido, entenda: com que frequência acontece, qual o resultado esperado
(entregável), e o passo a passo de como ela faz hoje.

## Fase 2 — Decidir a base

Antes de criar do zero, ver se dá pra aproveitar algo:
1. Tem skill parecida no núcleo (`carrossel`, `legenda`, `pauta`, `conselho`)? Adapta.
2. Tem uma skill no roadmap (`templates/skills/catalogo.md`) que resolve? Sugere instalar.
3. Se não, criar uma skill nova do zero (usar o skill-creator nativo do Claude).

## Fase 3 — Criar

- Skill específica deste negócio → `.claude/skills/[nome]/SKILL.md` (local).
- Calibrar pelo `_contexto/` (tom, preferências, o que evitar).
- Se precisar de arquivos de apoio (template, referência), criar dentro da pasta da skill.
- Se o processo NÃO for repetível de verdade, dizer isso — não criar skill por criar.

## Regras
- Tom direto, sem enrolação. Perguntas em conversa, não em lista.
- Mostre o plano da skill antes de criar e confirme com a pessoa.
