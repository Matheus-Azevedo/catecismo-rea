# catecismo-rea

Leitor **genérico de obras** (`Work`); primeiro conteúdo: **Catecismo da Igreja Católica (CIC)** em pt-BR.

Desenvolvimento **Spec-Driven Development (SDD)** (mesmo padrão do case *novadrive-dashboard*): implemente na ordem das specs; **requirements / design / tasks** são a fonte da verdade.

Investigação **REA** (clean room) sobre app Android de referência — UX de leitor, não corpus de texto.

## Estrutura SDD

```
specs/01-modelo-obra/       # Schema Work + amostra CIC
specs/02-rea-referencia/    # Sessões REA + notas
specs/03-leitor-web/         # Protótipo Vite + React
docs/CHARTER.md             # Visão e decisões (índice)
docs/notas-artefato-android.md
docs/notas-rea.md
AGENTS.md                     # Regras para o agente Cursor
prompts.md
content/catecismo/
evidence/                     # REA (local)
artifacts/                    # APK (local, gitignored)
src/                          # Implementação (spec 03)
```

Ordem: **01 → 02** (paralelo possível) **→ 03**. Detalhes em [`specs/README.md`](specs/README.md).

## Referência Play Store (REA)

- [Bíblia Ave Maria](https://play.google.com/store/apps/details?id=tepteev.ihar.biblia_ave_maria.AOUNVFLAKOECSYLY&hl=pt_BR)
- APK local v5.9.0: ver `docs/notas-artefato-android.md`

## Desenvolvimento

_(Stack e comandos aparecem após implementação da spec 03.)_

```bash
# Exemplo futuro:
npm install
npm run dev
```

## Conteúdo

Fonte CNBB 5ª edição: pendente — `content/catecismo/SOURCE.md`.
