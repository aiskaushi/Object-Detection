# Object-Detection
Object and Animal Recognition With Raspberry Pi and OpenCV
Basic and Initial Requirements
How to Flash the Old 'Buster' Raspberry Pi OS to a Micro-SD
Download this OS raspios_armhf
https://downloads.raspberrypi.org/raspios_armhf/images/raspios_armhf-2021-05-28/

**Enable camera and SSH**
$ sudo reboot
******Try to run ******
$ Raspistill -o test.jpg
$ Sudo apt-get  update
$ Sudo apt-get  upgrade
$ Raspistill -o test.jpg
**Install picamera**
$ sudo apt-get update
$ sudo apt-get install python-picamera python3-picamera

**Open a Python 3 editor, such as Thonny Python IDE:
 Open a new file and save it as camera.py.
Note: it’s important that you never save the file as picamera.py.
Setting Up Open-CV for Object Detection**

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
