---
name: iniciar
description: >
  Começa a sessão de trabalho carregando o contexto do teu negócio. Use no início de cada
  conversa nova no Claude Code. Lê _contexto/ + tarefas e devolve um resumo curto de onde você
  está e o que fazer hoje. Dispara com /iniciar ou "vamos começar", "carrega o contexto".
---

# /iniciar — carrega o teu Trilha OS

Use no começo de cada sessão. O objetivo é o Claude entrar já sabendo do teu negócio, sem você
ter que explicar tudo de novo.

## O que fazer

1. Ver se `_contexto/empresa.md` está preenchido de verdade (não só o template).
2. Ler `_contexto/empresa.md`, `_contexto/preferencias.md` e `_contexto/estrategia.md`.
3. Se existir `_contexto/diagnostico.md` (gerado pelo `/diagnostico`), ler também — é o gargalo e a trilha de aulas do aluno.
4. Ler o `CLAUDE.md` se existir.
5. Se houver `tarefas.md`, pegar os itens abertos.
6. Devolver um resumo curto e perguntar o que a pessoa quer fazer.

## Fluxo

### Se o contexto está configurado

Leia os três arquivos de `_contexto/` e devolva um resumo **de no máximo 5 linhas**, no formato:

```
Contexto carregado.

**Negócio:** [nome e o que faz, em uma linha]
**Foco agora:** [prioridade principal de estrategia.md — omitir a linha se não tiver]
**Gargalo + trilha:** [de diagnostico.md, se existir: o pilar que trava e a próxima aula do caminho — omitir se não tiver]
**Pra lembrar:** [preferência importante, ex: "sem travessão", "tom oral"]
**Aberto:** [até 3 itens de tarefas.md, se houver]

O que você quer atacar hoje?
```

Não reescreva tudo que está nos arquivos — só o essencial. Se existir `_contexto/diagnostico.md`,
use o **gargalo** e a **próxima aula da trilha** pra sugerir por onde começar. Sem ele, use o
gargalo registrado em `_contexto/empresa.md`.

### Se o contexto NÃO está configurado

```
O sistema ainda não foi configurado pro teu negócio.
Roda /setup primeiro — leva uns 5 minutos e o Claude aprende quem você é.
Depois disso, o /iniciar carrega tudo automático toda vez que você abrir.
```

## Comportamento
- Tom direto e humano. Nada de "Olá! Fico muito feliz em ajudar!".
- Não liste os arquivos que leu — só mostre o que importa.
- Depois do resumo, espere a pessoa dizer o que quer fazer.
