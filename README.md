# esp32_core
Core ESP32 micropython module

# Startup:
* On startup checks for stored WIFI data.
* If wifi data exists, try to connect to the given data. On success, it will use that connection.
* If there is no stored connection data or connection failed, it will start in AP mode. 

## Wifi AP mode
* print out the connection to the serial or stdout.
* get a list of available wifi networks.
* A simple webserver starts up, which 
** lists the available networks in a list (with some details)
** contains a password field for the selected wifi network
** a button to submit the values and store it in permamently (on NVS?)
After a restart, the device autmatically can connect to the specified network.

## Wifi client mode
* The device has a connection to the wifi network.
* A simple webserver is running, where 
** we can delete the existing configuration (next time it will start up in AP mode).
** we can see the current IP address (configration) of the device (or more details)
** 
