# 🚀 Awesome VS Code Vim Motions & Config

[![VS Code Extension](https://img.shields.io/badge/Extension-VSCodeVim-blue.svg?style=for-the-badge&logo=visual-studio-code)](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Vim Speed](https://img.shields.io/badge/Vim%20Speed-10x-orange.svg?style=for-the-badge)](https://github.com/rudranboitei/awesome-vim-motions)

A curated setup, pocket cheat sheet, and blogging-ready guide to master Vim motions directly inside **Visual Studio Code**. Learn how to configure your IDE to stay on the home row, throw away the mouse, and edit code at the speed of thought.

---

## 📂 Project Structure

*   [settings.json](file:///home/rudra/Documents/awesome-vim-motions/settings.json) — Copy-pasteable VS Code configuration with premium custom navigation bindings.
*   [vim-motion-combos.md](file:///home/rudra/Documents/awesome-vim-motions/vim-motion-combos.md) — Pocket-sized cheatsheet containing the 15 commands developers actually use daily.
*   [VIM-MOTIONS-GUIDE.mdx](file:///home/rudra/Documents/awesome-vim-motions/VIM-MOTIONS-GUIDE.mdx) — MDX-blogging ready guide with custom frontmatter, ready to publish on personal websites.

---

## ⚙️ The VS Code Vim Secret Sauce

Most Vim guides focus on vanilla Vim. This repository is customized specifically for **VS Code**. Here are the custom shortcuts configured in [settings.json](file:///home/rudra/Documents/awesome-vim-motions/settings.json) that bridge the gap:

### 🏠 1. The Home Row Escape
Stop stretching your pinky to the top-left of the keyboard to hit `Esc`.
*   **Insert Mode Binds:** Typing `jk` or `kj` will instantly return you to Normal mode.

### 📑 2. Browser-like Tab Switching (`H` and `L`)
Instead of clicking editor tabs or typing `Ctrl+PageUp`/`PageDown`:
*   Press **`H`** (Shift + h) to move to the **Previous Editor Tab**.
*   Press **`L`** (Shift + l) to move to the **Next Editor Tab**.

### 🧩 3. Split Editor Navigation (`Ctrl + h/j/k/l`)
Navigate multiple files open side-by-side using Vim home keys:
*   `Ctrl + h` ➔ Move focus to split on the **Left**
*   `Ctrl + l` ➔ Move focus to split on the **Right**
*   `Ctrl + j` ➔ Move focus to split **Below**
*   `Ctrl + k` ➔ Move focus to split **Above**

### 👑 4. The Spacebar Leader Key Commands
We map the Vim leader key to `Space` to trigger common VS Code actions instantly:
*   `Space + w` ➔ **Save File** (`Ctrl + S`)
*   `Space + q` ➔ **Close Editor Tab** (`Ctrl + W`)
*   `Space + f` ➔ **Fuzzy Search Files** (QuickOpen/`Ctrl + P`)
*   `Space + e` ➔ **Toggle Explorer Sidebar** (`Ctrl + B`)
*   `Space + n` ➔ **New File** (Creates file in selected explorer folder)
*   `Space + r` ➔ **Rename File** (In explorer tree)
*   `Space + d` ➔ **Delete File** (Moves file to trash)

---

## 🚀 Quick Start Guide

### Step 1: Install the VS Code extension
Search for and install **Vim** by `vscodevim` in the VS Code Marketplace.

### Step 2: Update your VS Code configuration
Open your VS Code `settings.json` (via command palette: `Ctrl + Shift + P` ➔ *Preferences: Open User Settings (JSON)*) and append the configuration from the [settings.json](file:///home/rudra/Documents/awesome-vim-motions/settings.json) file in this repository.

### Step 3: Disable arrow keys (Optional but recommended!)
Force muscle memory by preventing the use of standard arrow keys:
```json
"vim.handleKeys": {
  "<up>": false,
  "<down>": false,
  "<left>": false,
  "<right>": false
}
```

---

## 📚 Vim Motions Beginner-to-Pro Guide

Click the dropdowns below to read the comprehensive, scenario-based tutorials.

<details>
<summary><b>📖 Chapter 1: Basic hjkl Movements</b></summary>

### Understanding Vim Modes
Vim separates typing from navigation. Use these modes:
*   **NORMAL mode** (`Esc` or `jk`): Move around and trigger actions.
*   **INSERT mode** (`i`): Type text normally.
*   **VISUAL mode** (`v`): Select text blocks.

### Basic movements
*   `h` ➔ Left
*   `j` ➔ Down
*   `k` ➔ Up
*   `l` ➔ Right

*Practice:* Try navigating around any file in your workspace using only these keys.
</details>

<details>
<summary><b>📖 Chapter 2 & 3: Word and Line Jumping</b></summary>

### Jump across words
*   `w` ➔ Jump to the **start** of the next word.
*   `b` ➔ Jump **back** to the start of the previous word.
*   `e` ➔ Jump to the **end** of the word.
*   `3w` / `2b` ➔ Combine with numbers to jump multiple words at once.

### Jump across lines
*   `0` ➔ Jump to the absolute **beginning** of the line.
*   `^` ➔ Jump to the **first character** (skipping whitespace).
*   `$` ➔ Jump to the **end** of the line.
</details>

<details>
<summary><b>📖 Chapter 4 & 5: File Navigation & Search</b></summary>

### Scrolling
*   `gg` ➔ Go to top of file.
*   `G` ➔ Go to bottom of file.
*   `:85` ➔ Jump directly to line 85.
*   `Ctrl + d` / `Ctrl + u` ➔ Scroll page Down/Up.

### File-wide Search
*   `/myTerm` ➔ Searches for "myTerm". Hit `Enter`, then press `n` for next match, and `N` for previous match.
*   `*` ➔ Search forward for the word currently under your cursor.
</details>

<details>
<summary><b>📖 Chapter 6 & 7: Deleting & Changing (The powerhouses)</b></summary>

### Editing actions
*   `x` ➔ Delete character under cursor.
*   `dd` ➔ Delete (cut) entire line.
*   `dw` ➔ Delete from cursor to start of next word.
*   `d$` ➔ Delete from cursor to end of line.
*   `cw` ➔ Change word (deletes word, enters INSERT mode).
*   `cc` ➔ Change entire line.
*   `c$` ➔ Change to end of line.

### Inner Text Objects (The Magic)
Type `c` (change), followed by `i` (inner), followed by the delimiter:
*   `ciw` ➔ Change Inner Word (rename variable anywhere).
*   `ci"` ➔ Change inside quotes `""` or `''`.
*   `ci(` ➔ Change inside parentheses `()`.
*   `ci{` ➔ Change inside curly braces `{}`.
*   `cit` ➔ Change inside JSX/HTML tags `<tag>Text</tag>`.
</details>

<details>
<summary><b>📖 Chapter 8 & 9: Copy/Paste & Visual Selection</b></summary>

### Clipboard
*   `yy` ➔ Yank (copy) current line.
*   `p` ➔ Put (paste) after cursor / below line.
*   `P` ➔ Put (paste) before cursor / above line.
*   `dd` ➔ Acts as "cut" command, can be pasted with `p`.

### Selections
*   `v` ➔ Visual character selection.
*   `V` ➔ Visual line-by-line selection.
*   `Ctrl + v` ➔ Visual block selection.
</details>

<details>
<summary><b>📖 Chapter 10 & 11: Undo, Redo, & Repeating (The Dot Operator)</b></summary>

*   `u` ➔ Undo last edit.
*   `Ctrl + r` ➔ Redo last undone change.
*   `.` ➔ **Repeat last edit command** (The single most powerful Vim feature).

#### The Refactoring Workflow:
Need to rename a variable in 5 places?
1. Search for it: `/oldVariable`
2. Change the first one: `ciw` ➔ `newVariable` ➔ `Esc`
3. Jump to the next one: `n`
4. Repeat the rename: `.`
5. Repeat `n .` until done!
</details>

---

## ⚡ The React Developer Cheat Sheet

If you write React/JSX code daily, memorize these 6 combinations:
1.  `cit` ➔ Change JSX inner text (e.g. `<div>Edit Me</div>`).
2.  `ci"` ➔ Edit React prop strings (e.g. `className="..."`).
3.  `ci(` ➔ Change hook parameters (e.g. `useState(...)`).
4.  `ci[` ➔ Change `useEffect` dependency arrays.
5.  `ddp` ➔ Re-order JSX lines or imports (moves line down).
6.  `yyp` ➔ Duplicate components or Tailwind lines.

---

## 📄 License
This repository is released under the [MIT License](file:///home/rudra/Documents/awesome-vim-motions/LICENSE). Feel free to share and copy the configuration!
