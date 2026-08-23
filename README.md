# Noir — Omarchy theme

A dark theme for the whole desktop. Pure black background, warm grey text,
muted sage accents. Includes a matching Zed theme, and pairs with the
[noir.nvim](https://github.com/tahadx/noir.nvim) colorscheme for Neovim (manual
step below).

Built for current Omarchy (quattro) and the latest Lua-based Hyprland.
Hyprland colors ship as `hyprland.lua`, applied on top of Omarchy's
defaults by the theme system.

## Install

```bash
omarchy theme install https://github.com/tahadx/omarchy-noir-theme.git
```

Everything colors automatically on `omarchy theme set noir` — except Neovim,
which currently needs one manual step.

## Neovim (manual step)

Omarchy strips `.lua` files from themes installed from a git repo
(introduced in [basecamp/omarchy#7884](https://github.com/basecamp/omarchy/pull/7884),
shipped 2026-08-23), so this theme's `neovim.lua` is not applied and Neovim
falls back to the generic palette render. Until Omarchy provides a channel
for repo themes to ship editor integrations
([basecamp/omarchy#7942](https://github.com/basecamp/omarchy/issues/7942)),
enable the matching colorscheme once by hand.

[noir.nvim](https://github.com/tahadx/noir.nvim) is the companion Neovim
colorscheme (pure_black variant). With LazyVim — Omarchy's default config —
save this as `~/.config/nvim/lua/plugins/noir.lua`:

```lua
return {
  {
    "tahadx/noir.nvim",
    priority = 1000,
    config = true,
    opts = {
      variant = "pure_black",
    },
  },
  {
    "LazyVim/LazyVim",
    opts = {
      colorscheme = "noir",
    },
  },
}
```

Then restart Neovim (or run `:Lazy sync`). The theme hot-reloads on Omarchy
theme switches like before.

## Preview

![Noir preview](preview.png)

## Palette

| Role       | Hex       | Used for               |
| ---------- | --------- | ---------------------- |
| `bg`       | `#000000` | Background             |
| `alt_bg`   | `#1c1c1c` | Panels, hovers, status |
| `fg`       | `#c1c1c1` | Foreground             |
| `comment`  | `#505050` | Comments               |
| `constant` | `#aaaaaa` | Constants, numbers     |
| `func`     | `#888888` | Functions              |
| `keyword`  | `#999999` | Keywords, storage      |
| `operator` | `#9b99a3` | Operators, punctuation |
| `string`   | `#aa9988` | Strings                |
| `type`     | `#777755` | Types, classes         |
| `visual`   | `#333333` | Selection              |
| `accent`   | `#8a9a7b` | Accent, focus, tags    |

## License

MIT
