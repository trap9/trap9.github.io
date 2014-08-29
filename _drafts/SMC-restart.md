---
layout: post
title: "MBA slow wake or fan goes crazy?"
description: "First aid kit tool - SMC restart"
category: articles
tags: [mba, os x, troubleshooting, smc]
author: "Jiri Zoth"
comments: true
twitter: true
twitteraka: jzoaka
---

There was a pretty nasty thing about my MBA[^1]. Last two years I have started experiencing various issues that were progressively decreasing my satisfaction with the Apple product. And believe me I was not happy 'cause as any other Apple fan I want feel special :-)

Shortcut:

```
 press the (left side) Shift-Control-Option keys and the power button at the same time.
```
For full procedure to troubleshoot issues described here refer to Apple site[^2].

## The story
Over the time and many spent hours and hours ... and ... yeah ... hours. I nailed down following most repeatedly anoying issues:

1. fan noise - under unknwon conditions, fan speed and noise went up to VERY unacceptable levels and there was no way to get it back ... even when Activity Monitor showed essentially NO cpu load and temperature and ventilation where ok.
2. slow wake up - since install of OS X Lion wake up was progressively longer and longer. I did many tests what is a root cause. For example despite I have learned that leaving Safari open with multiple tabs, especially if there is a dynamic content in flash badly affects wake up time or I cleared out login items and utils hooked on start up/wake up. None of these let me to an ultimate fix.
3. battery started to be vicious - I was experiencing sudden charge drops and overall battery life was decreasing.

4. Mail started to ask for account passwords time to time. Actually it took me a several occasions till I realized that there is an issue and I started to be annoyed. You understand, I got apprx. 10 email accounts configured in my Mail app. So, every time it was 10x factor and frequency raised and raised.

The good news is I have found fix the issues above. In this post I will elaborate on fan noise, battery and slow wake up as the issues have same denominator.     I will publish in my next post fix to the Mail issue of 'forgotten passwords'.

### Fan noise
Struggling with raging fan in my mba over period of apprx. 2 years with volatile success I have nailed down that there is something called SMC and time to time it can get spoiled and then it impose negative effects on my mba such as outrageous fan. So, the cure is to RESTART SMC and bring mba back to line.

### Battery depreciation
One could expect battery depreciation over the time and necessity to replace battery in order to get back battery hours available. BUT is it assumable to start feeling discomfort about after one/one and half year? and rapid progress?
Finally I have checked my battery with CoconutBattery util - and learned that battery status is: service. The detailed log said that battery is not functional properly and replacement is needed. Well, I have bought a new battery and replaced the old one.

I connected the dots. Most likely because of my long term issues with mba EFI firmware, mitigated by SMC restart time to time, fan noise issues leaded to enormous energy consumption and it affected badly the battery lifetime.

### Slow wake up
I still remember my very first experience with Apple notebook. It was first model MBA with OS X Snow Leopard. The experience was amazing I came to notebook opened the lid and .... there was it ... yes nothing more .... system wake was ready in a blink of an eye .... as a Windows man tired down by Vista start up coffee breaks  .... I decided to switch completely to Apple ... everything ... notebook, phone, Apple TV, routers ... and it was decided really in that very first moment ... moment that one could easily miss - Snow Leopard wake.

You could understand that despite all Lions and successors bringing nice features the sacred one, wake up, was not such satisfying. But it was still FAST.

BUT not for long. Wake up started steadily slowing down. I cant tell when it started probable back two years ago after Lion was introduced. And it lead to unacceptable levels - it was 'similar' like back in windows times even I started to think twice if I need to close lid or not - just to prevent a wake up. Terrible.

I have tried many fixes like optimizing disk, keeping minimum apps open, clearing out all login/wake up utils/apps some with luck some without.

The issue 'resolved' itself as a by product when I found work around for fan noise issue.

SMC restart has helped also with lagging wake.


### Ultimate fix?
On July 31<sup>st</sup> Apple published MacBook Air EFI Firmware update 2.9.1 where admits issues of fan and slow wake up on mid 2011 mba. Well wording in the description plays down the severity of issues and scale of affected mba models ... but ... ?

Hurray ...hope I will never go through similar experience again.

![My helpful screenshot](/assets/2014/EFI-update.png)
_____

[^1]:Macbook Air mid 2011
[^2]:Apple support article with SMC restart procedure [here](http://support.apple.com/kb/HT3964?viewlocale=en_US&locale=en_US).
