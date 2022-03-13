## Raspberry Pi weather station

The goal of this project is a very simple raspberry pi weather station. Either it will be accessable from every browser currently logged in
or it will send periodic weather via a Telegram bot.
We will see.

There are endless possibilities of using a Raspberry Pi as a weather station. Feel free to try them all!
## Setup

#### Rasperry Pi
- used or new, i.e.: i got all my Pi's from ebay-Kleinanzeigen for a small buck
- i will take a Rasperry Pi Zero W V1.1, but every other Pi will work just as well

#### SD-Card
- the storage unit is needed for the image of the OS the Raspberry Pi will run with
- i got 32 GB, 8 GB will be sufficient enough for most OS, though
- with a script, you could easily store the weather data in various files on the SD-Card as well
- keep in mind, that a high number writing processes will shorten the life span of your card drastically

#### Bosch GY-BME280
- barometric sensor for temperature, humidity and air pressure
- i got one from AZ-Delivery, but there are different manufacturers using the BME280

- there are different sensors you could use for this task, another option could be DHT11 or DHT22

#### Tools and Equipment

#### Soldering Iron
- soldering iron is very useful for the connection of the pins from either the sensor or pi to the pcb's
- i think you can build this without the need of soldering, just need to be a bit creative (hit me up for tips and tricks)
  

## Process

#### Raspberry Pi Setup

- we will do a headless setup, meaning we won't have to connect the Pi to any peripherals other then the power cord
- the OS will be put on the SD-card with the help of the [Raspberry Pi Imager](https://www.raspberrypi.com/software/)
- there is two files in this repository you will need to add, to the SD-cards folder "Boot" (it's just the main folder):
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **wpa_supplicant.conf** - this is a simple text file containing the log-in info to the wifi
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **ssh** - this is a simple and **empty** text file, which activates the SSH-Protocoll, so we can remotely controll the Pi later on
- after the OS is on the card and both files have been added to the folder, we can insert the card it into the Pi, plug it in and let it boot up

**SSH connection**
- there is different ways of checking, if your Pi logged into your network (accessing router via browser)
- let's open the terminal and check for the ping:
''' ping raspberrypi
>>>Ping wird ausgeführt für raspberrypi.fritz.box [2a02:2454:95ac:1600:b95:6f1f:d2dc:9710] mit 32 Bytes Daten:
>>>Antwort von 2a02:2454:95ac:1600:b95:6f1f:d2dc:9710: Zeit=73ms
>>>Antwort von 2a02:2454:95ac:1600:b95:6f1f:d2dc:9710: Zeit=5ms
'''

- perfect, let's connect:
''' ssh pi@raspberrypi
>>> The authenticity of host 'raspberrypi (---)' can't be established.
>>> ECDSA key fingerprint is ---.
>>> Are you sure you want to continue connecting (yes/no/[fingerprint])?
yes
>>> Warning: Permanently added 'raspberrypi,2a02:2454:95ac:1600:b95:6f1f:d2dc:9710' (ECDSA) to the list of known hosts.
>>> pi@raspberrypi's password:
**enter password here** hint: default password of the pi is "raspberry")
- now you should be connected to the terminal of your pi
- to update your pi, which probably won't be necessary, you could get root permission with '''sudo su-'''
- update everything with '''apt-get update'''
- upgrade everything with '''apt-get upgrade'''
- 

