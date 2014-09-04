---
layout: post
title: "Mail time to time asks for account password?"
description: "Something went wrong - Keychain Access"
category: articles
tags: [Mail, mba, os x, troubleshooting, keychain access]
author: "Jiri Zoth"
comments: true
twitter: true
twitteraka: jzoaka
---

I didn't even noticed when it happened first time. I just entered a password and run a download again. Actually I do not remember when I realized there is something wrong. But I know when I started to be VERY annoyed. It was the moment I had to enter passwords to about almost all my accounts maybe second time in a week. Who was the trouble maker do you ask? The MAIL royalty itself. And it was start of my love-hate relationship.

### Shortcut:

```
If you tried all other options to fix an issue with Mail asking repeatedly for an account(s) password(s). Then you most likely end up with this:

1 open Keychain Access
2 search for 'Mail'
3 select items 'internet passwords' that are related to your Mail accounts
4 move all selected items to 'local items' storage of a Keychain
5 restart Mail (exit and open)
```

### The story
Mail does not work. It keeps asking for passwords. I am stuck.
There must be one to blame! So, I chose google. I tried many things and followed many guidances nothing helped. I ended up entering passwords for accounts messages I needed. I tried solved next time and next time and many times. The issues always kept to reoccur after some time.

Till the moment I acquired critical mass of knowledge: issues can arise from between Mail.app and Keychain access[^1] and OS X Maverics with its newly introduced iCloud keychain access did something nasty (even if the feature is not used)[^2]. Well I read much more articles about the topics over the internet I chose the only two for illustration and to pay a credit to others who did their part.

So, I opened Keychain Access learned that all my 'internet password' items are placed within 'login keychain'. See picture below.  So, I was already aware I should delete the items and let Apple Mail create new ones. BUT I have about 10 email accounts configured and they come with DIFFICULT passwords. And many of them google accounts with two way security - it is hell of work. I have done before several times and I am p****d. I do not want type a single character!
And then it come moment of a spark - I will move them from 'login' to 'local'. So, I did. I restarted Mail. And? It WORKED like a charm :-)


![Pre Maverics location of internet passwords](/assets/2014/keychain-login-items.png)
*Note: In the picture above, there is no 'local items' anymore becase I have switched iCloud feature on since.*

In preparation for this article I run google search again to gather sources for my ref list and knowing already solution I have found a small blog post describing the issue its root cause and solution[^3]. I wish I had found the article at the time.

### Who to blame?

Apple. Do they even test OS X upgrades with Apple apps? Hardly say anything else then - nope (with a grain of salt).

------

[^1]: CNet article about Mail trouble shooting specifically pointing out fiddling with Keychain Access entries [here](http://www.cnet.com/news/e-mail-servers-rejecting-passwords-in-os-x-mail/).
[^2]: Apple Support Communities article about Mail account password issues after installation of Maverics [here](https://discussions.apple.com/thread/5486175).
[^3]: The very brief and precise article describing fix [here](http://blog.centurio.net/2013/10/25/mac-os-x-mavericks-new-keychain-defaults/).
