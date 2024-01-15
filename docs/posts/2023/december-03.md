---
title: How much root cause analysis to do?
date: 2023-12-03
categories:
  - practicalli
---

**Thoughts for today**

Winter starts on Friday 22nd December, although its already much colder this year.

Early to bed tonight as I start commercial work on Monday morning.


<!-- more -->

## MkDocs

I havent been running the MkDocs server locally for the journal as the content is pretty straight forward.  However, I was reminded this morning that its useful to catch little issues like a missing title for the post.

If there are important things missing from the frontmatter of the post then MkDocs will fail to build.

!!! WARNING "MkDocs error - title missing in post"
    The `post_slugify` function in MkDocs takes a `post.title` and will generate an error if the title is empty. 
    ```python
    in _slugify_post
        return self.config.post_slugify(post.title, separator)
      File "/usr/lib/python3/dist-packages/markdown/extensions/toc.py", line 30, in slugify
        value = unicodedata.normalize('NFKD', value)
    TypeError: normalize() argument 2 must be str, not None
    ```

### Make and Kitty tweaks

I have a Makefile task called `docs` that will run the MkDocs server locally and serve up the built web site.  This runs very quickly, so there is little excuse not to run it.

For convienience of opening the MkDocs site in the browser the MkDocs server runs on the same port for all of the practicalli books and journal website, (localhost:7777).  

It is important to ensuring only one instance of the MkDocs servier is running.

Kitty terminal app has been configured to open a new terminal window in the same file path as the current tab.  This provides a quick way to start the MkDocs server for a particular project, opening up a new tab alongside and running `make docs` (after ensuring other MkDocs severs have been stopped)

!!! EXAMPLE "Kitty - Open new tab in current file path"
    ```shell
    # ---------------------------------------------------------
    # Key bindings

    # Open new tab in current window
    map ctrl+shift+t launch --cwd=current --type=tab

    # ---------------------------------------------------------
    ```
    [:fontawesome-brands-github: Practicalli Dotfiles - Kitty configuration](https://github.com/practicalli/dotfiles/tree/main/kitty)


## Neovim 

Lazy package manager continues to impress in terms of user experience.

`SPC p a` in AstroNvim was used to update plugins with Lazy and format tools with Mason.

There was an issue with LuaSnip update as Git detected local changes that were different to the commit history of LuaSnip it was cloning.  Lazy package manager displayed a message on how to resolve it, by using `x` to remove the LuaSnip plugin and `I` to reinstall. 

This kind of Git issue rarely occurs, so having an inline help message if very helpful.

Its assumed the root cause is some change to the LuaSnip commit history after the plugin was previously installed locally.  Or something locally was added by Neovim.  As the fix is very simple and fast to implement, there isnt much value in digging deeper unless this kind of issue occurs much more often.

---
Thank you.

[:fontawesome-brands-github: practicalli-johnny](https://github.com/practicalli-johnny){target=_blank .md-button}

