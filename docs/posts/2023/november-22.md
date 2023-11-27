---
title: "Onboarding to a new role, hacking Clojure & Neovim"
date: 2023-11-22
categories:
  - practicalli
---

**Thought of the day**

Nervous excitement about starting a new role and hopeful I dont mess it up.

Enjoying writing a regular practicalli again, which is something I missed when not working.

<!-- more -->

## The Arqivist

I've been contributing to The Arqivist open source project, used to back up Slack channels.

Another person was interested in collaborating but had a few issues getting started.  The README was updated and an additional `:dev/env` alias added to `deps.edn` configuration if a contributor is not using the [Practicalli Clojure CLI Config](https://practical.li/clojure/clojure-cli/practicalli-config/)

[PR93 - dev: update hack locally details for starting a REPL ](https://github.com/jcpsantiago/thearqivist/pull/93){target=_blank .md-button}


## Mulog Custom transformations

Discussing the Arqivist project, a question arose about hiding sensitive data in logs during production whilst still seeing them during development, e.g anonymise sensitive data

Mulog has [custom transformations](https://cljdoc.org/d/com.brunobonacci/mulog/0.9.0/doc/custom-transformations) which can be used to pre-process each event before the publisher dispatches the event.

The mulog maintainer created the [where project](https://github.com/BrunoBonacci/where) to define Human readable conditions to filter data. 

!!! EXAMPLE "where is a DSL for powerful predicate functions"
    ```clojure
    (mulog/start-publisher!
      {:type :console
       :pretty? true
       :transform
       (partial filter (where :mulog/event-name :in? [:secret/db-connection :secret/api-key]))})
    ```
In a donut-party/system config, a production config would include the `:transform` and the dev config would not include the `:transform`


## Neovim 

How to navigate Clojure code using AstorNvim was asked in the Clojurians Slack channel. 

- `g d` jumps to definitions, including let bindings and function args
- `SPC l s` shows symbols in telescope popup
- `SPC l S` shows symbols in a new buffer
- `S-(` and `S-(` to traverse code

Neovim commands to investigate further

- `:help path` and the related topics (gf, :find, etc.)
- `:help include` and related commands ([i, :isearch)
- `:help define` and related commands (esp. :help include-search)
- `:help gd` and related commands
- `:help Explore` and related commands
- `:help usr_22` has a good introduction

[Clojurians Slack - navigating code in neovim discussion](https://clojurians.slack.com/archives/C0DF8R51A/p1700651248926689){target=_blank .md-button} 

!!! TODO "Neovim plugin: nvim-treesitter-sexp"
    Evalaute the [nvim-treesitter-sexp](https://github.com/PaterJason/nvim-treesitter-sexp) plugin with the Practialli AstorNvim User configuration and see if it is a valuable way to navigate Clojure expressions.

    ```lua title="plugins/clojure.lua"
    return {
      {
        "PaterJason/nvim-treesitter-sexp",
        ft = { "clojure", "fennel", "janet" },
        opts = {
          -- configuration:
          -- https://github.com/PaterJason/nvim-treesitter-sexp#configuration
          enabled = true,
          set_cursor = true,
          keymaps = {
            commands = {
              promote_elem = "<LocalLeader>kO",
              promote_form = "<LocalLeader>ko",
              splice = "<LocalLeader>k@",
            },
            motions = {},
            textobjects = {},
          },
        },
      },
    }
    ```

    If the plugin is successful, add it to the AstroNvim Community Clojure pack


## New role

I'm starting a new role (references allowing) as an Engineering Manager at a very nice Fintech company.

I've signed a contract and started completing the inital onboarding forms.  Hopefully the people I have put as references have positive things to say about me and the company is satisfied.

Part of the onboarding is to select a laptop to use.  As the company is in a regulated industry, they use MacBook Pro for their engineers.  I did get a choice of 14" or 16" display and which keyboard layout I preferred.

My previous experience with MacBook was mared by the elusive `#` character, so I opted for the [International English Keyboard layout](https://keyshorts.com/blogs/blog/37615873-how-to-identify-macbook-keyboard-localization#us-international)

[MacBook Keyboard layouts visualised](https://keyshorts.com/blogs/blog/37615873-how-to-identify-macbook-keyboard-localization){target=_blank .md-button} 

[MacBook Keyboard guide](https://keyshorts.com/blogs/blog/41999105-the-ultimate-guide-to-macbook-keyboard){target=_blank .md-button} 


