# Charter — Obras / catecismo-rea

## Visão

Plataforma de **leitura genérica** (`Work` / `Book`): qualquer obra pode substituir outra. Primeiro milestone: **Catecismo da Igreja Católica (CIC)**.

## Princípios

- **Clean room:** implementação e código próprios; REA só para entender comportamento observável em apps de referência.
- **Conteúdo:** texto do CIC a partir de **fonte autorizada** (edição/licença documentada em `content/catecismo/`). Não usar APK como corpus principal.
- **REA:** perguntas estreitas, evidência (`evidence_id`), limitações e `unknowns` registrados.

## Fora de escopo (v1)

- Clonar marca, assets ou textos proprietários de apps de terceiros.
- Redistribuir APK ou dumps.
- “Feature parity” total com app comercial antes do leitor mínimo do CIC.

## Referência REA (Android)

| Campo | Valor |
|-------|--------|
| Play Store | https://play.google.com/store/apps/details?id=tepteev.ihar.biblia_ave_maria.AOUNVFLAKOECSYLY&hl=pt_BR |
| applicationId | `tepteev.ihar.biblia_ave_maria.AOUNVFLAKOECSYLY` |
| Uso | UX: índice, busca, progresso, offline (a confirmar na investigação) |

## Milestones

- [Catecismo v1](milestones/catecismo-v1.md)

## Decisões em aberto

_(Preencher após sessão grill-me / grilling.)_

- Stack alvo (web, mobile, ambos)?
- Formato canônico da obra (parágrafo §, hierarquia)?
- Fonte textual do CIC (edição PT)?
