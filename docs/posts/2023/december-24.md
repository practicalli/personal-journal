---
title: Practicalli work over the winter break
date: 2023-12-24
authors:
  - practicalli
categories:
  - practicalli
---

The company I work for takes a break over the winter, so I have some time to spend on Practicalli content.


<!-- more -->


## Practicalli work

Work for Practicalli that is at the top of my very long TODO list :)

- DONE: Advising on and researching for Arqivist project
- DOING: [Git Signing article - Engineering Playbook](https://practical.li/engineering-playbook/source-control/git-configuration/)
- Add ssh key to RangerOne and GKar laptops
- Git config enhancements - practicalli/dotfiles
- Neovim, Conjure & Portal video
- More content on using Neovim - Practicalli Neovim
- API with Clojure, Reitit, Swagger, mulog and http-kit - Practicalli Clojure Web Services
- AWS accounts with IAM Identity Center - Practicalli Engineering Playbook
- Check for costs once AWS free tier ends
- [just](https://just.systems/man/en/) tool, an enhanced version of make (can pass arguments to tasks) - review and add to Practicalli Engineering Playbook
- article: practicalli in 2023 - summary of work and projects

## Configure Git & SSH signing

The main development laptop used had an RSA type SSH key.  ED25519 is now generally recommended, so a new key was generated with a long passphrase.

!!! NOTE ""
    ```shell
    ssh-keygen -t ed25519 -C "engineering@practical.li"
    ```

Example output of the command,

```shell title="ssh-keygen command output"
❯ ssh-keygen -t ed25519 -C "engineering@practical.li"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/practicalli/.ssh/id_ed25519):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /home/practicalli/.ssh/id_ed25519
Your public key has been saved in /home/practicalli/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256:***********************/******************* engineering@practical.li
The key's randomart image is:
+--[ED25519 256]--+
...
+----[SHA256]-----+
```

The passphrase of the SSH key was added to the Debian key ring using the `ssh-add` command, which prompts for the passphrase used when creating the key.

!!! NOTE ""
    ```shell
    ssh-add ~/.ssh/id_ed25519
    ```

Example output of the command

```shell
❯ ssh-add ~/.ssh/id_ed25519
Enter passphrase for id_ed25519:
Identity added: id_ed25519 (engineering@practical.li)
```

!!! INFO "SSH Config for MacOSX"
    Edit the SSH configuration, `~/.ssh/config`, and configure SSH to use the operating system keychain for the passphrase.

    ```shell
    Host github.com
      AddKeysToAgent yes
      UseKeychain yes
      IdentityFile ~/.ssh/id_ed25519
    ```

    This configuration does not seem neccessary (or correct) for Linux

Run git commands to configure Git to use SSH signing for commits and tags.  Or edit the Git client configuration, `~/.config/git/config`

!!! NOTE ""
    ```shell
    git config --global gpg.format ssh && \
    git config --global user.signingkey $HOME/.ssh/id_ed25519.pub && \
    git config --global commit.gpgsign true && \
    git config --global tag.gpgsign true && \
    git config gpg.ssh.allowedSignersFile "$HOME/.config/git/allowed-signatures"
    ```

Added the new SSH key to my GitHub account twice, onces as an authorisation key and second as a signing key.

The public key was copied by opening in neovim and yanking the line, ++"y"++ ++"y"++

Opened GitHub Settings > [SSH and GPG keys](https://github.com/settings/keys) page and selected New SSH key

Created an authorisation and signing key.

Now I can push signed commits to GitHub

!!! INFO "All Practicalli Commits signed"
    From now on, all commits to Practicalli repositories will be signed.

    I'm still considering if I should enforce other contributors to sign their work.  I think I will mandate all code contributions be signed.  Any contributions via the GitHub website should be signed.

    So it makes sense to ask all contributions that will be merged to also be signed.


## Audacity for audio fun

Audacity is an excellent tool for sound editing and effects, e.g. editing podcasts and creating sounds overlays for screencasts

Install audacity and supporting libraries using Debian packages

```shell
apt install audacity ffmpeg lame pavucontrol
```

When recording sound from the desktop, Pulse Audio should be set to the monitor for the default sound device, e.g. speakers and headphones.

Run Audacity and Click the microphone icon for Recording. Choose **Start silent monitor**

Start Pulse Audio Volume Control from desktop launcher. Select Recording tab. Select drop-down of available audio devices and choose the monitor for speakers and headphones.

Start recording in Audacity and play the desktop audio. Waveforms should be displayed in Audacity to indicate that sounds are being detected and recorded.

> Ensure a sufficient amount of hard drive space is available when recording the desktop sound as the recorded uncompressed by default.

Press the stop button. Use audacity tooks to edit the sound and export it to a file or save the whole sound sample as an audacity project.

Codecs such as Opus can be used to compress the sound file to a few percent of their original size without noticable quality loss.

> Create a shell script wrapper around these codec tools to use a consistent codec configuration, e.g. convert-to-opus

!!! EXAMPLE "Zsh script to convert Wav files to Opus"
```shell
#!/usr/bin/zsh

for x in *.wav ; do
  ffmpeg -i "$x" -b:a 96k -c:a libopus "${x:r}".opus
done
```

## Health

A reasonably warm [84km club ride](https://www.strava.com/activities/10428270444) for the time of year, completed in 3.5 hours on Saturday.

This was the first time I had tried the close riding with a group, swapping the front rider every few minutes.  I found it unnatural and constraining for most of the ride.  I enjoyed it when I was either at the front where I wouldnt need to slow down when decending.  Or I would drop back a little from the group so I didnt have to ride the breaks down hill, as my bicycle seems to freewheel faster than the other bikes in the group (it is supposed to be an Aero bike, so it seems like that aero works).

I was tired once I got home after the ride, although had enough engergy to make brown rice with beetroot powder and walnut pieces.  I didnt need to have a big sleep

A walk on Sunday for an hour helped streatch my legs.  Walking is a good way to recover from the ride.

I joined the local 5 km park run event on December 25h and manage a time of 34 minutes and 34 seconds, although [the run on Strava it was 33 minutes and 59 seconds](https://www.strava.com/activities/10433750076).


---
Thank you.

[:globe_with_meridians: Practical.li Website](https://practical.li){target=_blank .md-button}

[:fontawesome-brands-github: Practical.li GitHub Org](https://github.com/practicalli){target=_blank .md-button}
[:fontawesome-brands-github: practicalli-johnny profile](https://github.com/practicalli-johnny){target=_blank .md-button}

[:fontawesome-brands-mastodon: @practicalli@clj.social](https://clj.social/@practicalli){target=_blank .md-button}
[:fontawesome-brands-twitter: @practical_li](https://twitter.com/practcial_li){target=_blank .md-button}
