---
title: "Continuing the move to Debian Linux"
date: 2023-11-21
categories:
  - practicalli
---

**Though of the day**

Uncluttering my laptop collection is a facinating journey down a long history of laptops, many of which  I had forgotten about.  Most of the laptops still work and run new versions of Linux pretty well.

I really enjoyed using the EzePc laptops as they were so easy to carry around to all the community events I used to go to.  Although they would have benefited from a nice [Atreus keyboard from Keyboard.io](https://shop.keyboard.io/products/keyboardio-atreus).

Debian is very useful for older i686 to i386 cpu based hardware.  Firefox-esr is the only browser that seems to still support these older chipsets.

<!-- more -->

## New Journal

Use Material for MkDocs blog feature to create a rich experience for journal entries written in markdown.

[Practicalli Journal](https://practical.li/journal){target=_blank .md-button} 

The journal will match the appearance of other Practicalli content and therefore have a light and dark theme built in.

Older developer journal content will be added to the new journal to make it easier to find and consume this content, e.g. [practicalli-johnny/developer-journal](https://github.com/practicalli-johnny/developer-journal) and [practicalli-johnny/100-days-of-code](https://github.com/practicalli-johnny/100-days-of-clojure-code)

> Consider creating a 100 Days of Clojure guide to those new to learning Clojure


## Practicalli Org .github

Updated Practicalli GitHub org with default repository healthcheck files

- Creative Commons License
- Code Of Conduct
- Funding with GitHub Sponsors
- Pull request templates

All repositories within the Practicalli Org on GitHub will use these defaults unless they provide their own, e.g. within a `.github` directory.

Updated the [Practicalli Org profile](https://github.com/practicalli) defined in the `.github` repository, updating the Clojure REPL workflow images and practicalli logo.

[Using the .github repository - FreeCodeCamp](https://www.freecodecamp.org/news/how-to-use-the-dot-github-repository/){target=_blank .md-button} 


## GitHub stats

Reached 366 consecutive days of commits on the `practicalli-john` GitHub account.

Added a `.gitattributes` configuration to some repositories reporting a different or irrelevant repository language.  GitHub uses

[Linguist troubleshooting: Repo language incorrectly detected](https://github.com/github-linguist/linguist/blob/master/docs/troubleshooting.md#my-repository-is-detected-as-the-wrong-language){target=_blank .md-button} 

[GitHub Linguist Overrides](https://github.com/github-linguist/linguist/blob/master/docs/overrides.md){target=_blank .md-button} 

[GitHub Linguist languages supported](https://github.com/github-linguist/linguist/blob/master/lib/linguist/languages.yml){target=_blank .md-button} 


## Debian

Spending the rest of 2023 moving over to Debian to compare the experience to Ubuntu.

One main driver for the switch is the every growing use of Snaps for major parts of Ubuntu, rather than the more efficient debian packages.

Snaps can make it easier for maintainers of applications and libraries.  

However, there is always at least 2 versions of a snap installed and as a snap is self-contained its install is typically larger.  Snaps such as firefox have also had a noticable impact on performance, especially when starting the application.  I am also concerned that a snap would be using more RAM memory as it is loading its own version of all its libraries into memory.

Debian has stayed with the highly reliable and efficient `deb` package format for everything.

Debian is 99% of all the things I like about Ubuntu already.


## Copy files using sftp

Requires `openssh-server` on the system that will be connected to.

Requires `ssh` package on the system that will connect to the Openssh-server (not installed on Debian by default).

!!! EXAMPLE "Connect to a user account on a remote system"
    ```shell
    sftp://192.168.0.200/home/remote-username
    ```

## Separate admin account

Debian creates a proper `root` account with password during the initial install, e.g. from the net.iso.  The root account is expected to be used to install packages and other administrative tasks, so the user account created is not added to a sudo list to carry out administration.

Ubuntu adds the user account created during initial install to the sudo list, which is a little more convenient but also increases the risk of security breaches if the sudo package is ever compromised.  If a user password is discovered or account otherwise compromised, then any administration task can be carried out.

The debian approach does require remembering two passwords, one for the daily user account and one for root administration account.  However, the root password could be added to a secure password manager, e.g. NordPass or 1Password.

---
Thank you.

[:globe_with_meridians: Practical.li Website](https://practical.li){target=_blank .md-button} 

[:fontawesome-brands-github: Practical.li GitHub Org](https://github.com/practicalli){target=_blank .md-button} 
[:fontawesome-brands-github: practicalli-johnny profile](https://github.com/practicalli-johnny){target=_blank .md-button}

[:fontawesome-brands-mastodon: @practicalli@clj.social](https://clj.social/@practicalli){target=_blank .md-button}
[:fontawesome-brands-twitter: @practical_li](https://twitter.com/practcial_li){target=_blank .md-button}
