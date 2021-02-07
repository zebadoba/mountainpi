# mountainpi
![slice1](/assets/slice1.png)
#### User documentation for Silke Com for Mountain Top Pi.
Each Mountain Top Raspberry Pi is a V3 Raspberry Pi with an RTL-SDR dognle attached.  The Mountain Top RPi OS build also includes a web based DVR interface with motion detection designed to use inexpensive USB web cameras.  It also includes a web based GPIO (General Purpose Input Output) page for toggleing GPIOs states to +5V or 0V.  The project was lead by the 😼Cat Lord Andy Record, with all devlopment by 👨‍💻 Oran Collins,  [wisehackermonkey](https://www.github.com/wisehackermonkey).


# [DOWNLOAD RPI Image here](https://mega.nz/file/kE1nFCqJ#GcHeHwa-VjEAzYPnRlEISpjaMustKIwGJkCFJIEr_1M) valid as of (20210206)
# How to connect to web based SDR 

### SDR Software:
#### Install basic SDR# software: https://airspy.com/download/  
#### Read this tutorial:      https://airspy.com/quickstart/  

![](2021-02-06-15-38-26.png)
------
![](2021-02-06-15-28-22.png)
### Extract and open `SDRSharp.exe`
![](2021-02-06-15-30-11.png)
![](2021-02-06-15-31-34.png)
![](2021-02-06-15-31-53.png)
![](2021-02-06-15-32-15.png)
![](2021-02-06-15-32-52.png)
![](2021-02-06-15-33-12.png)
![](2021-02-06-15-33-33.png)
![](2021-02-06-15-33-51.png)
![](2021-02-06-15-34-09.png)
![](2021-02-06-15-34-18.png)
![](2021-02-06-15-34-43.png)
![](2021-02-06-15-39-49.png)
![](2021-02-06-15-35-19.png)
![](2021-02-06-15-40-37.png)
#### Almost finished!
![](2021-02-06-15-41-36.png)
![](2021-02-06-15-41-57.png)
![](2021-02-06-15-42-17.png)
![](2021-02-06-15-42-42.png)
![](2021-02-06-15-43-17.png)
![](2021-02-06-15-46-46.png)
#### Set host to raspberry pi's ip address XXX.XXX.XXX.XXX for my network its 192.168.1.72
### Ip address = `192.168.1.72`
### Port = `1234`
### Sample rate = `0.25 MSPS`
![](2021-02-06-15-47-48.png)
### Hit play, if everything was setup correctly you should hear radio static!
### Success!
![](2021-02-06-15-59-45.png)

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
![](2021-02-06-15-49-01.png)

     -----------------
<br>
<br>
<br>

# How to connect to web based camera system  
### Camera System (motionEye): 

 ![](2021-02-06-14-19-58.png)
#### IP address + Port number 
#### Note: the  "192.168.2.72' will be different for each network.
<!-- ```bash -->
## http://XXX.XXX.XXX.XXX:8765
<!-- ``` -->
#### Example 
```bash
http://192.168.2.72:8765/

```

![](2021-02-06-14-21-26.png)
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
![](2021-02-06-14-26-01.png)
![](2021-02-06-14-29-36.png)
#### Note: "back up" before you make changes.

### If you set up motion detection, use email with the following SMTP info:
* Email addresses; mike@silkecom.com, Andre@silkecom.com, & others
* SMTP Server: xxxxxx
* SMTP port: xxxxx
* SMTP Account: xxxx
* SMTP Password: XXX
* From Address: site_name.rpicamera@silkecom.com
* Attached Pictures Time Span: “5”

# How to connect to and toggle GPIOs

### Turn GPIOs on and off
![](2021-02-06-16-07-30.png)
![](2021-02-06-16-07-50.png)
### http://192.168.2.72:8000/app/gpio-header
* ###### username 
> `silkecom`
*  ###### password 
> `&57wavesHUMAN`
![](2021-02-06-16-08-13.png)
![](2021-02-06-16-10-09.png)
### `OUT` = gpio pin is `ON`, and `IN` = gpio pin if `OFF`
![](2021-02-06-16-11-52.png)
### Reference
* GPIO Info: https://www.raspberrypi.org/documentation/usage/gpio/
* How to drive a relay: https://projects-raspberry.com/raspberry-pi-driving-a-relay-using-gpio/


-----------
# Sys admin guide

# Set Raspberry pi's Hostname
### login to pi
![](assets/2021-02-02-16-59-38.png)
### run `dietpi-config`
![](assets/2021-02-02-17-03-48.png)
![](assets/2021-02-02-17-04-10.png)
![](assets/2021-02-02-17-04-38.png)
![](assets/2021-02-02-17-04-54.png)
### change the hostname to what you want.
#### to hit 'OK' press `TAB` once then `enter`
![](assets/2021-02-02-17-06-14.png)
 
-----

# Set Raspberry pi's password
### login to pi
![](assets/2021-02-02-16-59-38.png)
### run `dietpi-config`
![](assets/2021-02-02-17-03-48.png)
![](assets/2021-02-02-17-04-10.png)
![](assets/2021-02-02-17-04-38.png)
![](assets/2021-02-02-17-08-25.png)
### enter you password , to hit 'OK' press `TAB` once then `enter` once
![](assets/2021-02-02-17-08-42.png)
 
-----

# How to set IP address
### login to pi
![](assets/2021-02-02-16-59-38.png)
### run `dietpi-config`
![](assets/2021-02-02-17-03-48.png)
![](assets/2021-02-02-17-12-34.png)
![](assets/2021-02-02-17-12-55.png)
![](assets/2021-02-02-17-13-10.png)
### change the ip address
![](assets/2021-02-02-17-13-46.png)
### example:
![](assets/2021-02-02-17-14-32.png)
![](assets/2021-02-02-17-14-55.png)
### Done!
 
-----

# Development by [wisehackermonkey](https://www.github.com/wisehackermonkey)

# License
```bash
MIT Copyright (c) 2021 zebadoba
```