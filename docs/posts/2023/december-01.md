---
title: Monthly library updates
date: 2023-12-01
authors:
  - practicalli
categories:
  - practicalli
---

The last monthly review of library dependency versions in Clojure CLI Config aliases for 2023

<!-- more -->

## Practicalli Clojure CLI Config

Many GitHub repositories maintained by Practicalli include a [:fontawesome-solid-book-open: Scheduled Version Check CI workflow](https://practical.li/engineering-playbook/continuous-integration/github/workflows/practicalli/#scheduled-version-check){target=_blank}, which reports newer versions of project library dependencies and GitHub actions. The CI workflow uses [:globe_with_meridians: antq](https://github.com/liquidz/antq){target=_blank} to check versions.

Antq is used locally via the `:search/outdated` alias name in Clojure CLI Config to update the libraries which are configured as dependencies in each alias.

`oudated` is a task defined in the project `Makefile` that runs Clojure with the `:search/outdated` and writes the results to a file with the current date/time stamp.

!!! NOTE "Run outdated task for a report new versions of on library dependencies"
    ```shell
    make outdated
    ```

??? EXAMPLE "Makefile outdated task configuration"
    ```Makefile
    # Define file name for report with date/time stamp
    OUTDATED_FILE := outdated-$(shell date +%y-%m-%d-%T).org

    outdated: ## Check deps.edn & GitHub actions for new versions
	$(info --------- Search for outdated libraries ---------)
	- clojure -T:search/outdated > $(OUTDATED_FILE)
    ```

[Make - Practicalli Engineering Playbook](https://practical.li/engineering-playbook/build-tool/make/)


## On-boarding

A few magic codes and some help and I'm all signed up to Google Workspaces for the new role, so I have no excuse to avoid working on Monday :)

I am actually quite excited about the new role, especially now I have the Keyboard.io keyboard wired up to the Mac laptop so I can type at speed again.


## Debian Linux

Continuing with setup of Debian Linux on Lenovo Thinkpad with AMD chipset.  Using trixie enabled the touchpad, so all the hardware is working except for the WiFi adaptor.

Configured Zsh as the default shell with Power10k as the terminal prompt theme.  Specific configuration is published in the [:fontawesome-brands-github: practicalli/dotfiles repository](https://github.com/practicalli/dotfiles){target=_blank}


## Blog idea

A summary of the tooling projects created and regularly maintained by Practicalli

- Clojure CLI Config aliases to extend the functionality with community tools (deps-new, antq, kaocha, etc from more than 30 other aliases)
- Project Templates to generate new production grade Clojure projects that support the Practicalli REPL workflow
- AstroNvim user config for Neovim
- Spacemacs user config for Emacs


??? INFO "Commonly used tools provides via Clojure CLI Config aliases"
    - `:project/create` - production grade templates for new projects, supporting the Practicalli Clojure REPL Reloaded workflow
    - `:repl/reloaded` - start a REPL process with nREPL server for Clojure editor connection, with REPL Reloaded tools (or `:dev/reloaded` for editor jack-in)
    - `:search/outdated` - report newer versions for library dependencies and GitHub actions
    - `:search/libraries` - find a fully qualified library name and current version (`clojure -X:deps find-versions` shows last 8 versions)
    - `:deploy/clojars` deploys libraries to Clojars.org using required signed approach
    - `:test/run` and `:test/watch` to run Kaocha test runner once or in watch mode
    - `:test/coverage` for a Cloverage report on unit test coverage in the project
    - `:repl/socket` and `:repl/socket-client` to run a socket REPL server and tubular socket REPL client
    - `:service/http` runs a nasus http server for local static files
    - `:performance/benchmark` to add Criterium library for running speed tests on expressions
    - `:performance/memory-meter` to measure memory usage by the Clojure project


## Social visits

Catch up with the neighbour who looks after my cats when away and I look after theirs.  Making plans for cat sitting over the holidays.


---
Thank you.

[:globe_with_meridians: Practical.li Website](https://practical.li){target=_blank .md-button}

[:fontawesome-brands-github: Practical.li GitHub Org](https://github.com/practicalli){target=_blank .md-button}
[:fontawesome-brands-github: practicalli-johnny profile](https://github.com/practicalli-johnny){target=_blank .md-button}

[:fontawesome-brands-mastodon: @practicalli@clj.social](https://clj.social/@practicalli){target=_blank .md-button}
[:fontawesome-brands-twitter: @practical_li](https://twitter.com/practcial_li){target=_blank .md-button}
