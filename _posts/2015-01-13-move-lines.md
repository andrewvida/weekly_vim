---
layout: post
title: Move Lines Up/Down
category: posts
---

For the past couple years I've floated back and forth between Vim and other editors, such as Sublime Text 2 and GitHub's Atom editor.  One of the things that I really liked, that Sublime Text and Atom had was the ability to instantly move lines up and down.  

![Atom Move](/weekly_vim/images/posts/move_lines/atom_move_lines.gif)

My usual Vim worflow for this, is to do `ddp`, which deletes the line and stores it in the default register and pastes from the default register.

![Vim ddp](/weekly_vim/images/posts/move_lines/vim_ddp.gif)

A better solution is to use the [unimpared](https://github.com/tpope/vim-unimpaired) plugin by Tim Pope.  We can use the exchange `[e` and `]e` mappings to 'exchange' the current line with the one above it or below it.

Add these mappings to your `.vimrc`:

``` bash
" Sort single lines
nmap <C-Up> [e
nmap <C-Down> ]e

" Sort multiple lines
vmap <C-Up> [egv
vmap <C-Down> ]egv
```

This will enable moving of single and multiple lines using unimpared.

![Vim move](/weekly_vim/images/posts/move_lines/vim_move.gif)

Note: If you are on a Mac and when you press `control + up/down` and it opens Apple Mission Control, you'll have to change your OS X keymappings.

If you are using tmux, you will also have to set the tmux window option `xterm-keys` so that tmux will pass these keys through.

To do that, in your `.tmux.conf`, add:

``` bash
set-window-option -g xterm-keys on
```

and in your `.vimrc`, add:

``` bash
if &term =~ '^screen'
    " tmux will send xterm-style keys when its xterm-keys option is on
    execute "set <xUp>=\e[1;*A"
    execute "set <xDown>=\e[1;*B"
    execute "set <xRight>=\e[1;*C"
    execute "set <xLeft>=\e[1;*D"
endif
```
