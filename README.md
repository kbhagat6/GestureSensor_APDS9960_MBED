# Gesture Sensor APDS9960 for MBED
APDS-9960 Light, RGB, Proximity, and Gesture Sensor https://www.sparkfun.com/products/12787 

The ~/APDS_9960 folder contains a library strictly for the MBED LPC 1768 microcontroller. It relies on the I2c mbed library. To use the library, instantiate a glibre object, call ginit(), and the appropriate functions. 

The ~/GestureSensor_Test folder contains uses the APDS_9960 Digital Proximity, Ambient Light, RGB and Gesture Sensor library to play detected gesture sounds on a speaker from the SDcard. It also relies on the SDFileSystem and wave_player library
