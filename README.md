# mountainpi
![slice1](assets/slice1.png)
#### User documentation for Silke Com for Mountain Top Pi.
Each Mountain Top Raspberry Pi is a V3 Raspberry Pi with an RTL-SDR dognle attached.  The Mountain Top RPi OS build also includes a web based DVR interface with motion detection designed to use inexpensive USB web cameras.  It also includes a web based GPIO (General Purpose Input Output) page for toggleing GPIOs states to 0V or +5v.  The project was lead by the 😼Cat Lord Andy Record, with all development by 👨‍💻 Oran Collins <[wisehackermonkey](https://www.github.com/wisehackermonkey)>.

# Quick start:
### - [Connect Radio](#how-to-connect-to-web-based-sdr)
### - [View Webcam](#how-to-connect-to-web-based-camera-system)
### - [Toggle Raspberry pi pins (GPIO)](#how-to-connect-to-and-toggle-gpios)
## Admin Guilds
### - [Change Hostname](#set-raspberry-pis-hostname)
### - [Change IP Address](#how-to-set-ip-address)
### - [Change webiopi password](#how-to-set-webiopi-password)
### - [Change Default RPI's password](#set-raspberry-pis-password)
### - [Change webcam password](###how-to-change-the-default-password)
### - [Advanced](#advanced)

# [DOWNLOAD RPI Image here](https://mega.nz/file/kE1nFCqJ#GcHeHwa-VjEAzYPnRlEISpjaMustKIwGJkCFJIEr_1M) valid as of (20210206)
# How to connect to web based SDR 

### SDR Software:
#### Install basic SDR# software: https://airspy.com/download/  
#### Read this tutorial:      https://airspy.com/quickstart/  

<img src="assets/2021-02-06-15-38-26.png" width="400">
------
<img src="assets/2021-02-06-15-28-22.png" width="400">
### Extract and open `SDRSharp.exe`
<img src="assets/2021-02-06-15-30-11.png" width="400">
<img src="assets/2021-02-06-15-31-34.png" width="400">
<img src="assets/2021-02-06-15-31-53.png" width="400">
<img src="assets/2021-02-06-15-32-15.png" width="400">
<img src="assets/2021-02-06-15-32-52.png" width="400">
<img src="assets/2021-02-06-15-33-12.png" width="400">
<img src="assets/2021-02-06-15-33-33.png" width="400">
<img src="assets/2021-02-06-15-33-51.png" width="400">
<img src="assets/2021-02-06-15-34-09.png" width="400">
<img src="assets/2021-02-06-15-34-18.png" width="400">
<img src="assets/2021-02-06-15-34-43.png" width="400">
<img src="assets/2021-02-06-15-39-49.png" width="400">
<img src="assets/2021-02-06-15-35-19.png" width="400">
<img src="assets/2021-02-06-15-40-37.png" width="400">
#### Almost finished!
<img src="assets/2021-02-06-15-41-36.png" width="400">
<img src="assets/2021-02-06-15-41-57.png" width="400">
<img src="assets/2021-02-06-15-42-17.png" width="400">
<img src="assets/2021-02-06-15-42-42.png" width="400">
<img src="assets/2021-02-06-15-43-17.png" width="400">
<img src="assets/2021-02-06-15-46-46.png" width="400">
#### Set host to raspberry pi's ip address XXX.XXX.XXX.XXX for my network its 192.168.1.72
### Ip address = `192.168.1.72`
### Port = `1234`
### Sample rate = `0.25 MSPS`
<img src="assets/2021-02-06-15-47-48.png" width="400">
### Hit play, if everything was setup correctly you should hear radio static!
### Success!
<img src="assets/2021-02-06-15-59-45.png" width="400">

### Trouble shooting
#### If you get an error like this one, 
- check that the pi is running and on the same network
- the port is correct
- the ip address to the pi is valid and correct 
     `ping 192.168.1.72` or `ssh root@192.168.1.72` to test if its up
- restart sdr sharp
- check wifi/local system connectivity
- Remember, only one person can login to a site at any time.  The SDR# software will hang if someone else is connected to the device.
- NOTE: `sdr-sharp` often crashes if you dont hit `stop` before quitting as a habit always click stop before exiting 
<img src="assets/2021-02-06-15-49-01.png" width="400">

     -----------------
<br>
<br>
<br>

# How to connect to web based camera system  
### Camera System (motionEye): 

 <img src="2021-02-06-14-19-58.png" width="400">
#### IP address + Port number 
#### Note: the  "192.168.2.72' will be different for each network.
<!-- ```bash -->
## http://XXX.XXX.XXX.XXX:8765
<!-- ``` -->
#### Example 
```bash
http://192.168.2.72:8765/

```

<img src="assets/2021-02-06-14-21-26.png" width="400">
### Default admin account 
#### Username
```bash
admin
```
#### Password
```bash
spainFLOWER96@@
```
### Default user account (cant make changes to cameras)
#### Username
```bash
silkecom
```
#### Password (note the * are included)
```bash
enterSATURN35**
```
### How to change the default password
<img src="assets/2021-02-06-14-26-01.png" width="400">
<img src="assets/2021-02-06-14-29-36.png" width="400">
#### Note: "back up" before you make changes.

### If you set up motion detection, use email with the following SMTP info:
* Email addresses; mike@silkecom.com, Andre@silkecom.com, & others
* SMTP Server: xxxxxx
* SMTP port: xxxxx
* SMTP Account: xxxx
* SMTP Password: XXX
* From Address: site_name.rpicamera@silkecom.com
* Attached Pictures Time Span: “5”


<br>
<br>
------------------
<br>
<br>

# How to connect to and toggle GPIOs

### Turn GPIOs on and off
<img src="assets/2021-02-06-16-07-30.png" width="400">
<img src="assets/2021-02-06-16-07-50.png" width="400">
### http://192.168.2.72:8000/app/gpio-header
* ###### username 
> `silkecom`
*  ###### password 
> `&57wavesHUMAN`

<img src="assets/2021-02-06-16-08-13.png" width="400">
<img src="assets/2021-02-06-16-10-09.png" width="400">
### `OUT` = gpio pin is `ON`, and `IN` = gpio pin if `OFF`
<img src="assets/2021-02-06-16-11-52.png" width="400">
### Reference
* GPIO Info: https://www.raspberrypi.org/documentation/usage/gpio/
* How to drive a relay: https://projects-raspberry.com/raspberry-pi-driving-a-relay-using-gpio/

<br>
<br>
------------------
<br>
<br>
# Sys admin guide

# Set Raspberry pis Hostname
### login to pi
<img src="assets/2021-02-02-16-59-38.png" width="400">
### run `dietpi-config`
<img src="assets/2021-02-02-17-03-48.png" width="400">
<img src="assets/2021-02-02-17-04-10.png" width="400">
<img src="assets/2021-02-02-17-04-38.png" width="400">
<img src="assets/2021-02-02-17-04-54.png" width="400">
### change the hostname to what you want.
#### to hit 'OK' press `TAB` once then `enter`
<img src="assets/2021-02-02-17-06-14.png" width="400">
 
-----

# Set Raspberry pis password
### login to pi
#### Default password OS
```text
4orderTERMS%%
```
<img src="assets/2021-02-02-16-59-38.png" width="400">
### run `dietpi-config`
<img src="assets/2021-02-02-17-03-48.png" width="400">
<img src="assets/2021-02-02-17-04-10.png" width="400">
<img src="assets/2021-02-02-17-04-38.png" width="400">
<img src="assets/2021-02-02-17-08-25.png" width="400">
### enter you password , to hit 'OK' press `TAB` once then `enter` once
<img src="assets/2021-02-02-17-08-42.png" width="400">
 
-----

# How to set IP address
### login to pi
#### Default password OS
```text
4orderTERMS%%
```
<img src="assets/2021-02-02-16-59-38.png" width="400">
### run `dietpi-config`
<img src="assets/2021-02-02-17-03-48.png" width="400">
<img src="assets/2021-02-02-17-12-34.png" width="400">
<img src="assets/2021-02-02-17-12-55.png" width="400">
<img src="assets/2021-02-02-17-13-10.png" width="400">
### change the ip address
<img src="assets/2021-02-02-17-13-46.png" width="400">
### example:
<img src="assets/2021-02-02-17-14-32.png" width="400">
<img src="assets/2021-02-02-17-14-55.png" width="400">
### Done!
 
# How to set webiopi password
###  type in to rpi bash `webiopi-passwd`
<img src="assets/Screenshot_4.png" width="400">

-----
# Advanced 
# How to stop/start webiopi
```bash
service webiopi start
service webiopi stop
service webiopi status
service webiopi restart

#  or alternatively
systemctl start webiopi
systemctl stop webiopi
```
### Advanced: edit the system service 
```bash
location of service
/etc/systemd/system/webiopi.service
```
#### example [ source link: webiopi.service](https://raw.githubusercontent.com/doublebind/raspi/master/webiopi.service)
```bash
[Unit]
Description = WebIOPi
After = syslog.target network.target

[Service]
Type = simple
WorkingDirectory = /usr/share/webiopi/htdocs
ExecStart = /usr/bin/python3 -m webiopi -l /var/log/webiopi -c /etc/webiopi/config

[Install]
WantedBy = multi-user.target
```
### Fix issues with RTL-sdr server (pi side) not working
#### Stop, Restart and build
##### Clone docker-compose file 
```bash
git clone https://github.com/zebadoba/mountainpi.git
cd mountainpi
```
##### or create one from scratch
```bash
nano docker-compose.yml

-----docker-compose.yml------
version: '3.3'
services:
    rtl-tcp:
        privileged: true
        devices:
            - /dev/ttyAMA0
        container_name: RTL-TCP
        ports:
            - '1234:1234'
        restart: always
        image: 'kosdk/rtl-tcp:latest'

-----end------
Press ctrl +x ,then 'y', then 
enter
```
##### stop
```bash
docker rm -f RTL-TCP
docker-compose down --remove-orphans
```

##### Start/Re-Start
```bash
docker-compose up -d
``` 
# Development by [wisehackermonkey](https://www.github.com/wisehackermonkey) 20210206
### This repository will not be actively maintained

# License
# `MIT Copyright (c) 2021 zebadoba`
