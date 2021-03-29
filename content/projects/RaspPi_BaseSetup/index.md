---
title: "Raspberry Pi Base Setup For Interactive Art"
date: 2019-10-27T23:53:00+01:00
draft: true
type: "project"
hideLastModified: true
summary: "Some base setup for Rasphberry PI"
summaryImage: "PiLogo.png"
tags: ["Interactive Art"]
weight: 65
---

{{<rawhtml>}}


<script src="https://unpkg.com/formiojs@latest/dist/formio.embed.js?src=https://qcaegiyxrnlbkdu.form.io/formsandbox"></script>


<div class="columns">
    <div class="column is-3"></div>
    <div class="column is-6">
       <center><img src="raspberry-pi-icon-png-0.jpg" alt="Raspberry Pi" style="width:50%">
    </div>
<div class="column is-3"></div>
</div>
{{</ rawhtml>}}

*Last Modified: February 13, 2021*

# Summary

This page covers getting a Raspberry Pi up from scratch and setting it up for screensharing to access from a laptop (in this case a Macbook Pro)

# Background

[Raspberry Pis](https://en.wikipedia.org/wiki/Raspberry_Pi) (aka "Pis") are small and inexpensive computers that have a variety uses including teaching computing, IoT, and art. Because of there small size and low cost they Pis are perfect for creating and curating interative art. 

I use Pis to connect to TVs for interactive art. 

Everytime I setup a new Pi I make a series of tweaks to set things as they come up - such as setting up for remote access, and installing new software. Each time I do it alittle differently -- so I lose some consistency and time googling. 

No longer! I am documenting it here:


#### Raspberry Pi Overview

* The computers are approximately the size of two decks of cards. 
* The 4th generation Raspberry Pis (aka Pis) are readily available and include wireless ethernet and dual monitor (1080) capabilities.  
* You can buy a 4th generation Pi for $30 with RAM 2GB of memory or $50 with 4GB of RAM memory

## Step 1: Get the equipment

Get a Pi (mini computer) and needed auxillary items to get started. 

* **1:** Get or have a Raspberry PI: [For Example](https://www.raspberrypi.org/products/raspberry-pi-4-model-b/?variant=raspberry-pi-4-model-b-4gb)
* **2:** MicoSD card (I use 32 or 64GB):
* **3:** If you have a Raspberry Pi 4 you will need micro HDMI to regard HDMI to connect to monitor. Adapters may have come with your Pi but if no you [can get them](https://www.amazon.com/gp/product/B00B2HORKE/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1) 
* **4:** A power adapter if not in your kit [get power](https://www.amazon.com/Raspberry-Power-Supply-USB-C-Listed/dp/B07W8XHMJZ/ref=sr_1_4?crid=224A2MQZYOJNJ&dchild=1&keywords=raspberry%2Bpi%2B4%2Badapter&qid=1613622754&sprefix=raspb%2Caps%2C182&sr=8-4&th=1)
* **5:** A computer with an way to read/write from a SD or microSD card (with adapter). The micro to standard SD adapter usually come with purchase of microSD 

<img src="MicroSdCard.png" alt="MicroSD Card" style="width:600px"></a><p>

* Raspberry Pi:

<img src="RaspberryPIPluggedIn.png" alt="MicroSD Card" style="width:600px"></a>

## Step 2: Get Etcher

* Go to: https://www.balena.io/etcher/
* Download Etcher for desired operating system.

<img src="Etcher.png" alt="Picture of Etcher Website" style="width:600px"></a><p>

## Step 3: Download the raw image

* Go to: https://www.raspberrypi.org/downloads/raspberry-pi-os/
* (For Mac) download the .zip file
* I chose "Raspberry Pi OS (32-bit) with desktop and recommended software"

{{< imageToClick imagePath = "RaspPiDownload.png" Capition = "Picture of Raspberry PI OS Download"  width ="50%">}}



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
* Plug in the Pi

## Step 6: Walk through One Time Prompts

After the first boot there are some one-time prompt that guides some one time setups:
* Set Country
* Change password
* Setup Screen
* Select Wireless Network
* Update Software
* Restart once "Setup Complete"


## Step 7: Config Pi to Allow For Screen Sharing

### **Get to *Raspberry PI Config*:**

From top left PI menu: PI -> Preferences -> Raspberry PI Config

{{< imageToClick imagePath = "turnOnVnc.png" Capition = "Raspbery PI Configuration"  width ="50%">}}


**Turn VNC from GUI:**

From new window go to Interfaces tab. Flip the VNC toggle to "enabled".

{{< imageToClick imagePath = "turnOnVNCServer.png" Capition = "Turn On VNC Server"  width ="50%">}}

**Setup remote user**

Open VNC Software from top right corner. Go to "User and Permissions"

{{< imageToClick imagePath = "setVNCUserName.png" Capition = "Set up VNC user"  width ="50%">}}

**Setup remote password**

You have to setup a password to connect remotely - such as with Mac. 

If you don't set a password you won't be able to connect. So, set a password (remember it):

{{< imageToClick imagePath = "setVNCpassword.png" Capition = "Set VNC Password"  width ="50%">}}

Make sure to set a password for MAC "Go To Server"

Open the command line and run:

{{< code language="term" >}}
sudo raspi-config
{{< /code >}}


Need to build out these steps:
https://fullstackproblemsolver.atlassian.net/wiki/spaces/FSPS/pages/279478273/Raspberry+PI+setup