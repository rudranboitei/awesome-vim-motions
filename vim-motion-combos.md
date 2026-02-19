# ✅ Vim Motion Combos — Developer Daily Use Only

## 🚀 Move Line (Keep — very useful)

```
ddp → move line down
ddkP → move line up
yyp → duplicate line
dd → delete line
yy → copy line
```

That's enough for line management.

## 🚶 Navigation (Only essentials)

```
gg → top of file
G → bottom of file
0 → start of line
$ → end of line
w → next word
b → previous word
Ctrl+d → half page down
Ctrl+u → half page up
```

You don't need H M L { } etc now.

## ✏️ Editing Combos (MOST IMPORTANT)

These are gold.

```
ciw → rename variable
ci" → edit prop / string
ci( → edit function / hook
ci[ → edit array
ci{ → edit object
cit → edit JSX text
```

Delete versions:

```
diw → delete word
di" → delete string
```

That's 80% real editing.

## 🧹 Line Editing (Daily)

```
cc → rewrite line
C → rewrite till end
D → delete till end
o → new line below
O → new line above
A → insert end
I → insert start
```

Used constantly.

## 🔎 Search + Fix (Senior workflow)

```
/text → search
n → next
. → repeat last change
u → undo
Ctrl+r → redo
```

Extremely important.

## 🔢 Counts (Very practical)

```
3dd → delete 3 lines
5j → move 5 lines
4w → move 4 words
```

Counts = speed.

## 📋 Visual Mode (Basic only)

```
v → select text
V → select line
Ctrl+v → block select
```

Good for Tailwind editing.

---

# 🔥 15 Vim Combos React Devs Actually Spam

These are **real combos React devs spam daily** — not fancy, just practical.

## 1️⃣ Move line down

👉 `ddp`

Fix order of JSX / imports fast.

---

## 2️⃣ Move line up

👉 `ddkP`

Very common while refactoring.

---

## 3️⃣ Duplicate line

👉 `yyp`

Copy component, hook, Tailwind line.

---

## 4️⃣ Rename variable

👉 `ciw`

Cursor on variable → rename instantly.

Used everywhere.

---

## 5️⃣ Edit prop value ⭐

👉 `ci"`

Example:

```
<Button size="lg" />
```

Change value in seconds.

---

## 6️⃣ Edit JSX children ⭐

👉 `cit`

```
<div>Hello</div>
```

Change text fast.

React dev spam this.

---

## 7️⃣ Edit hook / function ⭐

👉 `ci(`

```
useEffect(() => {}, [])
```

Edit callback quickly.

---

## 8️⃣ Edit dependency array

👉 `ci[`

Used daily with hooks.

---

## 9️⃣ Edit object

👉 `ci{`

State object, props object, API response.

Very common.

---

## 🔟 Rewrite whole line

👉 `cc`

Faster than deleting + typing.

---

## 1️⃣1️⃣ Change till end

👉 `C`

Example:

```
return slow + 1
```

Rewrite end fast.

---

## 1️⃣2️⃣ Search + fix workflow ⭐⭐⭐

👉 `/text`
👉 `n`
👉 `.`

Rename / clean logs everywhere.

Senior workflow.

---

## 1️⃣3️⃣ Open new line fast

👉 `o` → below
👉 `O` → above

Used constantly while coding.

---

## 1️⃣4️⃣ Duplicate then edit combo ⭐

👉 `yyp` → `ciw`

Clone variable / JSX → modify.

Super common pattern.

---

## 1️⃣5️⃣ Move fast in file

👉 `gg` → top
👉 `G` → bottom
👉 `Ctrl+d` → scroll

Huge project navigation.

---

# 🧠 The Real React Vim Pattern

While coding you repeat this:

Navigate → `w b gg`
Edit → `ciw ci" cit`
Refactor → `.` repeat
Reorder → `ddp`
Hooks → `ci(`
Search → `/text`

That's it.

---

# ⭐ If You Master These — You Look Fast

Seriously these 15 = 80% Vim productivity.

You don't need advanced macros yet.

---

If you want next level, I can show:

🔥 10 Vim combos Tailwind devs spam
🔥 Vim combos for DSA problems
🔥 Vim mistakes that slow React devs
🔥 Real senior coding workflow
🔥 Vim mental model (most important)

Just tell me 😄
