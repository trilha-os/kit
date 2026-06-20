---
name: atualizar
description: >
  Sincroniza os arquivos de contexto quando algo mudou no negócio.
  Use quando o usuário chamar /atualizar, disser "atualiza o contexto", "muita coisa mudou",
  ou ao fim de uma sessão de trabalho grande.
---

# /atualizar — Sincronizar contexto

Objetivo: manter o `CLAUDE.md` e o `_contexto/` em dia com o que mudou de verdade.

## Passo a passo

1. Olhe o que aconteceu na sessão (ou pergunte o que mudou).
2. Identifique o que precisa atualizar:
   - Novo cliente/serviço/ferramenta/equipe → `_contexto/empresa.md`
   - Mudança de prioridade/foco → `_contexto/estrategia.md`
   - Correção de tom/estilo → `_contexto/preferencias.md`
   - Nova pasta, regra de organização, skill criada → `CLAUDE.md`
   - Mudança visual (cor, fonte, logo) → `marca/design-guide.md`
3. **Mostre o que vai mudar antes de salvar.** Não reformate o arquivo inteiro — só a linha relevante.

## Quando NÃO atualizar
- Tarefa pontual que não muda o contexto (um post, um email avulso).
- Conversa sem ação.
