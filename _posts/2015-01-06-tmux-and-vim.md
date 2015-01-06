---
layout: post
title: Remote Pairing with tmux
category: posts
---

First, I'd like to wish everyone a Happy New Year!  One of my goals this year is to post something new here weekly.  I've been back and forth with different editors over the past couple years, but always seem to keep coming back to Vim.  So, this year, I want to challenge myself to learn something new -- keep improving so I can become much more proficient with Vim.

To kick things off this new year, I want to share how I've recently re-configured my machine and set up tmux for remote pairing.

Over the past several years, I've had the pleasure to pair with a friend of mine, Michael Joseph Kramer, who I feel is a pretty advanced Vim user. He has taught me many keybindings and shortcuts that I still use to this day.  In fact, I use most of his Vim configs, with several small tweaks.

If you're not already doing so, I suggest keeping your configuration files up on Github.  It's especially nice once you get a new computer to instantly go back to all of the things you know quickly.

You can find my settings [here](http://github.com/andrewvida/Config).  Be sure to take a look at the Rakefile as to how files get symlinked, plugins get installed and several other cool tricks!

Also be sure to take a look at the '.vim' directory.  There you will see how what plugins I run, as well as special keybindings and other goodness.  I feel that this is broken down very well.

If you're looking for other Vim config examples, I suggest that you take a look at the [Neo vim-config](https://github.com/neo/vim-config) and [Chris Hunt's dot-files](https://github.com/chrishunt/dot-files).

Next up is tmux.  If you've never worked with tmux before, you're in for a treat!  tmux is a terminal multiplexer.  It enables a number of terminals to be created, accessed, and controlled from a single screen.  A killer feature of tmux is that you can detach from a screen and it continues to run in the background until you come back to it.  I'll touch on this a bit later.  tmux is also excellent for remote pairing.

Here's how I set up my machine for remote pairing:

* [tmuxinator](https://github.com/tmuxinator/tmuxinator) - Allows easy creation and management of tmux sessions.
* [github-auth](https://github.com/chrishunt/github-auth) - Easily pair with anyone with a GitHub account by adding their public ssh keys to your authorized_keys file.

In my Config project, you'll see the '.tmux.conf' file with special bindings.

If you're new to tmux in general, be sure to pick up [tmux Productive Mouse-Free Development](https://pragprog.com/book/bhtmux/tmux) by Brian P. Hogan.

Enjoy learning about all of the things you can do with vim and tmux!  You're going to have a great time!  If you still don't believe me, check this out: [https://www.youtube.com/watch?v=9jzWDr24UHQ](https://www.youtube.com/watch?v=9jzWDr24UHQ)
