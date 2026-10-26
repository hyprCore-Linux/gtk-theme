# gtk-theme

Shared color profiles and UI chrome for the hyprCore Linux GTK apps (Rust crate + Python helpers).

Provides built-in and custom profiles, the suite **Profile** / About menu, Adwaita icon helpers, and theming utilities used by every `gtk-*` app.

Created by Kevin Hinds

## Layout

| Path | Role |
|------|------|
| `src/` | Rust library (`gtk-theme`) |
| `python/gtk_theme.py` | Python helpers for GTK4 apps |
| `profiles.json` | Built-in color profiles (**hyprCore Linux** first, plus well-known themes) |

Active profile selection lives in `~/.config/gtk-apps/theme.toml`; chrome overrides for hyprCore Linux (and any user-saved customs) live in `~/.config/gtk-apps/custom-profiles.json`.

## Use from Rust

Add a path dependency from a suite app:

```toml
gtk-theme = { path = "../gtk-theme" }
```

## Use from Python

```python
import sys
from pathlib import Path
sys.path.insert(0, str(Path(__file__).resolve().parent.parent / "gtk-theme" / "python"))
import gtk_theme
```

## License

GNU General Public License v3.0. See [LICENSE](LICENSE).
