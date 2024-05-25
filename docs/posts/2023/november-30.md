---
title: Updating my identity
date: 2023-11-30
categories:
  - practicalli
---

**Thoughts for today**

Security is very important but can be a challenge to usability.

<!-- more -->

## Security verses usability

Using a password manager is really effective, so long as it actually saves the password generated.

Creating a new Google workplace account can be a real challenge if you dont know the password the password generator created for you, especially when the organisation requires 2-Factor authorisation and that has not been set up due to not knowing the password.


## Flexiana prototype review

Ela Nazari arranged a review of a potential new product for team leads, managers and CEOs to give a team and individual performance tool, using data from various sources.  There seems a lot of potential there, compared to poking around GitHub for stats.

Hopefully I gave them lots of useful feedback during the session.


## Consistent identity

For greater discoverability and to avoid confusion it is very useful to have a consistent identity through all your internet presence.

I noticed that I had some variation, so I've updated my GitHub and Slack profiles to use the same name, Practicalli Johnny.

An interesting consequence of changing the GitHub name is that all GitHub pages within repositories of the account are rebuilt.  I assume due to the name being part of the URL to access the site.

Changing the GitHub account name doesnt affect Organisations that account participates in as the name doesnt change.

GitHub sponsorship seems unaffected by changing the GitHub account name.

The `practicalli-john` repository used to define an extended GitHub profile had to be renamed to match the change in account name, to [practicalli-johnny/practicalli-johnny](https://github.com/practicalli-johnny/practicalli-johnny)

[Practicalli Johnny GitHub profile](https://github.com/practicalli-johnny){target=_blank .md-button} 


## Neovim

Set Neovim 0.9 as the minimum recommeded version in the Practicalli Neovim book and updated laptops, [tablet and smartphone](https://practical.li/neovim/termux/) to use Neovim 0.9.4


## Debian and Java

Sofware updates today listed security updates for Java OpenJDK packages and I notices I still had several versions of those packages installed (11 and 17).

Time to remove Java 11 and use Java 21 as the default (keeping 17 for a little longer as a fall-back version).

!!! NOTE "Removing Java 11"
    ```shell
    apt remove --purge openjdk-11-jdk:amd64 openjdk-11-jdk-headless:amd64 openjdk-11-jre:amd64
    ```

    > `openjdk-11-source` package was not installed on my system


!!! NOTE "Add Java 21"
    ```shell
    apt install openjdk-21-jdk
    ```

    > `openjdk-11-source` package was not installed on my system

!!! WARNING "OpenJDK 21 Debian package availablity"
    Debian trixie (testing) includes [:globe_with_meridians: openjdk-21-* packages](https://packages.ubuntu.com/search?keywords=openjdk){target=_blank}

    Ubuntu 23.04 (lunar) and 23.10 (manic) include [:globe_with_meridians: openjdk-21-* packages](https://packages.ubuntu.com/search?keywords=openjdk){target=_blank}


## Using Debian Testing

Installing a laptop with Debian from scratch and using trixie (testing) version, which includes Java 21 and many updated packages.

After the install, edit `/etc/apt/sources.list` and replace all the instances of `bookworm` with `trixie` 

Debian documentation recommends a full upgrade after making such a change

!!! NOTE "Debian Linux full upgrade"
    ```shell
    apt full-upgrade
    ```

[Debian Linux - chainging to testing or unstable](https://www.debian.org/doc/manuals/debian-faq/choosing.en.html#s3.1.11){target=_blank .md-button} 

Continuing with Debian Linux install on Thinkpad with AMD chipset, using trixie (current testing) as the distribution verion.

---
Thank you.

[:globe_with_meridians: Practical.li Website](https://practical.li){target=_blank .md-button} 

[:fontawesome-brands-github: Practical.li GitHub Org](https://github.com/practicalli){target=_blank .md-button} 
[:fontawesome-brands-github: practicalli-johnny profile](https://github.com/practicalli-johnny){target=_blank .md-button}

[:fontawesome-brands-mastodon: @practicalli@clj.social](https://clj.social/@practicalli){target=_blank .md-button}
[:fontawesome-brands-twitter: @practical_li](https://twitter.com/practcial_li){target=_blank .md-button}
