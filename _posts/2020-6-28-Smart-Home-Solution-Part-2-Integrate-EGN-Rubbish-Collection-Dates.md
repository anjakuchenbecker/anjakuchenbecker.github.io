---
layout: post
title: My Smart Home Solution - Part 2 | Integrate EGN rubbish collection dates in your Smart Home Solution 
---

One part within my self-made Smart Home solution is the integration of rubbish collection dates from my local responsible provider: EGN (Entsorgungsgesellschaft Niederrhein mbH). In this very short post I'll share with you how to read the [EGN Abfallkalender](https://www.egn-abfallkalender.de/kalender) programmatically with Python, maybe this is useful for your own Smart Home solution.

# Table of contents
- [Motivation](#motivation)
- [Solution](#solution)
- [Source Code](#source-code)

# Motivation
Even though there is a (from time to time really buggy) EGN Abfallkalender App available within the App Store you know from my [first blog entry](https://anjakuchenbecker.github.io/Project-Presentation-Smart-Home-Solution-Part-1/#motivation) that I hate to use a lot of apps. Also the push notification that is provided by the EGN app is nice but very volatile in case you don't put out the related garbage container directly after it appears: out of sight out of mind ;-)

# Solution
In order to increase the chance not to forget next upcoming rubbish collection dates I've integrated the EGN appointments within my Smart Home solution.

Upcoming garbage collection appointments w.r.t. this and next calendar week are displayed permanently on the to right of the dashboard:
![_config.yml]({{ site.baseurl }}/images/Screenshot_EGN_1.png){:class="img-posts"}

In addition, I receive an e-mail reminder the day before at 7.15 pm in case of on the next day there is an appointment:
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_25.png){:class="img-posts"}

So now, the chance to forget to put out the garbage containers is reduced to an absolute minimum :-)

# Source Code
On GitHub I've uploaded a Jupyter notebook with the basic code to retrieve the [EGN Abfallkalender](https://www.egn-abfallkalender.de/kalender) programmatically:

[Read_EGN_Abfallkalender_Programmatically_With_Python.ipynb](https://github.com/anjakuchenbecker/smarthome-egn-calendar/blob/master/Read_EGN_Abfallkalender_Programmatically_With_Python.ipynb)

Even this provided code is only a small excerpt from my entire solution for the EGN calendar integration, I hope maybe someone can take advantage of it.
