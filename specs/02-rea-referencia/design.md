# Design — Investigação REA

## Fluxo por sessão

1. Ler pergunta da tabela em `requirements.md`.
2. Abrir alvo: `artifacts/biblia-ave-maria-5.9.0-base.apk` (+ split `pt` se necessário).
3. REA: inventário → classes/métodos relevantes → evidência (sem executar app além do que a tool exige).
4. Export JSON para `evidence/YYYY-MM-DD-<tema>.json` (local).
5. Atualizar `docs/notas-rea.md` (human-readable).
6. Atualizar seção **Mapeamento UX** em `docs/notas-rea.md`.

## Artefatos

| Artefato | Local |
|----------|--------|
| APK | `artifacts/` |
| Evidence bruta | `evidence/` (gitignore JSON) |
| Síntese | `docs/notas-rea.md` |
| Metadados APK | `docs/notas-artefato-android.md` |

## Mapeamento UX (template)

Para cada padrão observado:

- **Observado:** (fato com referência Evidence)
- **Proposta Obras:** adotar | inspirar | descartar
- **Notas CIC:** diferença vs. Parte/Sessão/Capítulo/Artigo/§

## Relação com spec 01

Schema JSON do CIC **não** é gerado pelo REA. REA só alimenta decisões de **spec 03** (ex.: usar localStorage vs. IndexedDB para posição).

## Riscos

- JADX/JDK não configurados → sessão bloqueada; registrar em notas e usar doctor.
- App ofuscado → pseudocode limitado; aumentar `unknowns`.
- Splits APK → analisar base primeiro.
