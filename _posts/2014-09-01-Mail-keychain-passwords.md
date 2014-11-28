---
layout: post
title: "Mail asks for an account password from time to time?"
description: "Something went wrong - Keychain Access"
category: articles
tags: [Mail, mba, os x, troubleshooting, keychain access]
author: jiri_zoth
---

I didn't even notice when it happened the first time. I just entered a password and ran the download again. Actually, I do not remember when I realized there is something wrong. But I know when I started to be VERY annoyed. It was the moment I had to enter passwords to all of my accounts for the second time in a week. Who was the troublemaker do you ask? The MAIL royalty itself. And it was the start of my love-hate relationship.

### Shortcut:

```
If you tried all other options to fix an issue with Mail asking repeatedly for an account password then you most likely end up with this:

1 open Keychain Access
2 search for 'Mail'
3 select items 'internet passwords' that are related to your Mail accounts
4 move all selected items to the 'local items' storage in Keychain
5 restart Mail (exit and open)
```

### The story
Mail does not work. It keeps asking for passwords. I am stuck.
There must be something to blame! So, I chose google. I tried many things and followed various attempts at guidance, but nothing helped. I ended up entering passwords only for accounts from which I urgently needed the messages. I tried solving the issue next time and the next time and the time after and many other times. The issue always reoccurred after some time.

Untill the moment that I acquired a critical mass of knowledge - the issue can be caused by:

* an error in communication between Mail.app and Keychain access[^1]
* an error introduced by OS X Maverics with its new iCloud keychain access option. Maverics did something nasty (even if the feature is not used)[^2].

Well, I read many more articles about the topic on the internet, though I chose only two articles for reference. Hereby I give credit also to other authors who did their research and published their findings.

So, I opened Keychain Access and I learned that all my 'internet password' items are placed within the 'login keychain'. See the picture below.  So, I was already aware that I should delete the items and let Apple Mail create new ones. BUT I have about 10 email accounts configured and they come with DIFFICULT passwords. And many of them are google accounts with two way security - it is a hell of a lot of work. I have done that before several times and I am p&lowast;&lowast;&lowast;&lowast;d. I do not want to type a single character anymore!
And then, a moment of inspiration came - I will move them from 'login' to 'local'. So, I did. I restarted the Mail. And? It WORKED like a charm :-)


![The pre-Maverics location of internet passwords](/assets/2014/keychain-login-items.png)
*Note: In the picture above, there is no 'local items' anymore because I have switched to the iCloud feature since.*

In preparation for this article I ran a google search again to gather sources for my ref list and, knowing the solution already, I found a small blog post describing the issue, its root cause and a solution[^3]. I wish I had found that article at the beginning.

### Who's to blame?

Apple. Do they even test OS X upgrades with Apple apps? It's hard to conclude anything other than - nope (take it with a grain of salt).

------

[^1]: CNet article about Mail troubleshooting specifically pointing out fiddling with Keychain Access entries [here](http://www.cnet.com/news/e-mail-servers-rejecting-passwords-in-os-x-mail/).
[^2]: Apple Support Communities article about Mail account password issues after installation of Mavericks [here](https://discussions.apple.com/thread/5486175).
[^3]: The very brief and precise article describing fix [here](http://blog.centurio.net/2013/10/25/mac-os-x-mavericks-new-keychain-defaults/).
