# Problem Statement

To design an electronic pen that stores the text (that is physically written on a surface) automatically in a storage device. This text could be later edited based on our needs. This device should have some sort of correction techniques to rectifiy any mistakes made previously. The size of the device must be reasonably small(diameter< 15 mm). The device should be able to collect data from different types of surfaces.  

Preferable Addition:
A live transfer of data to be viewed/edited via Bluetooth connection to an PC/Mobile application. This reduces the additional developments required to make it possible to do corrections and makes it significantly easier.  

# Different Ideations

## Different sensors

### Using IMU sensor coupled with Pressure Sensors, GPS sensors, ToF sensors

Feasibility: Easily available and dimensions suit the device size.   
Transciever method is tracking the trajectory of the pen and sends the data wirelessly to a smartphone or a PC. This localisation problem can be approached by using trilateration using distance sensors and distance measurement with submillimeter accuracy from two different points with known coordinates from the transciever. This method has considerable disadvantages like high cost, error due to handling of the pen. ToF sensor recieving module also need muliplexers to receive data from different devices.

### CMOS sensor with LED as Source light

Feasibility: Size constraints. Can't detect change if the pen is lifted by few millimeters. Adding an IMU sensor to detect that works.

### IR/Ultrasonic sources of different frequencies and a device to receive the reflected data  

Feasibility: Error prone. Ultrasonic sensors have better accuracy and would work in any surroundings. IR will face some interference from externalities.  

Inktuitive angle: Using Pen as transmitter and seperating receiver is a brilliat idea. It reduces error by some consideration.

### My thought on this:
Replicating the functions of mouse in a pen is very difficult because of the size constraints. If it is feasible, this would be the best method. Implementing IMU sensor is simple, but it required additional components like GPS module. IMU sensors are considerably small too. They are easily available and need not be reconfigured by much. UV/IR waves method is error prone and we will have to add extra components to fix them. However a combination of IMU, CMOS sensor/Optical sensors reduces the possibilities of errors, and enhance the functioning . The medhod implemented in Equil is also very good. We can enhance it for better precision and larger area. 

![image](https://user-images.githubusercontent.com/84671311/121810797-d0bea500-cc7f-11eb-9853-ba03bc152702.png)

## Processors/Controllers used

We can design a PCB of preferable size based on our need and implement necessary ICs, I/Os. This will reduce costs and we can remove unwanted peripherals. Other options include using ESP32/ESP12f/Arduino Nano depending on requirements.

## Implementing Neural Network

This should be a bit difficult to implement. My thoughts are to collect data and implement machine learning algorithms in an external device.

## Market Research  

Dividing existing products based on technology used:

### Using IR or Ultrasonic waves

Equil JOT smart pen:   
A very innovative and cool design. Can work on all papers.  
Livescribe Echo Camera:  
Needs special paper for it to work.  

### Camera based

NEWYES smartpen:
Takes photo of work done and processes it.  

### EMR based
This method is comparatively accurate but requires a reflecting device.  

Wacom Bamboo Tablet:  
Requires Tab for workspace.  

### Required Tablet/ Special paper

Neolab smart pen series  
Wacom Bamboo Tablet  
Moleskin Smart writing set  















