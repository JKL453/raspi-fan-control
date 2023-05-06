# Raspberry Pi PWM Fan Control

This script can run in background on a Raspberry Pi to control the RPM of a 5V Noctua fan via PWM, based on the CPU temperature of th Pi.

The original code was created by [DriftKingTW](https://github.com/DriftKingTW), and keeps my Raspberry Pi Cluster perfectly cool.

## Install

Create a folder on your Pi
```
mkdir python-scripts
cd mkdir 
```
Download the script 
```
wget https://raw.githubusercontent.com/JKL453/raspi-fan-control/master/fan_control.py
```
Start the script with
```
python fan_control.py
```
and add it to auto start by editing ```rc.local```
```
sudo nano /etc/rc.local
```
and add this before ```exit 0```
```
python /home/pi/Scripts/fan_control.py &
```

Restart the Pi to make sure everything works as expected.



