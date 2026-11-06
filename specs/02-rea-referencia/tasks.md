# Tasks — Investigação REA

## Tasks

- [ ] `rea doctor --client cursor --json` — registrar gaps (Ghidra/JADX) em notas se houver
- [ ] Sessão 1: índice + última posição → Evidence + `notas-rea.md`
- [ ] Sessão 2: busca
- [ ] Sessão 3: offline/cache
- [ ] Preencher **Mapeamento UX → produto Obras** em `notas-rea.md`
- [ ] Revisar spec `03-leitor-web/design.md` e ajustar decisões de persistência/busca se necessário

## Dependências

- **01-modelo-obra:** pode rodar **em paralelo** após schema mínimo definido (esta spec não altera JSON do CIC).
- **03-leitor-web:** deve consumir mapeamento UX da sessão 1 antes de fechar persistência/navegação (sessões 2–3 podem seguir depois do MVP).
