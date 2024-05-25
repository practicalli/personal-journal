---
title: Weekly journal & Neovide
date: 2023-12-09
categories:
  - practicalli
---

**Thoughts for today**

The Practicalli journal will move to a weekly cadence now I have a full time job with Griffin Bank.

I do write a daily journal for my activities in Griffin and will share information that is not sensitive or business valuable.

<!-- more -->

## Engineering Manager

![Engineering manager image - hackertrail](https://www.hackertrail.com/wp-content/uploads/2021/08/64yrpkiguae-1024x683.jpg){align=right loading=lazy style="height:150px"}

I've completed my first week as engineering manager and there has been a lot to learn (and still a huge amount more to learn).

I joined when we are reviewing working practices, which has given me an opportuntiy to contribute early on.  

As I am learning the business and development workflows, I am adding the occasional tweek to the already excellent docs, especially for onboarding engineers.  I have sneaked in a few links to the Practicalli content too :)


## MacOSX Development environment

![Kitty Logo](https://github.com/practicalli/graphic-design/blob/live/logos/kitty-light.png?raw=true#only-dark){align=right loading=lazy style="height:150px;width:150px"}
![Kitty Logo](https://github.com/practicalli/graphic-design/blob/live/logos/kitty-dark.png?raw=true#only-light){align=right loading=lazy style="height:150px;width:150px"}

As I am setting up a Macbook Pro as the development machine I will have a chance to add any small differences between Linux and MacOSX when it comes to Clojure development.

So far the Clojure development setup is almost identical to my Linux laptops, except for the use of Homebrew to install a few tools I would normally install via Debian packages

- Kitty, a fast terminal app with multiple session tabs
- Zsh and Prezto to optomise CLI commands, with fish-style completion enabled
- Neovim & AstroNvim for editing & coding, with Clojure LSP for live linting
- Emacs for all the things I havent learned to do in Neovim, e.g. Magit rebasing
- Java 21 (homebrew)
- Clojure
- Bazel build tool (this is new to me and looks very interesting)

May of the development tools at Griffin are installed via a single script, so its quite simple to get going.


## Neovide GUI for Neovim

![Neovide Logo](https://neovide.dev/assets/neovide-128x128.png){align=right loading=lazy style="height:150px"}

[:globe_with_meridians: Neovide](https://neovide.dev/){target=_blank} is a very nice and really fast GUI app on top of Neovim.

I'll be using Neovide for the rest of December to see if its preferable to Neovim in a terminal (kitty).

The initial reason to use Neovide seems mainly experiential, the cursor moves smoothly along and provides a pleasing visual effect when jumping around.  I am assuming this will help keep track of the cursor when navigating larger code bases and text documents.  There are other [:globe_with_meridians: cursor effects which can be configured](https://neovide.dev/configuration.html#cursor-settings){target=_blank} .


### Neovide install

Neovide install was via a Linux AppImage from the GitHub release page for the project.

The `guifont` option was set to define the font family and size specifically for Neovide

!!! EXAMPLE "Neovide guifont setting in AstroNvim"
    ```lua title=".config/astronvim-config/options.lua" hl_lines="12"
    return {
      opt = {
        -- set to true or false etc.
        relativenumber = true, -- sets vim.opt.relativenumber
        number = true, -- sets vim.opt.number
        spell = false, -- sets vim.opt.spell
        signcolumn = "auto", -- sets vim.opt.signcolumn to auto
        wrap = true, -- sets vim.opt.wrap
        -- showtabline = 0,    -- sets vim.opt.showtabline - zero hides tabs
        timeoutlen = 420,
        -- neovide font
        guifont = "Fira Code:h16",
      },
    ```

Neovide specific configuration can be added using a conditional block, checking the global value `vim.g.neovide`

!!! INFO "Neovide specific configuration"
    ```lua
    if vim.g.neovide then
        -- add configuration only for Neovide 
    end
    ```

### Run neovide

A shell alias called `neovide` that sets AstroNvim as the configuration and runs `neovide`

!!! EXAMPLE "Neovide shell alias"
    ```shell title=".config/shell-aliases"
    # Neovide alias with AstroNvim configuration
    alias neovide="NVIM_APPNAME=astronvim neovide"
    ```

### Remote server code
    
Neovide seems useful when working with code on a remote server, especially if the server has limited graphical support. 
    
Neovim can be run in headless server mode using Unix sockets or TCP (ideally over an SSH connection for added security).

Neovide can [:globe_with_meridians: connect to Neovim](https://neovide.dev/features.html#connecting-to-an-existing-neovim-instance){target=_blank} and display richer information, e.g. syntax warnings, ligatures, etc.

??? EXAMPLE "Headless command for Neovim"
    ```shell title=".local/bin/nvim-headless"
    #!/usr/bin/env zsh

    # Start Neovim as a headless service for connection by GUI tools, e.g. Neovide

    # Set AstroNvim Configuration for Neovim
    export NVIM_APPNAME=astronvim 

    # Start Neovim listening over Unix socket
    $HOME/.local/bin/nvim --headless --listen /tmp/.nvim-instance.sock

    # Start Neovim listening over TCP - Less secure
    # nohup nvim --listen 127.0.0.1:6666 --headless </dev/null >/dev/null 2>&1 &
    ```

??? EXAMPLE "Neovide command to connect to Neovim"
    ```shell title=".local/bin/neovide-connect"
    #!/usr/bin/env zsh

    # Connect Neovide to Neovim server

    # Connect over Unix sockets
    $HOME/.local/bin/neovide --server=/tmp/.nvim-instance.sock

    # Connect over TCP (less secure)
    # $HOME/.local/bin/neovide  --server=localhost:6666
    ```


## Park Run

![Park Run Logo](https://wilmslowrunningclub.co.uk/wp-content/uploads/2016/04/parkrun-logo.jpg){align=right loading=lazy style="height:150px"}

A very wet 5km park run today (although more preferable to a 4 hour cycle ride in the wet).

I am still quite unfit when it comes to running and so continue to have a mixture of speed walking, jogging and running.  I have been getting a fairly decent time with this combination.

Today I did 5km in 35 minutes and 5 seconds, which is 20 seconds faster than last week (which had less wind and rain).

I came 37th in my age group with an age-graded score of 42.42% (double the meaning of life).  The age-graded score is a measure against world record running times for a specific age range, so it seems I wont be breaking any world records for a while :)

---
Thank you.

[:globe_with_meridians: Practical.li Website](https://practical.li){target=_blank .md-button} 

[:fontawesome-brands-github: Practical.li GitHub Org](https://github.com/practicalli){target=_blank .md-button} 
[:fontawesome-brands-github: practicalli-johnny profile](https://github.com/practicalli-johnny){target=_blank .md-button}

[:fontawesome-brands-mastodon: @practicalli@clj.social](https://clj.social/@practicalli){target=_blank .md-button}
[:fontawesome-brands-twitter: @practical_li](https://twitter.com/practcial_li){target=_blank .md-button}
