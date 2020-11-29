---
title: "Raspberry Pi Base Setup For Interactive Art"
date: 2019-10-27T23:53:00+01:00
draft: true
type: "project"
hideLastModified: false
summary: "Some base setup for Rasphberry PI"
summaryImage: "PiLogo.png"
tags: ["Interactive Art"]
weight: 65
---

# Background

[Raspberry Pis](https://en.wikipedia.org/wiki/Raspberry_Pi) (aka "Pis") are small and inexpensive computers that have a variety uses including teaching computing, IoT, and art. Because of there small size and low cost they Pis are perfect for creating and curating interative art. 

I use Pis to connect to TVs for interactive art. 

Everytime I setup a new Pi I make a series of tweaks to set things as they come up - such as setting up for remote access, and installing new software. Each time I do it alittle differently -- so I lose some consistency and time googling. 

No longer! I am documenting it here:

### Raspberry Pi Overview
* The computers are approximately the size of two decks of cards. 
* The 4th generation Raspberry Pis (aka Pis) are readily available and include wireless ethernet and dual monitor (1080) capabilities.  
* You can buy a 4th generation Pi for $30 with RAM 2GB of memory or $50 with 4GB of RAM memory

https://www.rcmtiteurope.com/index.php/2019/06/04/developing-an-app-with-raspberry-pi-behind-the-scenes-of-horreum-weather/


## Step 1: Get the equipment


* Get or have a Raspberry PI: https://www.raspberrypi.org/products/raspberry-pi-4-model-b/?variant=raspberry-pi-4-model-b-4gb
* MicoSD card:

<img src="MicroSdCard.png" alt="MicroSD Card" style="width:600px"></a><p>

*Raspberry Pi:

<img src="RaspberryPIPluggedIn.png" alt="MicroSD Card" style="width:600px"></a>




## Step 2: Get Etcher

* Go to: https://www.balena.io/etcher/
* Download Etcher for desired operating system.

<img src="Etcher.png" alt="Picture of Etcher Website" style="width:600px"></a><p>

## Step 3: Download the raw image

* Go to: https://www.raspberrypi.org/downloads/raspberry-pi-os/
* (For Mac) download the .zip file
* I chose "Raspberry Pi OS (32-bit) with desktop and recommended software"

<img src="RaspPiDownload.png" alt="Picture of Raspberry PI OS Download" style="width:600px"></a><p>



## Step 4: Use Etcher to flash your microSD card

* Unzip downloaded file to an .img
* Insert card into computer
* Open Etcher it should see insert microSD
* Select image and flash card
* Flashing can take a few to many minutes, so be patient
* After flashing Etcher will validate the flash, this takes time to, so continue to be patient.

<img src="EtcherFlash.png" alt="Picture of Raspberry PI OS Download" style="width:600px"></a><p>

## Step 5: Boot ya PI

* Get card from your Mac/PC
* Physically insert microSD into PI as designed
* Plug in physical keyboard and mouse
* Plug in monitor
* Plug in the Pie

## Step 6: Walk through One Time Prompts

After the first boot there are some one-time prompt that guides some one time setups:
* Set Country
* Change password
* Setup Screen
* Select Wireless Network
* Update Software
* Restart once "Setup Complete"


## Step 7: Enable VNC Server

Make sure to set a password for MAC "Go To Server"

Need to build out these steps:
https://fullstackproblemsolver.atlassian.net/wiki/spaces/FSPS/pages/279478273/Raspberry+PI+setup