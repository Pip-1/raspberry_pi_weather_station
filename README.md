## Raspberry Pi weather station

The goal of this project is a very simple raspberry pi weather station. Either it will be accessable from every browser currently logged in
or it will send periodic weather via a Telegram bot.
We will see.

There are endless possibilities of using a Raspberry Pi as a weather station. Feel free to try them all!
## Setup

#### Rasperry Pi
- used or new
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

- get a Raspi, either new or used from ebay-kleinanzeigen, craigslist or similar second hand sites
- i will do a headless setup, meaning i won't have to connect the Pi to any peripherals
- the OS will be put on the SD-card, after that we will put two files on the SD-Card

[Downloading the Raspberry Pi Imager](https://www.raspberrypi.com/software/)
