---
title: "Practicalli Email"
date: 2023-11-23
categories:
  - practicalli
---

**Thought of the day**

Making a note of why things are set up are useful so you dont delete anything important!


<!-- more -->

## Practicalli Email address

The [Practical.li](https://practical.li) domain is managed via Gandi domain name service.

Recieving emails from @practical.li addresses is manged by Gandi Email forwarding, each @practical.li email is mapped to a GMail email account.

Gandi also provided a free mailbox and SMTP service, although from November 2023 this is only a commercial servce.

The Gandi mailbox was used to send emails from @practical.li addresses, although Gandi are only providing this as a paid service.  I had forgotten why I had a mailbox with them as all the mail is forwared to GMail.  Once I deleted the Gandi mailbox and send an email with a @practical.li email address I quickly remembered...

I would rather use the sponsorship money to support writing content for Practicalli rather than speding it on services.

Luckily I found many articles on using Gmail SMTP server for applications and this includes GMail when using a different domain.  This is also much simpler to maintain and understand what it is used for.


!!! NOTE "Create a Google account app password"
    Open **myaccount.google.com** > **Security** > **2-Step Verification** > **App passwords**

    Save app password in password manager as it will not be shown again.

    Google account will confirm it was the correct user creating the app password, via an email and notification on the users android phone.

    [Sign in with app password - Google Account Help](https://support.google.com/accounts/answer/185833){target=_blank .md-button} 


The Google account App Password is used to send @practical.li emails via Google `smtp.gmail.com` server.

> The Google account name and password cannot be used as that approach also requires a 2-factor token

!!! NOTE "Add another email account in Gmail"  
    Open **Gmail** > **Settings** > **Accounts and Import**

    Enter Name and Email address for the new email

    Ensure **Treat as an alias** is ticked

    Click **Next Step>>**

    Configure the SMTP server with the Google Mail host

    **SMTP:** server smtp.gmail.com

    **Username:** Google account user name something@gmail.com

    **Password:** App password (not the gmail login password) 

    Assuming the credentials are correct, Gmail will send a confirmation email to verify the new email address

    To add your email address, click on the link in the confirmation email in Gmail Inbox.

    [Send Emails from different address or alias - Gmail help](https://support.google.com/mail/answer/22370){target=_blank .md-button} 

> If the email is not recieved, visit the **Gmail** > **Settings** > **Accounts and Import** and select **veryify** on the new email address


## Debian Migration

Backing up a Lenovo laptop to get ready to install Debian Linux.

Backup [Asus Eze PC 900](https://en.wikipedia.org/wiki/Asus_Eee_PC) and installed Debian Linux using i386 net iso image.
