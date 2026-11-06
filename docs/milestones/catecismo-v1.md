# Milestone — Catecismo v1

## Objetivo

Entregar um **leitor mínimo** do CIC sobre o modelo genérico de obras, provando que outro livro pode ser plugado depois sem reescrever o núcleo.

## Entregáveis

- [ ] Modelo de dados `Work` + divisões (parte / seção / parágrafo ou equivalente)
- [ ] Import do CIC em `content/catecismo/` (fonte documentada)
- [ ] Leitura contínua + índice navegável
- [ ] Busca full-text no conteúdo importado
- [ ] Última posição / marcador local

## Investigação REA (referência app)

Perguntas iniciais (uma por sessão):

1. Como o app estrutura **índice e navegação** entre seções?
2. Como funciona **busca** (local, índice, SQLite)?
3. Há **offline** e onde persiste estado?

Artefatos: APK em `artifacts/` (local, gitignored). Evidência em `evidence/`.

## Critério de pronto

Usuário consegue ler um parágrafo do CIC, voltar ao índice, buscar um termo e retomar a leitura na posição anterior — sem depender do app de referência.
