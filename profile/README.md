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
cpsize -K                       # → 0    (kilobytes, truncated)
cpclear                         # empty the clipboard
```

Binary-safe. MIME-aware. Survives `| head -1`. Works in scripts, keybindings,
and pipelines without surprises.

[![CI](https://img.shields.io/github/actions/workflow/status/clicraft/cpclip/ci.yml?label=CI&style=flat-square)](https://github.com/clicraft/cpclip/actions/workflows/ci.yml)
[![Tests](https://img.shields.io/badge/tests-70%20passing-brightgreen?style=flat-square)](https://github.com/clicraft/cpclip/actions)
[![License](https://img.shields.io/github/license/clicraft/cpclip?style=flat-square)](https://github.com/clicraft/cpclip/blob/main/LICENSE)

```sh
# Install (Linux, amd64)
curl -fsSL https://raw.githubusercontent.com/clicraft/cpclip/main/install.sh | sh
```

---

*More tools in the works. GPL-2.0-or-later throughout.*
