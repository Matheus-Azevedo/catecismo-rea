# Instruções do projeto (Obras — catecismo-rea)

## Sobre o projeto

**Leitor genérico de obras** (`Work`); primeiro conteúdo: **Catecismo da Igreja Católica (CIC)** em pt-BR. Desenvolvimento guiado por **Spec-Driven Development**: implemente apenas o que está em `specs/`; `requirements.md`, `design.md` e `tasks.md` de cada pasta são a fonte da verdade.

Investigação do app **Bíblia Ave Maria** (Android) usa **REA** em clean room — só mecânica de leitor, nunca corpus de texto do APK.

## Regras não negociáveis

- **Conteúdo:** texto do CIC só de fonte declarada em `content/catecismo/SOURCE.md`. APK **não** é fonte de texto.
- **REA:** uma pergunta estreita por sessão; salvar Evidence em `evidence/` (JSON gitignored por padrão; relatórios sanitizados podem ir em `docs/`).
- **APK / artifacts:** nunca commitar em `artifacts/` (local only).
- **Código:** TypeScript strict, **Vite + React** em `src/` (spec `03-leitor-web`).
- **Domínio CIC:** árvore Parte → Sessão (×2) → Capítulo → Artigo → Parágrafo (§); menu raiz inclui Carta apostólica, Constituição apostólica e Sumário — **não** copiar schema livro/capítulo/versículo do app de referência.
- **UI:** pt-BR; sem clonar marca ou assets do app comercial.

## Como trabalhar neste repositório

1. Antes de codar, leia `specs/<pasta>/requirements.md`, `design.md` e `tasks.md`.
2. Consulte `docs/notas-artefato-android.md` para versão/hash do APK de referência.
3. Não implemente fora da spec. Ambiguidade → pare e pergunte.
4. Ordem: `01-modelo-obra` → `02-rea-referencia` (paralelo possível após schema mínimo) → `03-leitor-web`.
5. Comandos Cursor (workspace **`Obras/`**): `/cic-spec-01`, `/cic-spec-02-rea`, `/cic-spec-03`, `/cic-review`, `/cic-explore` — ver `../.cursor/commands/cic-*.md` e `../README.md`.
6. Referência: `prompts.md`.

## Visão resumida

Detalhes de produto e decisões da entrevista (grill-me): `docs/CHARTER.md` (índice); especificação completa: `specs/`.
