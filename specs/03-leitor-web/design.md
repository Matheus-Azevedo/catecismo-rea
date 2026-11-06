# Design — Leitor web

## Stack

- Vite + React 18+ + TypeScript
- Roteamento: **React Router** (URLs refletem caminho no work, ex. `/parte/1/sessao/1/capitulo/1/artigo/1/p/255`)
- Estilo: CSS modules ou Tailwind (escolha na implementação; manter simples)
- Dados: import estático de `sample.work.json` no MVP; loader abstrato para futuro `cic.work.json`

## Estrutura `src/` (alvo)

```
src/
  main.tsx
  App.tsx
  domain/work.ts          # tipos + helpers (árvore, busca)
  data/loadWork.ts
  components/
    RootMenu.tsx
    NodeList.tsx
    Reader.tsx
    SearchBar.tsx
  hooks/useReadingPosition.ts
```

## Navegação

- **RootMenu:** filhos diretos de `workId` mapeados para entradas de menu (partes + carta + constituição + sumário).
- **NodeList:** lista filhos do nó atual (título + link).
- **Reader:** exibe § sequenciais do artigo selecionado ou nó folha.

## Busca

- Client-side sobre `nodes` com `body` e `title` (case-insensitive, pt-BR).
- Resultado: `nodeId`, snippet, breadcrumb.

## Posição de leitura

- Chave: `obras.readingPosition.{workId}` → `{ nodeId, paragraphNumber? }`
- Default spec 02: **localStorage** até REA sugerir padrão mais rico (IndexedDB).

## Acessibilidade mínima

- Foco visível, títulos semânticos (`h1`/`h2`), contraste razoável.

## Testes

- Vitest: helpers de árvore + busca (sem E2E obrigatório no MVP).

## Dependências de dados

- `content/catecismo/sample.work.json` (spec 01).
