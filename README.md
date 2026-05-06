# ts-runtime

Runtime local para usar Tree-sitter del core de Neovim sin depender de `nvim-treesitter` ni ensuciar el repo principal de dotfiles.

## Qué instala

- parsers compilados en `~/.local/share/nvim/site/parser/`
- queries en `~/.local/share/nvim/site/queries/`

## Lenguajes incluidos

- rust
- markdown
- markdown_inline
- html
- css
- javascript
- typescript
- tsx
- svelte
- go
- c
- cpp
- c_sharp
- python
- `javascriptreact` / JSX vía mapeo al parser `javascript`
- `typescriptreact` / TSX vía mapeo al parser `tsx`

## Requisitos

- `git`
- `cc`
- `curl`
- `tar`

## Uso

```bash
./scripts/install
```

Para reinstalar todo limpiando el runtime local:

```bash
./scripts/install --clean
```

## Notas

- Este repo administra artefactos de runtime, no la config de Neovim.
- `gdscript` no quedó automatizado todavía porque su parser no tiene una fuente estándar tan estable como el resto.
- `javascriptreact` queda cubierto mapeando ese filetype al parser `javascript` desde tu config de Neovim.
- `typescriptreact` queda cubierto mapeando ese filetype al parser `tsx` desde tu config de Neovim.
