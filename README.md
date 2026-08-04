# Noir - Omarchy theme

![Noir](icon.png)

A dark Omarchy/Hyprland theme. Pure black background, warm grey text, muted
sage accents. Includes matching Neovim and VS Code themes.

## Screenshots

![Noir desktop](preview.png)

![Noir](preview-unlock.png)

## Contents

| File               | Purpose                                            |
| ------------------ | -------------------------------------------------- |
| `colors.toml`      | Base palette (accent, foreground, ANSI colors)     |
| `neovim.lua`       | Neovim colorscheme spec + plugin                   |
| `vscode.json`      | VS Code theme name + marketplace extension         |
| `btop.theme`       | btop color theme                                   |
| `icons.theme`      | Icon set (noir-sage custom theme)                 |
| `icon.png`         | Theme/logo icon                                    |
| `backgrounds/`     | Wallpapers, sorted; first = default                |
| `preview.png`      | Theme preview for the theme picker (1800x1012)     |
| `preview-unlock.png` | Lock-screen preview (1920x1080)                  |
| `unlock.png`       | Lock-screen preview (800x378)                      |

## Editing this theme

1. Edit any file here.
2. Copy changed files to your live theme dir and reapply:

   ```bash
   cp <files> ~/.config/omarchy/themes/noir/
   omarchy theme set noir
   ```

   Or edit `~/.config/omarchy/themes/noir/` directly (that dir is the live
   source; this repo is the publishable copy).

## Installing

```bash
omarchy theme install https://github.com/tahadx/omarchy-noir-theme.git
```

The theme name (`noir`) is derived from the repo name.

## Icon set

This theme's `icons.theme` sets the GNOME icon theme to **`noir-sage`**, a
custom folder icon theme matching the sage accent. Omarchy only applies the
name, so install the icons once:

```bash
git clone https://github.com/tahadx/noir-sage.git /tmp/noir-sage
/tmp/noir-sage/install.sh
```

Then reapply the theme so the icon setting takes effect:

```bash
omarchy theme set noir
```

Alternatively, point `icons.theme` at any installed Yaru variant (e.g.
`Yaru-dark`) and the theme will use it instead.

## Matching colorschemes

- **Neovim**: `tahadx/noir.nvim` (set as `colorscheme = "noir"` in `neovim.lua`)
- **VS Code**: `tahadx.noir-omarchy` extension (auto-installed by omarchy on theme set)

## License

MIT (c) Taha Sadough 2026
