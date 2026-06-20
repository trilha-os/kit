---
name: syncar
description: >
  Salva teu trabalho no GitHub (backup) e configura o git na primeira vez.
  Use quando o usuário chamar /syncar, disser "salva no github", "faz backup", "commit",
  "não quero perder meu trabalho".
---

# /syncar — Backup no GitHub

Objetivo: garantir que o teu sistema nunca se perca. Na primeira vez, configura tudo; depois,
é só salvar.

## Primeira vez (configurar)

1. Verifique se já existe repositório git nesta pasta (`git status`). Se não:
2. Pergunte se a pessoa tem conta no GitHub. Se não tiver, oriente criar em github.com (grátis).
3. Confirme que o `.gitignore` protege o `.env` (chaves nunca sobem).
4. Crie um repositório **privado** e faça o primeiro push. Use o `gh` se disponível; senão,
   guie a pessoa pelos comandos mínimos.

## Toda vez (salvar)

1. `git add -A`
2. Commit com mensagem curta do que mudou.
3. `git push`.
4. Confirme com uma linha: "Salvo. Teu trabalho tá seguro no GitHub."

## Regras
- Nunca subir `.env` ou chaves. Conferir o `.gitignore` antes do primeiro push.
- Repositório sempre privado por padrão.
