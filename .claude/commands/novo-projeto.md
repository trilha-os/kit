---
name: novo-projeto
description: >
  Cria a pasta e o contexto de um projeto ou cliente novo, com CLAUDE.md próprio.
  Use quando o usuário chamar /novo-projeto, disser "novo cliente", "começar um projeto",
  "criar pasta pra X".
---

# /novo-projeto — Criar projeto ou cliente novo

Objetivo: criar um espaço de trabalho isolado pra um projeto/cliente, com contexto próprio, e
deixar o sistema sabendo que ele existe.

## Passo a passo

1. Pergunte: é um **cliente** (alguém que você atende) ou um **projeto** seu?
2. Pergunte o nome e, em 1-2 frases, do que se trata e qual o objetivo.
3. Crie a pasta no lugar certo:
   - cliente → `clientes/[nome]/`
   - projeto → `projetos/[nome]/`
4. Crie dentro um `CLAUDE.md` dedicado, curto: o que é, objetivo, o que já se sabe, próximos passos.
5. Adicione no `CLAUDE.md` principal (raiz) uma linha na estrutura de pastas apontando pra esse novo.
6. Se for cliente novo, ofereça registrar em `_contexto/empresa.md`.

## Regras
- O `CLAUDE.md` do projeto é o que dá contexto isolado — não precisa explicar tudo de novo depois.
- Confirme o nome e o local antes de criar.
