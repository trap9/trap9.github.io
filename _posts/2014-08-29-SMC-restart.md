---
layout: post
title: "How to stop MBA slow wake and excessive fan noise?"
description: "First aid kit tool - SMC restart"
category: articles
tags: [mba, os x, troubleshooting, smc]
author: jiri_zoth
---
### Does your MBA have slow wake? Has its fan gone crazy? Mine did too.
There was a pretty nasty thing about my MBA[^1]. Over last two years I have started experiencing various issues that were progressively decreasing my satisfaction with the Apple product. And believe me, I was not happy, cos like any other Apple fan, I want to feel special :-)


Shortcut:

```
 press the (left side) Shift-Control-Option keys and the power button at the same time.
```
For the full procedure to troubleshoot the issues described here, refer to the Apple site[^2].

## The story
Over the time and after many hours and hours ... and ... yeah ... hours spent. I nailed down the following repetitive and irritating issues:

1. fan noise - under unknown conditions, fan speed and noise went up to VERY unacceptable levels and there was no way to get it back even when Activity Monitor showed essentially NO CPU load and the temperature and ventilation were ok.
2. slow wake up - since the install of OS X Lion, the wake up was progressively longer and longer. I did many tests to find the root cause. For example I learned that leaving Safari open with multiple tabs, especially if there is dynamic content in Flash, badly affects wake up time, Or I cleared out login items and utilities hooked on start up/wake up. None of these led me to an ultimate fix.
3. battery started to be vicious - I was experiencing sudden charge drops and the overall battery life was decreasing.

4. Mail started to ask for account passwords from time to time. Actually, it took me several occasions till I realized that there is an issue, and I started to be annoyed. You have to understand, I have apprx. 10 email accounts configured in my Mail app. So, every time the issue appeared it was 10x work, and the frequency raised and raised.

The good news is I have found how to fix the issues above. In this post I will elaborate on fan noise, battery and slow wake up as these issues have the same denominator.     I will publish, in my next post, a fix to the Mail issue of 'forgotten passwords'.

### Fan noise
Struggling with raging fan in my MBA over the period of apprx. 2 years with volatile success, I have nailed down that there is something called SMC and from time to time it can get spoiled and then it imposes negative effects on my MBA such as an outrageous fan. So, the cure is to RESTART SMC and bring your MBA back into line.

### Battery depreciation
One could expect battery depreciation over the course of time and as well se the necessity to replace the battery in order to get back increased availability in battery hours. BUT, is it ok to start feeling discomfort after 12-18 months? and a rapid decline?
Finally I have checked my battery with the CoconutBattery utility - and learned that the battery status is: service. The detailed log said that the battery is not functioning properly and a replacement is needed. Well, I bought a new battery and replaced the old one.

I connected the dots. Most likely because of my long term issues with MBA EFI firmware, mitigated by the SMC restart from time to time, fan noise issues led to enormous energy consumption and it badly affected the battery lifetime.

### Slow wake up
I still remember my very first experience with Apple notebook. It was the first model MBA with OS X Snow Leopard. The experience was amazing. I came to the notebook, opened the lid and it was there! Yes, nothing more nothing less, the system was ready in a blink of an eye! As a Windows man tired of Vista start up coffee breaks, I was stunned. I decided to switch completely to Apple - everything - notebook, phone, Apple TV, routers etc. And that decision came really in that very first moment. The moment that one could easily miss - Snow Leopard's awakening.

You could understand that, despite all Lions and their successors bringing nice features, the sacred one, wake up, was not as satisfying. But it was still FAST.

BUT not for long. Wake up started steadily slowing down. I can't tell when it started - probably back two years ago, after Lion was introduced. And it led to unacceptable levels - it was 'similar' to back in the times of Windows. I even started to think twice about whther I needed to close the lid or not - just to prevent a wake up. Terrible.

I have tried many fixes like optimizing disk, keeping minimum apps open, clearing out all login/wake up utils/apps - some with luck, some without.

The issue 'resolved' itself as a by-product when I found a workaround for the fan noise issue - the SMC restart.

The SMC restart has also helped with the lagging wake.


### Ultimate fix?
On July 31<sup>st</sup>, Apple published MacBook Air EFI Firmware update 2.9.1 where it admits issues on the fan and slow wake up on mid-2011 MBA. Well, the wording in the description plays down the severity of issues and scale of the affected MBA models ... but ... ?

Hurray ...hope I will never go through a similar experience again.

![My helpful screenshot](/assets/2014/EFI-update.png)
_____

[^1]:Macbook Air mid 2011
[^2]:Apple support article with SMC restart procedure [here](http://support.apple.com/kb/HT3964?viewlocale=en_US&locale=en_US).
