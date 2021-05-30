---
title: "Pi Processing Art"
date: 2019-10-27T23:53:00+01:00
draft: false
type: "project"
hideLastModified: true
summary: "Some base setup for Rasphberry PI"
summaryImage: "PiLogo.png"
tags: ["Interactive Art"]
weight: 15
---


<div class="columns">
    <div class="column is-4"></div>
    <div class="column is-4">
       <img src="raspberry-pi-icon-png-0.jpg" alt="Raspberry Pi" style="width:50%">
    </div>
<div class="column is-4"></div>
</div>

  {{<imageToClick imagePath = "RaspberryPIArtCollage.jpg" Capition = "Example That Expands"  width ="50%" >}}


*Last Modified: May 21, 2021*

# Summary 

This page document the steps on getting a Raspberry Pi up from scratch and setting it up for screensharing to access from a laptop (in this case a Macbook Pro) using a VPN connection.

I used these steps to create some visual art from a [Raspberry Pi computer](https://en.wikipedia.org/wiki/Raspberry_Pi) and software called [Processing](https://processing.org/) . Here's the finished "product":

<details><summary>What is A PI?</summary>
&nbsp

[Raspberry Pis](https://en.wikipedia.org/wiki/Raspberry_Pi) (aka "Pis") are small and inexpensive computers that have a variety uses including teaching computing, IoT, and art. Because of there small size and low cost they Pis are perfect for creating and curating interative art. 

</details>
&nbsp





<div class="columns">
    <div class="column is-6">
            {{<imageToClick imagePath = "IMG_0077.png" Capition = "Example That Expands"  width = "100%" resize = "1000x800" >}}
    </div>
    <div class="column is-6">
        {{<imageToClick imagePath = "IMG_0083.png" Capition = "Example That Expands"  width ="100%" resize = "600x400"  >}}
    </div>
</div>

<div class="columns">
    <div class="column is-6">
            {{<imageToClick imagePath = "IMG_0078.png" Capition = "Example That Expands"  width ="100%" resize = "600x400" >}}
    </div>
    <div class="column is-6">
        {{<imageToClick imagePath = "IMG_0079.png" Capition = "Example That Expands"  width ="100%" resize = "600x400">}}
    </div>
</div>


# Setting up the PI


## Step 1: Get the equipment

Get a Pi (mini computer) and needed auxillary items to get started. 

* **1:** Get or have a Raspberry PI: [For Example](https://www.raspberrypi.org/products/raspberry-pi-4-model-b/?variant=raspberry-pi-4-model-b-4gb)
* **2:** MicoSD card (I use 32 or 64GB): 
         
<div class="columns">
    <div class="column is-4"></div>
    <div class="column is-5">
     {{<imageToClick imagePath = "MicroSdCardv2.jpg" Capition = "MicroSD Card"  width ="50%">}}
    </div>
<div class="column is-5"></div>
</div>

* **3:** If you have a Raspberry Pi 4 you will need micro HDMI to regard HDMI to connect to monitor. Adapters may have come with your Pi but if no you [can get them](https://www.amazon.com/gp/product/B00B2HORKE/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1) 
* **4:** A power adapter if not in your kit [get power](https://www.amazon.com/Raspberry-Power-Supply-USB-C-Listed/dp/B07W8XHMJZ/ref=sr_1_4?crid=224A2MQZYOJNJ&dchild=1&keywords=raspberry%2Bpi%2B4%2Badapter&qid=1613622754&sprefix=raspb%2Caps%2C182&sr=8-4&th=1)
* **5:** A computer with an way to read/write from a SD or microSD card (with adapter). The micro to standard SD adapter usually come with purchase of microSD 




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




<details><summary>Continue</summary>


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

</details>




