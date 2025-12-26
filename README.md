
---

# TMUX MANUAL (YOUR CONFIG)

## PREFIX

**Prefix key:** `Ctrl + a`

Everything below assumes that.

---

## START / EXIT / DETACH

### Start tmux

```bash
tmux
```

### Detach (leave tmux running)

```text
Ctrl-a d
```

### Exit tmux completely

* Close current shell:

```text
exit
```

or

```text
Ctrl-d
```

* Kill entire session:

```bash
tmux kill-session
```

* Kill everything:

```bash
tmux kill-server
```

---

## CONFIG MANAGEMENT

### Reload tmux config

```text
Ctrl-a r
```

(No restart needed)

---

## WINDOWS (TABS)

### Create window

```text
Ctrl-a c
```

### Rename window

```text
Ctrl-a ,
```

### Kill window

```text
Ctrl-a &
```

### Switch windows (FAST)

```text
Alt + 1 → Window 1
Alt + 2 → Window 2
...
Alt + 9 → Window 9
```

> Windows are **1-based** (no 0).

---

## PANES (SPLITS)

### Split panes (keeps current directory)

```text
Ctrl-a |   → Horizontal split
Ctrl-a -   → Vertical split
```

### Kill pane

```text
Ctrl-a x
```

---

## PANE NAVIGATION (VIM BRAIN)

### With prefix

```text
Ctrl-a h → Left
Ctrl-a j → Down
Ctrl-a k → Up
Ctrl-a l → Right
```

### Without prefix (BEST PART)

```text
Alt + h → Left
Alt + j → Down
Alt + k → Up
Alt + l → Right
```

No thinking. Just move.

---

## COPY / PASTE (VIM MODE)

### Enter copy mode

```text
Ctrl-a [
```

### Inside copy mode

```text
v        → Start selection
Ctrl-v   → Block (rectangle) selection
y        → Yank (copy) & exit
```

### Notes

* Uses **Vim keys**
* Copies to **system clipboard**
* Mouse drag copy is **disabled** (on purpose)

---

## MOUSE (OPTIONAL BUT ENABLED)

You can:

* Scroll terminal history
* Resize panes
* Click panes/windows

Keyboard-first still wins.

---

## STATUS BAR (WHAT YOU’RE SEEING)

### Center

* Current window:

  * Window number
  * ✓ indicator
  * Last **2 folders** of current path

### Right side

* Window name
* Prefix state indicator (changes color when active)
* Session name

### Left side

* Empty (clean, minimal)

---

## VISUAL / THEME

* Theme: **Tokyonight Moon**
* Truecolor enabled
* Active pane border = **blue**
* Inactive pane border = **gray**
* Copy/command mode = **blue + bold**

---

## INDEXING RULES (IMPORTANT)

* Windows start at **1**
* Panes start at **1**
* When you close a window → others renumber automatically

---

## DAILY FLOW (RECOMMENDED)

```text
tmux
Ctrl-a c            → new window
Ctrl-a |            → split
Alt + hjkl          → move around
Ctrl-a [ + v + y    → copy
Ctrl-a d            → detach
```

---

## WHEN THINGS BREAK

* Reload config:

```text
Ctrl-a r
```

* Panic exit:

```bash
tmux kill-server
```

---
