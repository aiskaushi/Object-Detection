# Object-Detection using Raspberry pi

Object and Animal Recognition With Raspberry Pi and OpenCV

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Basic and Initial Requirements
1. Download the link for armhf-image
   ```bash
   https://downloads.raspberrypi.org/raspios_armhf/images/raspios_armhf-2021-05-28/
1. Clone the repository.
   ```bash
   git clone https://github.com/aiskaushi/Object-Detection.git






**Setting Up Open-CV for Object Detection**
1.$ sudo apt-get update && sudo apt-get upgrade

2.$ sudo nano /etc/dphys-swapfile
**The change the number on CONF_SWAPSIZE = 100 to CONF_SWAPSIZE=2048.** 

3.$ sudo apt-get install build-essential cmake pkg-config
4.$ sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev
5.$ sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
6.$ sudo apt-get install libxvidcore-dev libx264-dev
7.$ sudo apt-get install libgtk2.0-dev libgtk-3-dev
8.$ sudo apt-get install libatlas-base-dev gfortran
9.$ sudo pip3 install numpy
10.$ wget -O opencv.zip https://github.com/opencv/opencv/archive/4.4.0.zip
11.$ wget -O opencv_contrib.zip https://github.com/opencv/opencv_contrib/archive/4.4.0.zip
12.$ unzip opencv.zip
13.$ unzip opencv_contrib.zip
14.$ cd ~/opencv-4.4.0/
15.$ mkdir build
16.$ cd build
17.$ cmake -D CMAKE_BUILD_TYPE=RELEASE \
18.$ -D CMAKE_INSTALL_PREFIX=/usr/local \
19.$ -D INSTALL_PYTHON_EXAMPLES=ON \
20.$ -D OPENCV_EXTRA_MODULES_PATH=~/opencv_contrib-4.4.0/modules \
21.$ -D BUILD_EXAMPLES=ON ..
22.$ make -j $(nproc)      ** #This | make | Command will take over an hour to install and there will be no indication of how much longer it will take. **
23.$ sudo make install && sudo ldconfig
24.$ sudo reboot
