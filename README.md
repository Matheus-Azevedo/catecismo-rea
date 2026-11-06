# catecismo-rea

Leitor de obras (genérico) com primeiro milestone: **Catecismo da Igreja Católica**.

Investigação técnica com [REA](https://rea.tools/) sobre apps de referência (ex.: leitores Android) para orientar UX e arquitetura em **clean room**. O texto do Catecismo entra por fonte autorizada e estrutura própria — não por extração de APK.

## Estrutura

| Pasta | Uso |
|-------|-----|
| `docs/` | Charter, milestones, notas de investigação |
| `content/catecismo/` | Obra estruturada (fonte legal) |
| `evidence/` | Exports e notas REA |
| `artifacts/` | APKs locais (não versionados) |
| `src/` | Implementação do leitor |

## Referência Play Store (REA)

- App de referência UX: [Bíblia Ave Maria](https://play.google.com/store/apps/details?id=tepteev.ihar.biblia_ave_maria.AOUNVFLAKOECSYLY&hl=pt_BR)
- `applicationId`: `tepteev.ihar.biblia_ave_maria.AOUNVFLAKOECSYLY`

## Desenvolvimento

Documentação de escopo: [`docs/CHARTER.md`](docs/CHARTER.md).
