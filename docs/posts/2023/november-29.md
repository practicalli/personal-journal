---
title: Lightening my life
date: 2023-11-29
authors:
  - practicalli
categories:
  - practicalli
  - neovim
---

Feeling the space I've made after rearranging the office space and uncluttering more belongings

The cat has taken over my new BeYou chair, despite providing an even nicer space for her to sit.  My cats are a regular reminder that change cannot be forced.

<!-- more -->

## Rearranging office space

![ThingyClub dual mounting arms](https://www.thingyclub.com/cdn/shop/products/2_copy.jpg?v=1496227295){align=right loading=lazy style="height:240px"}

Even though I have multiple monitors and laptops in the boxy room that is my home office, rearranging a few items has really maximised the space. I have plenty of room for the laptop I will used for the new company I will work for.

[ThingyClub mounting arms](https://www.thingyclub.com/products/adjustable-laptop-monitor-dual-arm-desk-mount-bracket) are used for monitors and laptops to minimise desk space use, especially for the LG 34" ultra-wide monitor used as a second monitor.

[Keyboard.io](https://keyboard.io) is used as an external keyboard, using a USB switch to toggle attachement to work and personal laptop.  A Logitech bluetooth trackball is used for the few times I need a mouse, although only really for browsers and video editing.

The keyboard and trackball rest on a [Grandma Shark bamboo wood laptop desk](https://www.amazon.co.uk/gp/product/B087MCGY4M/) that sits on top of a corner shaped office desk to create a standing desk position.

The [BeYou chair kneeling position](https://practical.li/journal/health-and-new-chair/#beyou-chair) is ideal for the same the standing desk position the Grandma Shark desk provides.

> NOTE: when I was ill with Covid I used the Grandma Shark desk in bed to be able to do a little bit of work in-between sleeping and coughing.


## Recycling

The freecycle website is very convienient to find a new life for unwanted items.  It seems to be a more useful service during the warmer months, as more recently people are saying they are interested in items but then not turning up.

A have a small collection of items that hopefully I can give away before starting the new job next week.


## More parcel madness

Evri (formerly Hermes) delivery service continue to meet my very low expectations and completely failed to turn up today, saying they couldnt get access to the property.  No one knocked or rang the front door, so either they didnt turn up or went to the wrong location.

I am not planning on using WeBuyBooks again and will stick with MusicMagpie (who use DHL) and Zwifit (local collection lockers) for future book, DVD and video game sales.

## Neovim AstroNvim update

Update AstroNvim to 3.39.0 from within AstroNvim, using `SPC p A`.

`SPC p v` to show the AstroNvim version as a notification.

> Using the Practicalli Astronvim-config the notification level used for AstroNvim version is not shown and but can be seen in the notification history.

`SPC f n` to see the notification history and the output of AstroNvim version.

??? EXAMPLE "Updates from AstroNvim v3.39.0"
    ```vim
        ● alpha-nvim 14.8ms 󰢱 alpha  astronvim.autocmds
            29074ee DirChanged keymaps (21 hours ago)

        ○ astrocommunity
            e984f31 docs(rust): add guide on how to format with clippy (#649) (2 days ago)

        ○ friendly-snippets  LuaSnip
            53d3df2 add-xml-tag-go-snippet (#377) (3 days ago)
            9e99f7d Updated edge framework snippets (#378) (3 days ago)
            068b165 changed c++ cout to a more efficient and polyvalent snippet (#381) (3 days ago)
            83c54cd fix: django rest view snippets (#383) (3 days ago)

        ○ neogit  <leader>gs  <leader>gnt  <leader>gnc  <leader>gnd  <leader>gnk  User AstroGitFile
            bb538f1 Merge pull request #980 from gollth/merge-help-popups (6 hours ago)
            c87a51e Revert "CHANGE: Allow to open help popup from commit, log, reflog views" (7 hours ago)
            2d2a98f FIX: Add `fetch` popup keybind to reflow in visual mode (8 hours ago)
            f0864be CHANGE: Allow to open help popup from commit, log, reflog views (8 hours ago)
            d408aed CHANGE: Allow to open merge popup from commit, log, reflog views (8 hours ago)
            763948a Merge pull request #948 from NeogitOrg/flog-graph (20 hours ago)
            69ca013 Update readme (20 hours ago)
            273027a Only show "--color" switch when rendering ASCII graph (20 hours ago)
            ce47476 Flog -> Unicode (20 hours ago)
            e1a0a9d Allow configuring graph style (20 hours ago)
            961a9af Merge pull request #974 from gollth/fix-head-log-graph (21 hours ago)
            b3d7a01 FIX: Properly highlight remote only branches (29 hours ago)
            6d92f47 FIX: Properly render HEAD with `NeogitBranchHead` highlight group (29 hours ago)
            76a400a Merge pull request #976 from NeogitOrg/CKolkey-patch-1 (31 hours ago)
            b464b8a Update README.md (31 hours ago)
            7eccfc4 Formatting, gsub (9 days ago)
            d3dbebb Change the author color highlight (10 days ago)
            8a1f7cc Formatting (10 days ago)
            c9cad0a Replace commit.description in favor of subject/body (10 days ago)
            1b63c04 Use git lib entrypoint (11 days ago)
            7a3dea2 Use new field (11 days ago)
            f22f074 WIP flog graph (12 days ago)
            b7b9a83 Use builtin function to escape string (12 days ago)
            b23bb99 Escape escape characters (12 days ago)
            d56e1ca Need to wrap this so we can concatenate the result (12 days ago)
            975a0d4 Cleanup (12 days ago)
            158d8b0 Annotations (12 days ago)
            14bae65 Parse log output as JSON (12 days ago)

        ○ nvim-lspconfig  Neoconf  User AstroFile
            39546f7 fix(typos_lsp): use configuration file for root detection #2918 (29 hours ago)
            daaf00a docs: update server_configurations.md skip-checks: true (3 days ago)
            c6a62c7 chore(emmet_language_server): remove languages with emmet bundled by their language server (#2914) (3 days ago)
            e4a56ad perf: reduce an unnecessary function call #2913 (3 days ago)

        ● nvim-treesitter 11.95ms ✔ build
            8f16c39 feat(make): highlight phony prerequisites as functions (7 hours ago)
            fb101ed feat(make): give targets the function highlight (7 hours ago)
            10432e6 parsers: add tree-sitter-slang (9 hours ago)
            b04f990 Update parsers: css, facility, foam, wing (10 hours ago)
            bf982eb feat: add facility (24 hours ago)
            582a92e Update parsers: erlang, wing (33 hours ago)
            ba588ee fix(cpp): remove `@field` for identifiers with `_` prefix (#5731) (2 days ago)
            b8fbd13 Update README (2 days ago)
            8189d91 astro: add custom component highlighting (#5728) (2 days ago)
            482a2f1 Fix robot parser metadata in parsers.lua (2 days ago)
            b056e42 Update README (3 days ago)
            52b25c9 fixup: parser requires generate (ABI) (3 days ago)
            de51978 fixup: lint (3 days ago)
            274370e fixup: use any-of instead of vim-match (3 days ago)
            1e74c34 feat: add angular parser and queries (3 days ago)
            9d91101 twig queries: add combined injections (#5721) (3 days ago)
            eafc0c2 Update parsers: swift, wing (3 days ago)
            d8a7182 Update parsers: dtd, ssh_config, wing, xml (4 days ago)
            649d137 Update parsers: erlang, ssh_config, wing (5 days ago)
            71bdf97 feat(hocon): add fold query (#5710) (6 days ago)
            6d45b34 Update parsers: sql, wing (6 days ago)

        ○ nvim-web-devicons
            5efb8bd ci: use vim-colortemplate tarball rather than git clone (#347) (3 days ago)
            e034579 feat: add .luaurc and luau colours (#346) (3 days ago)
            7b1c4a8 feat: update fnl icons (#345) (3 days ago)
            3fe528b ci: pre-commit uses make (#344) (3 days ago)

        ○ rest.nvim  RestNvimPreview  RestNvimLast  RestNvim  <leader>rr  <leader>r  json  http
        ○ SchemaStore.nvim
            54a4ea1 Update SchemaStore catalog (4 days ago)
            c2c6bd2 Update SchemaStore catalog (5 days ago)

        ○ telescope.nvim  Telescope  nvim-neoclip.lua  telescope-file-browser.nvim
    ```

---
Thank you.

[:globe_with_meridians: Practical.li Website](https://practical.li){target=_blank .md-button}

[:fontawesome-brands-github: Practical.li GitHub Org](https://github.com/practicalli){target=_blank .md-button}
[:fontawesome-brands-github: practicalli-johnny profile](https://github.com/practicalli-johnny){target=_blank .md-button}

[:fontawesome-brands-mastodon: @practicalli@clj.social](https://clj.social/@practicalli){target=_blank .md-button}
[:fontawesome-brands-twitter: @practical_li](https://twitter.com/practcial_li){target=_blank .md-button}
