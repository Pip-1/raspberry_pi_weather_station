## Raspberry Pi weather station

This is a little private side project.
Goal very simple raspberry pi weather station which can be accessed either through a URL, setup via Node-red, while connected to the Wifi.
Other possibility is a telegram bot which messages you with current meassurements.

There are endless possibilities of using a Raspberry Pi as a weather station. I will use Python

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

- soldering iron is very useful for the connection of the pins from either the sensor or pi to the pcb's
- i think you can build this without the need of soldering, just need to be a bit creative (hit me up for tips and tricks)


## Process

#### Raspberry Pi Setup

- get a Raspi, either new or used from ebay-kleinanzeigen, craigslist or similar second hand sites
- 
