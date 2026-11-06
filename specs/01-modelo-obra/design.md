# Design — Modelo de obra e conteúdo

## Visão geral

Um **Work** é uma obra versionada. Nós formam árvore com `kind` discriminando nível. Folhas de leitura contínua são **Parágrafos** com corpo textual.

## Tipos de nó (`NodeKind`)

| kind | Uso CIC v1 | Filhos |
|------|------------|--------|
| `root_menu` | Container lógico da app (opcional no JSON) | entradas de menu |
| `parte` | Parte I … IV | `sessao` (exactamente 2 por parte, validado no import) |
| `carta_apostolica` | Carta apostólica | blocos de texto ou subseções |
| `constituicao_apostolica` | Constituição apostólica | idem |
| `sumario` | Sumário (fim da obra) | entradas indexadas |
| `sessao` | Sessão dentro da parte | `capitulo` |
| `capitulo` | Capítulo | `artigo` |
| `artigo` | Artigo | `paragrafo` |
| `paragrafo` | Unidade § | _folha_ |

## Identificadores

- `workId`: ex. `cic`
- `nodeId`: estável, único no work — ex. `cic:parte-1`, `cic:p-255`
- `paragraphNumber`: inteiro do **§** quando `kind === paragrafo`
- Exibição: `§ {paragraphNumber}`

## Modelo (TypeScript conceitual)

```typescript
interface Work {
  workId: string;
  title: string;
  locale: string; // "pt-BR"
  version?: string; // ex. rascunho amostra
  nodes: WorkNode[];
}

interface WorkNode {
  nodeId: string;
  kind: NodeKind;
  title: string;
  order: number;
  parentId: string | null;
  paragraphNumber?: number;
  body?: string; // só parágrafo (ou blocos simples carta/sumário)
}
```

## Menu raiz (UX)

Ordem sugerida na UI (spec 03):

1. Parte I … IV  
2. Carta apostólica  
3. Constituição apostólica  
4. Sumário  

## Amostra de conteúdo

- Arquivo: `content/catecismo/sample.work.json` (nome fixo na implementação).
- Deve incluir: 1 parte (ou stub), 1 sessão, 1 capítulo, 1 artigo, **≥ 3 parágrafos** com § fictícios ou de domínio público **explicitamente marcados como amostra** em `title`/`version`.
- Quando CNBB 5ª for importada, substituir por `cic.work.json` (ou pipeline) sem mudar contrato `Work`.

## Validação

- `parentId` referencia nó existente.
- `order` único entre irmãos.
- Parágrafos têm `paragraphNumber` e `body` não vazio.

## Riscos / pontos em aberto

- Carta / Constituição / Sumário podem não seguir Parte→Sessão→… — modelar como subárvore própria sob `kind` dedicado.
- Import CNBB: mapeamento editorial (numeração §) — spec futura `04-import-conteudo` se necessário.
