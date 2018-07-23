---
layout: post
title: multiple terminal manager: tmux/screen/byobu
description: multi-window manager in Linux
category: blog
---

The first thing you should know is that Ctrl+b is the default prefix in tmux. It means that running any command requires typing in the prefix first. As you probably have guessed, this is to avoid conflicts with key combinations used in other programs run in the terminal.

Here is a list of a few basic tmux commands:

    Ctrl+b " — split pane horizontally.
    Ctrl+b % — split pane vertically.
    Ctrl+b arrow key — switch pane.
    Hold Ctrl+b, don’t release it and hold one of the arrow keys — resize pane.
    Ctrl+b c — (c)reate a new window.
    Ctrl+b n — move to the (n)ext window.
    Ctrl+b p — move to the (p)revious window.

Other thing worth knowing is that scrolling is enabled by pressing Ctrl+b PgUp/PgDown. In fact, it enables the copy mode, which can also be done by pressing Ctrl+b [. When in copy mode, you can use PgUp/PgDown and arrow keys to scroll through the terminal contents. To (q)uit the copy mode, simply press the q key.

That should do the trick. At least, most of it.
Quitting tmux

To close a single pane in tmux, you need to either press Ctrl+d or type exit and press Return.

If you have multiple windows or panes opened and want to close them all at once, press the prefix (Ctrl+b), then type :kill-session and press Return.


screen:
screen the terminal multiplexer.

    To split vertically: ctrla then |.
    To split horizontally: ctrla then S (uppercase 's').
    To unsplit: ctrla then Q (uppercase 'q').
    To switch from one to the other: ctrla then tab

Note: After splitting, you need to go into the new region and start a new session via ctrla then c before you can use that area.

EDIT, basic screen usage:

    New terminal: ctrla then c.
    Next terminal: ctrla then space.
    Previous terminal: ctrla then backspace.
    N'th terminal ctrla then [n]. (works for n∈{0,1…9})
    Switch between terminals using list: ctrla then " (useful when more than 10 terminals)
    Send ctrla to the underlying terminal ctrla then a.

Share terminal:
Basic sharing with tmux

Again, there are only two steps. In the first terminal, start tmux where shared is the session name:

tmux new-session -s shared

Then in the second terminal attach to the shared session.

tmux attach-session -t shared 

Note:
https://lukaszwrobel.pl/blog/tmux-tutorial-split-terminal-windows-easily/

[Shannonh]:    https://github.com/xhan-shannon "xhan-shannon"
