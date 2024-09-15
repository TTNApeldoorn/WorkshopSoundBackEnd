# Required material

 - Laptop (to install the OS on a micro SD card)
 - Raspberry Pi 4 or higher
 - 5V power supply for the selected Raspberry Pi.
 - MicroSD card 32 GB or more. (Do consider using a Extreme XDHC card or equivalent because of wear out due to extensive read-write).
 - UTP network cable to connect to wired internet. 
 - micro-hdmi to hdmi cable to connect to a monitor.
 - A monitor with HDMI. (as an alterative consider a *hdmi to usb adapter* to have your laptop act as a monitor uring the camera app with Windows. These adapters can be puchased from Amazon for less than 9 Euros).
 - USB keyboard.
 
 *Note: Although this readme was developed using a Raspberry Pi 4000, compatible minicomputers are likley to be useable. This was not tested.*
 
# Installation
Installation of the required software can be done in multiple ways. This howto will use Docker compose to streamline installation. 

## Warning:
It is known that some docker containers for this workshop will not work on 32-bit OS. Therefore install only a 64-bit OS for this hwowto.

# Install OS on micro SD card
More extensive help can be found at [Getting started with your Raspberry Pi](https://www.raspberrypi.com/documentation/computers/getting-started.html).

 1. Install Raspberry Pi Imager; Download ([here](https://www.raspberrypi.com/software/) the latest version) on the OS of your laptop.
 2. With Raspberry Pi Imager select Model, (PI4 or later)
 3. Select the OS: Raspberry Pi OS (Other) --> Raspberry Pi OS Lite (64-bit)
 4. select storage medium: SD-card inserted. 
 5. click next.
 6. Now the installer asks for *OS customisation*. Select *EDIT SETTINGS*.
    a. If required, set the *hostname* of your raspberry.
    b. **Set you username and password.** *You may want to write these down somewhere.*
    c. If you want to connect to WiFI, set your SSID and Password. **With this workshop we connect to the WiFi using SSID: xxxx and password: yyyyyy**
    d. If required, set you locale settings: 
       - Time zone: Europe/Amsterdam
       - Keyboard layout: us
 7. When all OS settings are set, choose *YES*.
 8. When the installer warns that all content of the selected media will be erased, **ensure you selected the right media**, and click *YES*.
 9. The installer starts downloading the image and write it to the micoSD card. 
 10. After the installer finalised writing, place the storage-medium in your Raspberry Pi and boot it.
 
# Finalising the installation. 

 1. Login to your raspberry with the user name and credentials provided with step 6b.
 2. Ensure that you have connection to the network or internet. type `$ ip a` to see the network setting currectly active. 
    - with `wlan0` you see a ip-address at `inet` when you are connected and received an ip-address over dhcp. 
    - if the command `$ ping 8.8.8.8` repies with a time in ms, Google dns replies so you have internet access. 
 3. Update the os to teh latest version with `sudo apt update && sudo apt upgrade -y`.
 4. reboot your Raspberry Pi with the command `sudo shutdown -r 0` and you are good to go to the next phase of the workshop. 
 
## Install options. 
Raspberry Pi 4, 400, and 5 are capeable of booting from USB instead of micro USB. Therefore you may decide to write the image to a USB memory stick in the previous instructions. 

To make the Raspberry Pi 4, 400 or 5 boot from USB follow [this tutorial](https://linuxconfig.org/boot-your-raspberry-pi-from-a-usb-a-tutorial). 

# Install software. 
For this howto, the following software is required:

 - git,
 - docker, docker-compose.
 
## git. 
To install git give command `$ sudo apt install git` and type `y`(es) to continue installing. 
As we are only using git to pull the repository used for this workshop, no further configuration is required. 

## docker.
blah