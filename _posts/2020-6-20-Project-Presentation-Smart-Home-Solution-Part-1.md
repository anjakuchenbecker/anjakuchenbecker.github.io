---
layout: post
title: Project presentation | My Smart Home Solution - Part 1
---

I want to start my blog with the presentation of my self made Smart Home Solution I'm working in my spare time. In part 1 of this series I'll give you a general overview of my solution.

# Motivation
TBD

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
- TBD

## Dashboard - Remote Control

![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_10.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_11.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_12.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_13.png)
![_config.yml]({{ site.baseurl }}/images/Screenshot_Smart_Home_Web_App_14.png)

Key Features
- TBD

# Platform
## Front End
- Responsive web application based on PHP, HTML, CSS, JavaScript, jQuery, Foundation
- Optimized for different device sizes (Smartphone, Tablets) operating system neutral (iOS or Android)

## Backend
- http-API based on Python which integrates the differend hardware devices (apache, wsgi, flask)
- no database, in case of data must be stored simple json files are used
- Backend services based on Python
- Backend cron jobs based on Python

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
