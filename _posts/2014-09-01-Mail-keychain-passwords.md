---
layout: post
title: "The Mail from time to time asks for an account password?"
description: "Something went wrong - Keychain Access"
category: articles
tags: [Mail, mba, os x, troubleshooting, keychain access]
author: jiri_zoth
---

I didn't even noticed when it happened the first time. I just entered a password and run a download again. Actually, I do not remember when I realized there is something wrong. But I know when I started to be VERY annoyed. It was the moment I had to enter passwords to about almost all my accounts, the second time in a week. Who was the trouble maker do you ask? The MAIL royalty itself. And it was the start of my love-hate relationship.

### Shortcut:

```
If you tried all other options to fix an issue with the Mail asking repeatedly for an account(s) password(s). Then you most likely end up with this:

1 open Keychain Access
2 search for 'Mail'
3 select items 'internet passwords' that are related to your Mail accounts
4 move all selected items to 'local items' storage of a Keychain
5 restart Mail (exit and open)
```

### The story
The Mail does not work. It keeps asking for passwords. I am stuck.
There must be one to blame! So, I chose google. I tried many things and followed many guidances, but nothing helped. I ended up entering passwords only for accounts which messages I needed urgently right now. I tried solved next time and next time and many times. The issue always reoccured after some time.

Till the moment I acquired a critical mass of knowledge, that the issue can be caused by:

* an error in communication between Mail.app and Keychain access[^1]
* an error introduced by OS X Maverics with its new iCloud keychain access option. The Maverics did something nasty (even if the feature is not used)[^2].

Well, I read much more articles about the topic on the internet I chose only two articles for reference. Hereby I give credit also to other authors who did their research and published their findings.

So, I opened Keychain Access and I learned that all my 'internet password' items are placed within the 'login keychain'. See picture below.  So, I was already aware I should delete the items and let Apple Mail create new ones. BUT I have about 10 email accounts configured and they come with DIFFICULT passwords. And many of them are google accounts with two way security - it is a hell of a work. I have done that before several times and I am p&lowast;&lowast;&lowast;&lowast;d. I do not want to type a single character anymore!
And then, a moment of a spark come - I will move them from 'login' to 'local'. So, I did. I restarted the Mail. And? It WORKED like a charm :-)


![Pre Maverics location of internet passwords](/assets/2014/keychain-login-items.png)
*Note: In the picture above, there is no 'local items' anymore becase I have switched to iCloud feature on since.*

In preparation for this article I run a google search again to gather sources for my ref list and knowing the solution already, I have found a small blog post describing the issue, its root cause and a solution[^3]. I wish I had found the article at the beginning.

### Who to blame?

Apple. Do they even test OS X upgrades with Apple apps? Hardly to say anything else then - nope (take it with a grain of salt).

------

[^1]: CNet article about Mail trouble shooting specifically pointing out fiddling with Keychain Access entries [here](http://www.cnet.com/news/e-mail-servers-rejecting-passwords-in-os-x-mail/).
[^2]: Apple Support Communities article about Mail account password issues after installation of Maverics [here](https://discussions.apple.com/thread/5486175).
[^3]: The very brief and precise article describing fix [here](http://blog.centurio.net/2013/10/25/mac-os-x-mavericks-new-keychain-defaults/).
