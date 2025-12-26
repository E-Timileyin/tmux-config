--

# TMUX CHEAT SHEET

**Config: Neovim-First | Prefix = `Ctrl + a`**

---

## START / EXIT

```text
tmux            → start tmux
Ctrl-a d        → detach (leave running)
exit / Ctrl-d   → exit tmux
tmux kill-server→ kill everything
```

---

## WINDOWS (TABS)

```text
Ctrl-a c   → new window
Ctrl-a ,   → rename window
Ctrl-a &   → kill window

Alt + 1..9 → jump to window 1–9
```

> Windows start at **1**

---

## PANES (SPLITS)

```text
Ctrl-a |   → split horizontally
Ctrl-a -   → split vertically
Ctrl-a x   → kill pane
```

(splits keep current directory)

---

## PANE NAVIGATION

### Vim style (with prefix)

```text
Ctrl-a h   → left
Ctrl-a j   → down
Ctrl-a k   → up
Ctrl-a l   → right
```

### Fast mode (no prefix)

```text
Alt + h/j/k/l → move panes
```

---

## COPY / PASTE (VIM MODE)

```text
Ctrl-a [   → enter copy mode
v          → start selection
Ctrl-v     → block selection
y          → yank & exit
```

> Copies to **system clipboard**

---

## CONFIG

```text
Ctrl-a r   → reload tmux config
```

---

## MOUSE (ENABLED)

```text
Scroll     → scroll history
Click      → select pane/window
Drag       → resize pane
```

---

## STATUS BAR (WHAT YOU SEE)

* Window number + ✓
* Last **2 folders** of current path
* Right side:

  * Window name
  * Prefix indicator (color changes)
  * Session name

---

## INDEXING RULES

```text
Windows start at 1
Panes start at 1
Auto-renumber ON
```

---

## DAILY FLOW

```text
tmux
Ctrl-a c
Ctrl-a |
Alt + hjkl
Ctrl-a [ v y
Ctrl-a d
```

---

## PANIC / RECOVERY

```text
Ctrl-a r          → reload config
tmux kill-server  → hard reset
```

---

