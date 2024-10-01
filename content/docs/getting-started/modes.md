---
title: Learn about the different k9s modes
linkTitle: Modes
weight: 30
description: >
    k9s has different modes and here's the info
---

Like `vim` k9s is text-based and commands are typed in. A command can be a sequenz of keys or a single key, for example `CTRL + :` means hit the `CTRL` key and `:` key. Just `/` means "Hit the `/` key", which may be multiple keys depending on your keyboard layout.

## Command mode

**Shortcuts:** 
- `CMD + :` (MacOS) 
- `CTRL + :` (Windows / Linux)

Opens a prompt where commands can be entered.

### Auto Suggestion

k9s command mode supports autosuggestions. Suggestions are based on supported Kubernetes resource in singular/plural as well as short names and command aliases as describe below. The command mode supports the following keys:

| Key                | Description                                |
|--------------------|--------------------------------------------|
| ⬆️ ⬇️               | Navigate up or down thru the suggestions   |
| Ctrl-w, Ctrl-u     | Clear out the command                      |
| Tab, Ctrl-f, ➡️     | Accept the suggestion                      |

## Search mode


**Shortcut:** 
- `/`

Opens a search prompt. Type text to live-filter the current view.