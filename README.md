# SmartHumanDetection

SmartHumanDetection is a Software, which detects if a human or a pet is in the Room.

This software is based on RIOT operating system (https://www.riot-os.org/),the main goal of the project is to control the functions of the house by using a microconrollers and sensors.

In order to achieve this we need to work by the IoT network, where the electronics devices (Arduino, Raspberry pi ) are goinig to be connected by wires and communicate by MQTT protocol.

Two main sensors are going to be needed to establish this:

Photodiode-Laser sensor: The principle is to detect any object enters the room, however to distinguish the humans from the pets, a specific hight must be chosen. 
Infrared sensor: This sensor is responsible for detecting the presence of the human, to decide which room to turn the light on (For example).

**The overview of the project:**
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/OverAll%20picture.PNG) 


**Hardware Components:**

***SAM R21 Xplained Pro Evaluation Kit*** 
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/SAM%2BR21%2BXplained%2BPro%2BEvaluation%2BKit%2B5511ec1bc0543.png)

***Nokia 5110 graphic lcd 84_48***
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/nokia_5110_graphic_lcd_84_48-500x500.jpg)

***LED*** 
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/LED5MM.png)

***Raspberry pi***
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/91zSu44%2B34L._SX355_.jpg)

***Laser***
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/NEJE-DK-8-KZ-1000mW-DIY-Laser-Machine-Parts-Laser-Module-High-Power-Violet-Light-Laser.jpg_640x640.jpg)

***PIR Passive-infrared-sensor-motion-sensor*** 
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/hc-sr501-pir-passive-infrared-sensor-motion-sensor-arduino-arelectronics-1709-23-F528300_1.jpg)

***photoesistor***
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/photo-resistor.jpg)

***Resistors***
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/Resistors-Array.jpg)

***Publisher***
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/publisher.PNG)

***Subscriber***
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/d85e56822681ab2eca09a19629c64cf6e5d39c09/SHD_subscriber/Samr21-xpro1.jpg)


**Software setup:**

***Workflow of the Human Detection System***
![alt text](https://github.com/smartuni/SmartHumanDetection/blob/master/imgs/RIOT.png)


**How to setup up the Raspberry-Pi:**

1. You need to install the Lowpan interface and set it up.
    https://github.com/RIOT-Makers/wpan-raspbian/wiki/Create-a-generic-Raspbian-image-with-6LoWPAN-support
2. You need to Install the usefull tools and packeges and configure Systemd lowan
    https://github.com/RIOT-Makers/wpan-raspbian/wiki/Spice-up-Raspbian-for-the-IoT
3. You need set up your Raspberry-Pi as router
    https://github.com/RIOT-Makers/wpan-raspbian/wiki/Setup-native-6LoWPAN-router-using-Raspbian-and-RADVD
4. Setup the mqtt-broker:
    https://github.com/RIOT-OS/RIOT/tree/master/examples/emcute_mqttsn
5. You can now download the parser and unzip it. After you downloaded the parser you should edit the mqttsn.csv, config.csv and
    cayenne.csv. The Mqttsn.csv contains the internal Topic of your System and the channel of the cayenne-cloud. The Cayenne.csv
    contains the channel of the cayenne-cloud and the internal topic. The config.csv contains the account-date for the Cayenne 
    cloud and the information of the broker.
6. Now you can start the parser with **parser Cayenne-Cloud-Password Broker-IP**
  
