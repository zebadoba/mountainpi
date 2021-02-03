# mountainpi
![slice1](/assets/slice1.png)
#### User documentation for Silke Com for Mountain Top Pi.
Each Mountain Top Raspberry Pi is a V3 Raspberry Pi with an RTL-SDR dognle attached.  The Mountain Top RPi OS build also includes a web based DVR interface with motion detection designed to use inexpensive USB web cameras.  It also includes a web based GPIO (General Purpose Input Output) page for toggleing GPIOs states to +3V or 0V.  The project was lead by the Cat Lord Andy Record, with all devlopment by Oran Collins.

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

# 

# How to connect to web based SDR 

### SDR Software:

* Install basic SDR# software: https://airspy.com/download/  
* Read this tutorial:      https://airspy.com/quickstart/  
* Connect your SDR# application to http://192.168.2.72:1234  
* Remember, only one person can login to a site at any time.  The SDR# software will hang if someone else is connected to the device.

# How to connect to web based camera system  
### Camera System: 

* http://192.168.2.72:8765/
     * admin
     * spainFLOWER96@@

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
* http://192.168.2.72:8000/app/gpio-header
     * ###### username 
     > `silkecom`
     *  ###### password 
     > `&57wavesHUMAN`

* GPIO Info: https://www.raspberrypi.org/documentation/usage/gpio/
* How to drive a relay: https://projects-raspberry.com/raspberry-pi-driving-a-relay-using-gpio/


-----------
# Sys admin guide
## TODO

# License
```bash
MIT Copyright (c) 2021 zebadoba
```