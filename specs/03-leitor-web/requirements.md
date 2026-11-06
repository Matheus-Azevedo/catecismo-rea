# Requirements — Leitor web (MVP CIC)

**Stakeholder:** Matheus (produto Obras)

## Objetivo

Protótipo **Vite + React + TypeScript** que carrega `content/catecismo/sample.work.json`, oferece **menu raiz**, **navegação hierárquica**, **leitura de §**, **busca** e **retomada da última posição** — alinhado ao modelo spec 01 e informado por spec 02 quando disponível.

## User stories

- Como leitor, abro o app e vejo **Partes I–IV**, Carta, Constituição e Sumário.
- Entro em Parte I → Sessão → Capítulo → Artigo → vejo parágrafos com **§** e texto.
- Uso **busca** por termo no corpo/títulos da amostra (e futuro corpus).
- Ao sair e voltar, **retomo** o último § visitado (persistência local).
- Interface em **pt-BR**, layout simples (mobile-friendly desejável, desktop ok).

## Fora de escopo (v1)

- PWA instalável, sync, login, temas avançados, áudio.
- Import CNBB completo (spec futura).
- Parity visual com Bíblia Ave Maria.

## Critérios de aceite

- [ ] `npm run dev` sobe app; `npm run build` passa.
- [ ] Menu raiz conforme ordem em spec 01 design.
- [ ] Drill-down até parágrafo funcional na amostra.
- [ ] Busca retorna resultados clicáveis.
- [ ] Última posição persiste após reload (localStorage ou equivalente documentado).
- [ ] Sem credenciais ou APK no bundle.
