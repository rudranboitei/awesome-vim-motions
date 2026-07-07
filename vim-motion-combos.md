# ⚡ Vim Motion Pocket Reference Cheatsheet

A developer-focused cheat sheet designed to be kept open on a second screen or printed. Focuses on the 20% of commands that yield 80% of the speed gains.

---

## 🛠️ Custom VS Code Vim Configuration

These bindings are defined in [settings.json](file:///home/rudra/Documents/awesome-vim-motions/settings.json) and optimize VS Code navigation.

| Shortcut | Action | VS Code Command / Description |
| :--- | :--- | :--- |
| `jk` or `kj` | `<Esc>` | Exit Insert mode back to Normal mode (Home Row escape) |
| `Space` | `<leader>` | The primary custom leader key |
| `Space + w` | Save File | `workbench.action.files.save` |
| `Space + q` | Close Tab | `workbench.action.closeActiveEditor` |
| `Space + f` | Fuzzy File Search | `workbench.action.quickOpen` (QuickOpen explorer) |
| `Space + e` | Focus Explorer Tree | `workbench.view.explorer` (Open project sidebar) |
| `Space + n` | New File | `explorer.newFile` (Create file in current directory) |
| `Space + r` | Rename File | `renameFile` (Rename file in sidebar explorer) |
| `Space + d` | Delete File | `deleteFile` (Send file to trash) |
| `H` | Prev Editor Tab | `workbench.action.previousEditor` (Switch to left tab) |
| `L` | Next Editor Tab | `workbench.action.nextEditor` (Switch to right tab) |
| `Ctrl + h` | Focus Left Split | `workbench.action.focusLeftGroup` |
| `Ctrl + l` | Focus Right Split | `workbench.action.focusRightGroup` |
| `Ctrl + j` | Focus Below Split | `workbench.action.focusBelowGroup` |
| `Ctrl + k` | Focus Above Split | `workbench.action.focusAboveGroup` |

---

## 🏃 1. Essential Navigation

Move across words and documents instantly.

| Command | Action | Description |
| :--- | :--- | :--- |
| `h` / `j` / `k` / `l` | Left / Down / Up / Right | Basic character and line movements |
| `w` | Next Word | Jump to start of the next word |
| `b` | Previous Word | Jump back to start of the previous word |
| `e` | End of Word | Jump to the end of the current or next word |
| `0` | Start of Line | Jump to absolute column 0 |
| `^` | First Text Character | Jump to the first non-whitespace character on the line |
| `$` | End of Line | Jump to the end of the current line |
| `gg` | Top of File | Jump to line 1 |
| `G` | Bottom of File | Jump to the very last line of the file |
| `Ctrl + d` | Half Page Down | Smooth scrolling down |
| `Ctrl + u` | Half Page Up | Smooth scrolling up |

---

## ✏️ 2. Core Editing Combos

These change commands automatically delete target text and drop you in **Insert mode**, saving valuable keystrokes.

| Command | Targets | Real-world React/JS Example |
| :--- | :--- | :--- |
| `ciw` | **Change Inner Word** | Edit a variable name at the cursor: `const my[Var] = 10` |
| `ci"` | **Change inside Quotes** | Edit prop value or string: `className="[flex items-center]"` |
| `ci(` | **Change inside Parentheses**| Edit function params or hooks: `useEffect(() => {}, [[count]])` |
| `ci[` | **Change inside Brackets** | Edit array elements: `const list = [[1, 2, 3]]` |
| `ci{` | **Change inside Braces** | Edit object body: `const config = {[theme: "dark"]}` |
| `cit` | **Change inside JSX Tag** | Edit element text: `<div>[Hello World]</div>` |
| `cc` | **Change Whole Line** | Rewrite current line from scratch |
| `C` | **Change to End of Line** | Rewrite from cursor position to line end |

---

## ✂️ 3. Deleting & Copying (Yanking)

| Command | Action | Description |
| :--- | :--- | :--- |
| `dd` | Delete Line | Cut the current line to clipboard |
| `yy` | Yank (Copy) Line | Copy current line to clipboard |
| `p` | Paste After | Paste clipboard content after cursor / below line |
| `P` | Paste Before | Paste clipboard content before cursor / above line |
| `diw` | Delete Inner Word | Delete word under cursor without entering Insert mode |
| `di"` | Delete inside Quotes | Clear string contents |
| `D` | Delete to End of Line | Cut cursor position to line end |
| `ddp` | Move Line Down | Cut line and paste below (swaps line with down-neighbor) |
| `ddkP` | Move Line Up | Cut line and paste above (swaps line with up-neighbor) |
| `yyp` | Duplicate Line | Copy and paste the current line directly below |

---

## 🔎 4. Search, Select, & Repeat (Senior Workflow)

The secret to massive speed is chaining navigation with the dot operator (`.`) to apply edits repeatedly.

| Command / Flow | Action | Description / How to use |
| :--- | :--- | :--- |
| `/searchTerm` | Search Forward | Find instances of `searchTerm` in the file. Press `Enter` to confirm. |
| `n` | Next Match | Jump to the next search occurrence |
| `N` | Previous Match | Jump to the previous search occurrence |
| `.` | **Repeat Last Edit** | Repeats your last change (e.g. if you did `ciw` or `dd`) |
| `u` | Undo | Undo last change |
| `Ctrl + r` | Redo | Redo last undone change |
| `v` | Visual Selection | Select character-by-character |
| `V` | Visual Line Selection| Select line-by-line (perfect for block operations) |
| `Ctrl + v` | Visual Block Selection| Select column block (ideal for editing Tailwind class lists) |

---

## ⚡ Multi-Command Combos

Use these powerful combinations for day-to-day speed coding:

* **Fuzzy Edit:** `/myVar` ➔ `ciw` (type new name) ➔ `Esc` ➔ `n` ➔ `.` (Repeatedly renames occurrences)
* **Clone & Edit:** `yyp` ➔ `ciw` (Clones a line/variable and immediately starts renaming it)
* **Clean Code:** `/console.log` ➔ `dd` ➔ `n` ➔ `.` (Rapidly purges console logs throughout the file)
