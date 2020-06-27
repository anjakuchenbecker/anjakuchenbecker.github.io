---
layout: post
title: Project presentation | My Smart Home Solution - Part 1
---

I want to start my blog with the presentation of my self-made Smart Home solution I'm working in my spare time. In part 1 of this series I'll give you a general overview of my solution.

# Motivation
I've started with the installation of some WLAN IP cameras at my home but was very bugged after a short time for two main reasons:
1. The integrated motion detection flooded me with e-mails (with attached camera pictures) the whole day. Most time the reason was the change of the brightness (sun vs shadows or darkness vs headlights coming from cars or bicycles). Checking such e-mails and delete 99% of them makes no fun. Also tweaking the camera settings (exclude specific areas from motion detection or reducing the sensitivity) did not lead to the desired result. 
2. I've started directly with two different camera vendors (indoor / outdoor) therefore I had to handle two (buggy and slow) native smartphone apps. On top of that, when leaving or coming home I had to start each app and turn on or off motion detection... in total for seven cameras. Also no fun, time consuming ceremony, believe me.

That was the time when I've started to develop my own web-based application which runs in an usual browser regardless of the operating system. And since I'm heavily interested in Machine Learning the first goal was also to combine my low-end WLAN cameras with an object detection model that is able to detect persons on pictures. I'm not interested in getting informed when the neighbor's cats cross my cameras view. 

My boyfriend was the "end customer" and "tester" to ensure that the application is easy to handle. Little by little I've integrated more and more devices that are running at my home. All stuff is controlled in one web app, no need to open any additional native vendor application.

I'm not yet finished - there are still items on my todo list to enhance the functionality and integrate more devices ;-)

# Screenshots
Because images say more than a thousand words let's start with screenshots. 
Please note that I have blackened the parts containing sensitive information and pictures from my cameras.

The app is separated in two main parts the dashboard and the room surveillance:

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_19.png){:class="img-posts"}

## Dashboard - Camera

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_1.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_2.png){:class="img-posts"}

Key Features
- Embedded front door camera view, you can request a new snapshot or a ten second live video stream
- Activate specific camera scene and (depending on the scene) also object detection (persons only) with one click.
- Whenever a person is detected on a picture you will receive an e-mail with attached pictures (person is surrounded with a blue box and percentage probability of the model on each person detected in the image)
- Based on the selected camera scene also the radiators are switched accordingly in the background
- Upcoming garbage collection appointments are displayed. You also receive an e-mail reminder the day before.

## Dashboard - Alarm System

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_3.png){:class="img-posts"}

Key Features
- Activate or deactivate your GSM alarm system

## Dashboard - Smart Plugs

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_4.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_5.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_6.png){:class="img-posts"}

Key Features
- Status indicator for each available smart plug
- Turn smart plugs on or off
- Set smart plug timer with related action (if supported by smart plug)

## Dashboard - Mower

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_7.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_8.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_9.png){:class="img-posts"}

Key Features
- Embedded mower camera view, you can request a new snapshot or a ten second live video stream
- Start or stop mower
- See details and status history of mower

## Dashboard - Remote Control

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_10.png){:class="img-posts"}

### Onkyo Receiver
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_11.png){:class="img-posts"}

Key Features
- Turn receiver on or off
- Volume control (increase / decrease volume, mute / unmute)
- Volume presets (background, TV, Movie)
- Source selection
- Radio station presets

### Dreambox SAT Receiver

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_12.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_13.png){:class="img-posts"}

Key Features
- Dreambox specific remote-control buttons (on / off, volume, ...)
- Channel list with integrated search

### Apple TV

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_14.png){:class="img-posts"}

Key Features
- AppleTV selector
- AppleTV specific remote-control buttons (Home, Menu, OK, ...)

## Dashboard - Climate

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_15.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_16.png){:class="img-posts"}

Key Features
- Information about temperature and humidity coming from temperature/humidity sensors
- Information about current setting and mode coming from radiator thermostats
- Set temperature for a specific radiator thermostat
- Switch to auto, comfort or eco mode for a specific radiator thermostat

## Dashboard - SONOS

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_17.png){:class="img-posts"}

Key Features
- SONOS Speaker selector
- Status highlighting
- Current volume
- Current title (in case of SONOS is in play mode)
- Current radio station
- Volume control (increase / decrease volume, mute / unmute)
- Volume presets (telco, normal, party)
- Radio station presets

## Dashboard - Key Finder

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_18.png){:class="img-posts"}

Key Features

Ad-hoc search can be triggered to determine
* distance (calculated based on measured power/TxPower and RSSI)
* temperature
* battery status

of Beacons nearby

## Room Surveillance

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_20.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_21.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_22.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_23.png){:class="img-posts"}
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_24.png){:class="img-posts"}

Key Features
- Embedded views of all cameras (indoor / outdoor)

## E-mail notifications

### Person detection notification

Whenever a person is detected on a picture you will receive an e-mail with attached pictures (person is surrounded with a blue box and percentage probability of the model on each person detected in the image):

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_26.png){:class="img-posts"}

### Upcoming garbage collection notification

Whenever there is at least one upcoming garbage collection appointment on the next day, you receive an e-mail reminder the day before at 7:15 pm (one e-mail for multiple upcoming garbage collection appointments):

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_25.png){:class="img-posts"}


# Platform
## Front End
- Responsive web application based on HTML, CSS, JavaScript, jQuery, Foundation
- Optimized for different device sizes (Smartphone, Tablets) operating system neutral (iOS or Android)

## Backend
- http-API based on Python which integrates the different hardware devices (apache, wsgi, flask)
- no database, in case of data must be stored simple json files are used
- Backend services based on Python
- Backend cron jobs based on Python
- Integrated logging

# Hardware

## Server
- Raspberry Pi 3 Model B+ with 32GB SD Card
- Remote server on which the object detection model and person detection backend service (based on Python) is deployed

## Devices
- WLAN IP Cameras (different vendors e.g. D-Link)
- GSM alarm system
- Gardena sileno city mower
- SONOS WLAN Speaker (One and Play:1)
- WLAN Smart Plugs (TP-Link, Shelly Plug)
- Onkyo Receiver TX-5081
- Dreambox DM520 Satellite Receiver
- AppleTV (AppleTV 1, AppleTV 4)
- ELV Mobile Alerts Gateway with attached temperature and humidity sensors (radio based)
- Eqiva Bluetooth Smart Radiator Thermostats
- Bluetooth Low Energy Beacons
