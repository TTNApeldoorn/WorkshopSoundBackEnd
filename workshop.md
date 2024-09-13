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

# Prepare the Raspberry

 1. Install Raspberry Pi Imager ([Download here](https://www.raspberrypi.com/software/) latest version) on the OS of your laptop.
 2. With Raspberry Pi Imager select Model, (PI4 or later)
 3. Select the OS: Raspberry Pi OS (Other) --> Raspberry Pi OS Lite (64-bit)
 4. select storage medium: SD-card inserted. 
 