# Requirements — Modelo de obra e conteúdo (fundação)

**Stakeholder:** Matheus (produto Obras)

## Objetivo

Definir o **modelo de dados genérico** (`Work`) e a **instância CIC** (hierarquia + parágrafos §), com **amostra** de conteúdo para desenvolvimento antes da fonte CNBB 5ª edição estar fechada.

## Contexto do pedido

Plataforma deve servir **qualquer livro** no futuro; v1 valida com o Catecismo. Navegação inspirada em apps de referência (REA), mas a **árvore é do domínio CIC**, não cópia Bíblia livro/capítulo/versículo.

## Perguntas de esclarecimento e respostas (grill-me)

| Pergunta | Resposta |
|----------|----------|
| Entrega v1? | Protótipo **web** navegável (não parity com app comercial). |
| Stack? | **TypeScript + Vite + React**. |
| Hierarquia CIC? | Menu: **Partes I–IV**, **Carta apostólica**, **Constituição apostólica**, **Sumário**. Dentro de cada Parte: **2 Sessões** → **Capítulos** → **Artigos** → **Parágrafos**. |
| Id do parágrafo? | Número oficial **§** (ex. § 255). |
| Fonte do texto? | **CNBB 5ª** (desejada); licença **a verificar** — ver `content/catecismo/SOURCE.md`. Até lá: **amostra** mínima. |
| REA vs. formato final? | Schema CIC **primeiro**; REA informa UX; **não** exportar dump do APK como corpus. |

## User stories

- Como desenvolvedor, quero um **JSON schema documentado** para `Work` reutilizável por outras obras.
- Como leitor, quero que o CIC exponha **§** estáveis e títulos de capítulo/artigo para contexto.
- Como mantenedor, quero **SOURCE.md** registrando pendência de licença antes do import completo.
- Como time, quero **amostra** com pelo menos uma cadeia completa Parte → … → § para testes de UI.

## Fora de escopo

- Import completo do CIC sem `SOURCE.md` aprovado.
- Texto extraído do APK da Bíblia Ave Maria.
- Backend, sync em nuvem, contas de usuário.

## Critérios de aceite

- [ ] `design.md` descreve tipos/nós e IDs canônicos.
- [ ] Arquivo de amostra em `content/catecismo/` (ex. `sample.work.json` ou equivalente) validável pelo leitor (spec 03).
- [ ] `content/catecismo/SOURCE.md` com status pendente e checklist de licença.
- [ ] README ou `specs/README` referencia esta spec como dependência da 03.
