# Requirements — Investigação REA (app de referência)

**Stakeholder:** Matheus (produto Obras)

## Objetivo

Obter **evidência técnica** sobre mecânica de **leitor** no app Android Bíblia Ave Maria (v5.9.0 local), para informar UX do produto Obras **sem** copiar texto, marca ou schema bíblico.

## Contexto

APK extraído do aparelho do usuário; metadados em `docs/notas-artefato-android.md`. Ferramenta: **REA** (MCP ou CLI). Clean room documentado em `docs/notas-rea.md`.

## Escopo REA (permitido)

- Índice / menu hierárquico e navegação.
- Persistência (última posição, favoritos, preferências locais).
- Busca local (mecanismo, índice, storage).
- Offline / cache (se existir).

## Fora de escopo REA

- Extrair ou republicar texto bíblico ou assets proprietários.
- Tratar saída REA como schema de dados do CIC.
- Múltiplas perguntas na mesma sessão (uma pergunta estreita por sessão).

## Sessões planejadas

| # | Pergunta |
|---|----------|
| 1 | Como o app monta o **menu/índice hierárquico** e **persiste a última posição** de leitura (tabelas, arquivos, APIs locais)? |
| 2 | Como funciona a **busca** (índice, SQLite, full-text)? |
| 3 | Há **offline/cache** de conteúdo ou só metadados? Onde? |

## User stories

- Como implementador, quero **Evidence** salva em `evidence/` com caminho absoluto do APK registrado.
- Como arquiteto, quero **notas-rea.md** separando **observado** vs. **inferido** vs. **desconhecido**.
- Como produto, quero tabela **mapeamento UX** (adotar / inspirar / descartar) antes de fechar spec 03.

## Pré-requisitos técnicos

- REA MCP configurado no Cursor **ou** CLI `rea`.
- Android: `inspect_android_package` / JADX conforme doctor REA (JDK + JAR se exigido).

## Critérios de aceite

- [ ] Sessão 1 concluída: Evidence + linha em `docs/notas-rea.md` + rascunho de mapeamento UX.
- [ ] Sessões 2 e 3: idem ou explicitamente **N/A** com motivo na nota.
- [ ] Nenhum texto sagrado commitado a partir do APK.
- [ ] Decisões de produto derivadas citam evidence_id ou arquivo em `evidence/`.
