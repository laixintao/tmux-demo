# Tmux (Terminal Multiplexer)

Source: https://github.com/tmux/tmux
Mnaual: `man tmux`
---

# Tmux VS GNU Screen

+++
## tmux

### Pros
- Can send keys to other panes, kind of like an IDE
- Easy keybindings -- with the right config, you'll feel at home from Vim or Screen
- Vim-ish and Emacs-ish bindings built-in
- Good layout management, a lot like a tiling window manager
- Unicode seems to Just Work with modern terminals
- Some terminal issues fixed with TERM=tmux

+++
### Cons
- Slow -- unsure why, but keystrokes seem laggy No more issues with slowness
- Multiplexing forces the whole session width and height to the smallest attached terminal
- Has crashed multiple times on Mac OS X, losing the entire session
- Has failed on Linux after upgrade, where I couldn't reconnect to my old session
- Misses command keystrokes occasionally - ^A ^[ takes a few tries for copy mode
- Can't move a pane from one window to another Fixed with the join-pane command
- No line unwrapping (or "reflow" or "rewrap") after terminal width change (window resizing)

+++

## GNU Screen

### Pros
- Extremely stable (v1.0 was in 1987)
- Some terminal issues fixed with TERM=screen
- Emacs-ish bindings built in
- Easy to move and control horizontal panes
- When multiplexing, any attached terminal can resize a pane

+++

### Cons
- No vertical splits without patch (except on Ubuntu)
- Pane splits are lost when detaching
- Getting Unicode to work takes a little finesse and determination
- Crazy status line configuration
