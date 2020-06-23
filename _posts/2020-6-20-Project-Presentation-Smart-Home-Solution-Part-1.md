---
layout: post
title: Project presentation | My Smart Home Solution - Part 1
---

I want to start my blog with the presentation of my self-made Smart Home solution I'm working in my spare time. In part 1 of this series I'll give you a general overview of my solution.

# Motivation
I've started with the installation of some WLAN IP cameras at my home but was very bugged after a short time for two main reasons:
1. The integrated motion detection flooded me with e-mails (with attached camera pictures) the whole day. Most time the reason was the change of the brightness (sun vs shadows or darkness vs headlights coming from cars or bikecycles). Checking such e-mails and delete 99% of them makes no fun. Also tweaking the camera settings (exclude specific areas from motion detection or reducing the sensitivity) did not lead to the desired result. 
2. I've started directly with two differend camera vendors (indoor / outdoor) therefore I had to handle two (buggy and slow) native smartphone apps. On top of that, when leaving or coming home I had to start each app and turn on or off motion detection... in total for seven cameras. Also no fun, time consuming ceremony, believe me.

That was the time when I've started to develop my own web based application which runs in an usual browser regardless of the operating system. And since I'm heavily interested in Machine Learning the first goal was also to combine my low end WLAN cameras with an object detection model that is able to detect persons on pictures. I'm not interested in getting informed when the neighboors cats cross my cameras view. 

My boy friend was the "end customer" and "tester" to ensure that the application is easy to handle. Little by little I've integrated more and more devices that are running at my home. All stuff is controlled in one web app, no need to open any additional native vendor application.

I'm not yet finished - there are still items on my todo list to enhance the functionality and integrate more devices ;-)

# Screenshots
Because images says more than a thousand words let's start with screenshots. 
Please note that I have blackened the parts containing sensitive information and pictures from my cameras.

## Dashboard - Camera

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_1.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_2.png)

Key Features
- Embedded front door camera view, you can request a new snapshot or a ten second live video stream)
- Activate specific camera scene and (depending on the the scene) also object detection (persons only) with one click.
- In case of a person is detected on a picture you'll receive an e-mail with attached pictures (person is surrounded with a blue box and percentage probability of the model on each person detected in the image)
- Based on the selected camera scene also the radiators are switched accordingly in the background
- Upcoming garbage collection appointments are displayed. You receive also an e-mail reminder the day before.

## Dashboard - Alarm System

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_3.png)

Key Features
- Activate or deactivate your GSM alarm system

## Dashboard - Smart Plugs

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_4.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_5.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_6.png)

Key Features
- Status indicator for each available smart plug
- Turn smart plugs on or off
- Set smart plug timer with related action (if supported by smart plug)

## Dashboard - Mower

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_7.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_8.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_9.png)

Key Features
- Start or stop mower
- See details and status history of mower

## Dashboard - Remote Control

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_10.png)

### Onkyo Receiver
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_11.png)

Key Features
- Turn receiver on or off
- Volume control (increase / decrease volumne, mute / unmute)
- Volume presets (background, TV, Movie)
- Source selection
- Radio station presets

### Dreambox SAT Receiver

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_12.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_13.png)

Key Features
- Dreambox specific remote control buttons (on / off, volume, ...)
- Channel list with integrated search

### Apple TV

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_14.png)

Key Features
- AppleTV selector
- AppleTV specific remote control buttons (Home, Menu, OK, ...)

## Dashboard - Climate

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_15.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_16.png)

Key Features
- TBD

## Dashboard - SONOS

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_17.png)

Key Features
- TBD

## Dashboard - Key Finder

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_18.png)

Key Features
- Ad-hoc search can be triggered to determine the following information of Beacons nearby
-- distance
-- temperature
-- battery status

# Platform
## Front End
- Responsive web application based on HTML, CSS, JavaScript, jQuery, Foundation
- Optimized for different device sizes (Smartphone, Tablets) operating system neutral (iOS or Android)

## Backend
- http-API based on Python which integrates the differend hardware devices (apache, wsgi, flask)
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
- Eqiva Bluetooth Smart Radiator Thermostat
- Bluetooth Low Energy Beacon
