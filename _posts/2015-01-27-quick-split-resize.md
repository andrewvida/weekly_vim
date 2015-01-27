---
layout: post
title: Quick Split Resize
category: posts
---

This quick tip comes from my fellow Double Agent, Ryan Castillo (@rmcastil).  Thanks Ryan!

When working in Vim, I typically have two vertical splits going.  One for tests and the other for the code under test.  If I decide to disconnect from my cinema display, then the splits need to be resized to work on my MacBook screen.

My typical workflow was to use `:vertical resize` and keep incrementing until the splits look about the same size.

One afternoon, Ryan and I were pairing and as he was watching my play around with my splits, he suggested this: {% highlight vim %} ctrl-w = {% endhighlight%}

Splits within the window are now equally sized!
