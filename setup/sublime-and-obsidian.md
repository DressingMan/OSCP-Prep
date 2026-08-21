# Sublime + Obsidian setup

Short version of the editor (9:13) and notes (26:07) parts of [My Setup, Config and More (Hacking in 2024)](https://www.youtube.com/watch?v=50WggAUjVus). Mac-first.

## Sublime Text

1. Install from [sublimetext.com/download](https://www.sublimetext.com/download) → drag to Applications.
2. Open Sublime → **Tools → Install Command Line Tool**.
3. Confirm:

```bash
which subl
```

4. Add to `~/.zshrc`:

```bash
alias st='subl ~'
alias config='subl ~/.zshrc'
```

5. Reload and test:

```bash
source ~/.zshrc
st        # home folder in Sublime
config    # opens ~/.zshrc
```

Optional (Oh My Zsh): add `sublime` to `plugins=(...)` in `~/.zshrc`, then `source ~/.zshrc`. That gives `st file.md`.

**Kali / Parrot:** `sudo apt install sublime-text` (or Sublime’s [Linux repo](https://www.sublimetext.com/docs/linux_repositories.html)). Use `subl` or `sublime` in the aliases.

## Obsidian

1. Install from [obsidian.md](https://obsidian.md).
2. **Open folder as vault** on a clone of this repo, or keep a local notes vault and copy `templates/` into it.
3. Settings → **Appearance** → Themes → **Manage** → install **Obsidian Nord** → **Use**.
4. Appearance → **Base color scheme** → **Dark** (or Adapt to system).
5. Settings → **Files and links**:
   - Default location for new attachments: **In subfolder under current folder**
   - Subfolder name: `evidence`
6. Test: open a note → screenshot (`Cmd+Ctrl+Shift+4` on Mac) → paste (`Cmd+V`). An `evidence/` folder should appear next to that note.

## Split of work

| Do this in | Tool |
| --- | --- |
| `.zshrc`, scripts, one-off files | Sublime (`st` / `config`) |
| Box notes + screenshots | Obsidian |

Next: [how to structure a box](../README.md#structure-your-own-notes) and [templates](../templates/).
