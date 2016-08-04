# Gesture Sensor APDS 9960 for MBED
APDS-9960 Light, RGB, Proximity, and Gesture Sensor https://www.sparkfun.com/products/12787 


The project is about wirelessly controlling and steering a Magician Robot using a gesture sensor.
* Collision avoidance is implemented using IR sensors. 
* A uLCD and speaker are used to provide the appropriate audio and visual feedback to user on a per-gesture basis.
* Two mbeds - one that is hooked up to the gesture sensor and one that drives the Robot - and two Series 1 XBees to establish a wireless link between the two.

Controller
![](https://github.com/kbhagat6/GestureSensor_APDS9960_MBED/blob/master/g1.PNG?raw=true)
The controller receives the gesture input from user. This command is then sent to the robot using the XBee module. 
The controller also has audio and video feedback, namely an LCD that displays the command being sent to the robot and a voice output.

Magician Robot
![](https://github.com/kbhagat6/GestureSensor_APDS9960_MBED/blob/master/g2.PNG?raw=true)
The robot receives the command sent by the controller and executes it in real time. 
Collision avoidance is implemented using IR sensors. When the sensor returns a value above a certain threshold (0.6 here), the robot sends a message back to the controller saying it detected a collision and waits for a new command.


The ~/APDS_9960 folder contains a library strictly for the MBED LPC 1768 microcontroller. It relies on the I2c mbed library. To use the library, instantiate a glibre object, call ginit(), and the appropriate functions. 

The ~/GestureSensor_Test folder contains uses the APDS_9960 Digital Proximity, Ambient Light, RGB and Gesture Sensor library to play detected gesture sounds on a speaker from the SDcard. It also relies on the SDFileSystem and wave_player library




