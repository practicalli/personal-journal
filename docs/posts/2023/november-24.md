---
title: "Neovim search replace & Debian DRM"
date: 2023-11-24
categories:
  - practicalli
  - debian
  - neovim
---

**Thought of the day**

What are the options for search and replace text in Neovim?

Sometimes error messages are missleading...

<!-- more -->


## Neovim Search and Replace

Known options

- `g m A` will match text under curor allowing in-place editing with visual-multi plugin 
- `:%substitue` vim-style search and replace (I find this fiddley and not reliable, although could be user errror)
- Clojure LSP for symbols, etc.


Use a visual select to search and replace, with confirmation

Note: `'<,'>` is automatically included when in visual mode and `:` is pressed to start a command 

```vim
:'<,'>s/search-text/replace-text/gc
```

Previous slack discussions
- [3 November 2022](https://clojurians.slack.com/archives/C0DF8R51A/p1667466346891749)


### :cdo neovim command

Telescope can generate a quickfix list, showing the results of pattern matches across the current project files.  Then use search and replace on the quickfix list to make changes across the project.

++spc++ ++"f"++ ++"w"++ search for a word across a project

++ctrl++ ++"q"++ opens the quickfix list

Use `:cdo` command to search and replace in the quickfix list

```vim
:cdo %s/current-pattern/new-pattern/g
```

Including the `c` option to confirm each replacement (using a noice popup when using Practicalli AstroNvim-config)

> Practicalli Neovim search-replace pages update with lessons learned today

## Debian Linux

Firefox ESR has DRM disabled by default, so streaming video sites like Amazon Prime and Netflix will show errors

!!! INFO "Enable DRM for streaming video sites"
    Open **Settings** > **General** 

    Scroll down to **Play DRM Content** option and ensure it is checked.


Amazon Prime shows an error describing how to enable the Widevine Content Decryption Module, however this plugin will not show in the `about:plugins` until the Settings > General > Play DRM Content option is checked.

---
Thank you.

[:fontawesome-brands-github: practicalli-johnny](https://github.com/practicalli-johnny){target=_blank .md-button}

