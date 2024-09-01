---
title: "Day 101: An extra day of code"
date: 2018-12-24
authors:
  - practicalli
categories:
  - 100daysofcode
tags:
  - clojure
  - games
---


**Thoughts for today**

Added more 4Clojure solutions

`def` supports a doc-string (I missed that ability previously).

Emacs Window management when running tests in Cider with Spacemacs.

The Logitech MX Ergo trackball mouse arrived today and it is so nice to use.  Its a trackball so the mouse itself stays static on the desk avoiding the need to move my hand around and therefore reducing RSI.  Using a trackball also means very little space is use.  The trackball is tilted so the hand is in a natural and more comfortable position, the same position I configured with my tented Model01 keyboard.

<!-- more -->

## Clojure core

I finally noticed `def` supports a doc-string as with `defn`.

> `ns` also supports a doc-string to define the overall purpose of the namespace

Adding a string after the name in the `def` expression will be used as the docstring, assuming there is another value after the string (otherwise the name is bound to the string).


## Cider tests in Spacemacs

`, t a` key binding in Spacemacs was used to run all tests for a Clojure project.

The test report buffer is shown, replacing an existing buffer if the test buffer is not already showing.  This is normal behaviour as I understand it.  The test buffer should be the active window (has the cursor) so pressing q will quit the test report and show you the buffer that was in the window previously.  If test report buffer is kept open in a window, then any new test report should always appear there.

The [Spacemacs Window Purpose layer](https://github.com/bmag/spacemacs-config/tree/master/layers/window-purpose) could be used to modify the behaviour of the test report buffer placement and window positions for other kinds of buffer (not something I have tried yet)

---
Thank you.

[:globe_with_meridians: Practical.li Website](https://practical.li){target=_blank .md-button}

[:fontawesome-brands-github: Practical.li GitHub Org](https://github.com/practicalli){target=_blank .md-button}
[:fontawesome-brands-github: practicalli-johnny profile](https://github.com/practicalli-johnny){target=_blank .md-button}

[:fontawesome-brands-mastodon: @practicalli@clj.social](https://clj.social/@practicalli){target=_blank .md-button}
[:fontawesome-brands-twitter: @practical_li](https://twitter.com/practcial_li){target=_blank .md-button}
