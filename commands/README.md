# Commands Used in the Raspberry Beret Tutorial

## Prepare the Pi
#### Update
    sudo apt-get update && sudo apt-get upgrade
#### Find IP Address
    hostname -I

## Piezo RTTTL Music Setup
#### Install Java Version 8
    sudo apt-get install oracle-java8-jdk
#### Check Java Version
    java -version
#### Download Pisoundo Jar
    wget https://cdn-learn.adafruit.com/assets/assets/000/023/642/original/pisoundo-0.0.1-SNAPSHOT-jar-with-dependencies.jar
#### Launch RTTTL Jar File
    sudo java -jar pisoundo-0.0.1-SNAPSHOT-jar-with-dependencies.jar
#### Launch Raspberry Beret Jar File
    sudo java -jar pisoundo-raspberry-beret.jar

## Neopixel Setup
#### Install Prerequsite Packages
    sudo apt-get install build-essential python-dev git scons swig
#### Download RPi Library for Neopixels
    git clone https://github.com/jgarff/rpi_ws281x.git
#### Install Library
    cd python
    sudo python setup.py install
#### Edit Strandtest file to Number of Neopixels
    sudo nano strandtest.py
#### Launch the Strandtest Program
    sudo python ./strandtest.py

## Setup Camera Module
#### Enable Camera
    sudo nano raspi-config
#### Install RPi-Cam-Web-Interface
    git clone https://github.com/silvanmelchior/RPi_Cam_Web_Interface.git
    cd RPi_Cam_Web_Interface
    chmod u+x *.sh
    ./install.sh
