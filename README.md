![Example Image](https://github.com/aiskaushi/Object-Detection/blob/main/image1.jpg)


# Object-Detection using Raspberry pi

Object and Animal Recognition With Raspberry Pi and OpenCV

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)

## Basic and Initial Requirements
0. Download the link for armhf-image
   ```bash
   https://downloads.raspberrypi.org/raspios_armhf/images/raspios_armhf-2021-05-28/
## Check the current size of the Raspberry Pi OS Install. 
1. type this command
   ```bash
   df -h /
## Cutting the Fat from Raspberry Pi OS.   
2. type this command
   ```bash
   dpkg-query -Wf '${Installed-Size}\t${Package}\n' | sort -n -r | head -n 20

## First let’s prepare the system for the installation.
3. Remove unnecessary files
   ```bash
   sudo apt-get -y purge wolfram-engine
   sudo apt-get -y purge libreoffice*
   sudo apt-get -y clean
   sudo apt-get -y autoremove

## Setting Up Open-CV for Object Detection
1. Update & upgrade your raspberry pi-4
   ```bash
   sudo apt-get update && sudo apt-get upgrade
2. The change the number on CONF_SWAPSIZE = 100 to CONF_SWAPSIZE=2048.
   ```bash
   sudo nano /etc/dphys-swapfile
3. just copy and paste
   ```bash
   sudo apt-get install build-essential cmake pkg-config
3. ff   



2. Clone the repository.
   ```bash
   git clone https://github.com/aiskaushi/Object-Detection.git
