# Charter — Obras / catecismo-rea

_Índice executivo. Especificação completa: [`specs/`](../specs/README.md)._

## Visão

Plataforma **genérica de leitura**; milestone v1: **CIC** (pt-BR), protótipo web.

## Decisões (grill-me, 2026-11)

| Tema | Decisão |
|------|---------|
| Entrega v1 | Protótipo web navegável |
| Stack | TypeScript + Vite + React |
| Hierarquia CIC | Partes I–IV (+ Carta, Constituição, Sumário) → 2 Sessões → Capítulos → Artigos → § |
| Conteúdo | CNBB 5ª desejada; licença **pendente** (`content/catecismo/SOURCE.md`) |
| REA | Mecânica do app referência; schema CIC **próprio** |
| Repo | Público; APK só local |

## Specs

1. [01-modelo-obra](../specs/01-modelo-obra/requirements.md)
2. [02-rea-referencia](../specs/02-rea-referencia/requirements.md)
3. [03-leitor-web](../specs/03-leitor-web/requirements.md)

## Fluxo de trabalho

1. Implementar specs em ordem (ver `AGENTS.md`).
2. REA: uma pergunta por sessão → `evidence/` + `docs/notas-rea.md`.
3. Conteúdo completo só após `SOURCE.md` aprovado.

## Milestone legado

Detalhe histórico do milestone v1: [`milestones/catecismo-v1.md`](milestones/catecismo-v1.md) (referencia as specs acima).
