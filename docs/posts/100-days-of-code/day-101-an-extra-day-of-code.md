---
title: "Day 101: An extra day of code"
date: 2018-12-24
categories:
  - 100daysofcode
---


**Thoughts for today**

Added more 4Clojure solutions

Got a Logitech MX Ergo trackball mouse today and it is so nice to use.  It is a trackball, so the mouse itself stays static on the desk meaning I dont need to move my hand around and reducing RSI.  It also means I dont need a lot of space to use the mouse either.  The trackball is tilted so my hand is in more comfortable position, the same position I maintain with my tented Model01 keyboard.

<!-- more -->

## Clojure core

I finally noticed `def` supports a doc-string as with `defn`.  

> `ns` also supports a doc-string to define the overall purpose of the namespace

Adding a string after the name in the `def` expression will be used as the docstring, assuming there is another value after the string (otherwise the name is bound to the string).


## Cider tests in Spacemacs

`, t a` key binding in Spacemacs was used to run all tests for a Clojure project.

The test report buffer is shown, replacing an an existing buffer if the test buffer is not already showing.  This is normal behaviour as I understand it.  The test buffer should be the active window (has the cursor) so pressing q will quit the test report and show you the buffer that was in the window previously.  If test report buffer is kept open in a window, then any new test report should always appear there.

The [Spacemacs Window Purpose layer](https://github.com/bmag/spacemacs-config/tree/master/layers/window-purpose) could be used to modify the behaviour of the test report buffer placement and window positions for other kinds of buffer (not something I have tried yet)

