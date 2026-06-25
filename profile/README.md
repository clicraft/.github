# clicraft

**Minimal, composable CLI tools for Linux.**

Single-purpose utilities that do one thing well — binary-safe, scriptable,
and built to compose with the rest of your shell.

---

## Tools

### [`cpclip`](https://github.com/clicraft/cpclip) — clipboard for the command line

One binary, seven commands. Copies, pastes, appends, and reports clipboard
content on both **X11 and Wayland** with identical syntax.

```sh
echo "hello world" | cpclip    # copy to clipboard
cppaste                         # paste to stdout
echo "and more" | cpadd         # append (with newline separator)
cpsize                          # → 28   (bytes in clipboard)
cpclear                         # empty the clipboard
```

Binary-safe. MIME-aware. Survives `| head -1`. Works in scripts, keybindings,
and pipelines without surprises.

[![CI](https://img.shields.io/github/actions/workflow/status/clicraft/cpclip/ci.yml?label=CI&style=flat-square)](https://github.com/clicraft/cpclip/actions/workflows/ci.yml)
[![Tests](https://img.shields.io/badge/tests-70%20passing-brightgreen?style=flat-square)](https://github.com/clicraft/cpclip/actions)
[![License](https://img.shields.io/github/license/clicraft/cpclip?style=flat-square)](https://github.com/clicraft/cpclip/blob/main/LICENSE)

```sh
curl -fsSL https://raw.githubusercontent.com/clicraft/cpclip/main/install.sh | sh
```

---

### [`mdink`](https://github.com/clicraft/mdink) — terminal markdown renderer

Reads a Markdown file and renders it beautifully in your terminal — syntax-highlighted
code blocks, tables, nested lists, task lists, block quotes, and images
(Sixel / Kitty / iTerm2 / half-block fallback, or `--ascii-images` for every terminal).

```sh
mdink README.md
mdink --ascii-images doc/guide.md   # images as Unicode half-block art
```

Built in Rust on [ratatui](https://ratatui.rs) and [syntect](https://github.com/trishume/syntect) (40+ languages, base16-ocean theme).
Keyboard navigation (`j`/`k`, `d`/`u`, `g`/`G`) and a toggleable outline panel (`o`).

[![License](https://img.shields.io/github/license/clicraft/mdink?style=flat-square)](https://github.com/clicraft/mdink/blob/main/LICENSE)

```sh
cargo install mdink
```

---

### [`ghw` / `glw`](https://github.com/clicraft/ghw-github-actions-watcher) — CI watcher

Terminal UI for monitoring CI/CD pipelines without leaving the keyboard.
`ghw` watches **GitHub Actions**; `glw` watches **GitLab CI**.

```sh
ghw          # live workflow list for the current repo
glw          # same for GitLab CI
```

Live-updating tree view (runs → jobs → steps), failure log viewer, cancel/retry
actions, desktop notifications on status changes, and direct browser open.
Adaptive polling: 3 s when active, 30 s when idle.

[![License](https://img.shields.io/github/license/clicraft/ghw-github-actions-watcher?style=flat-square)](https://github.com/clicraft/ghw-github-actions-watcher/blob/main/LICENSE)

```sh
curl -sSL https://raw.githubusercontent.com/clicraft/ghw-github-actions-watcher/master/install.sh | sh
```

---

*GPL-2.0-or-later / MIT throughout.*
