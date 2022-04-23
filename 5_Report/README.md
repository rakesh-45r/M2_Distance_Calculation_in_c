# Abstract:
The project is designed to develop distance measurement system using ultrasonic waves and interfaced with arduino. We know that 
human audible range is 20hz to 20khz.We can utilize these frequency range waves through ultrasonic sensor HC-SR04.The advantages of this sensor when interfaced with arduino which is a control and sensing system, a pro per distance measurement can be made with new techniques. As large amounts are spent for hundreds of inflexible circuit boards, the arduino will allow business to bring many more unique devices. This distance measurement system can be widely used as range meters and as proximity detectors in industries. The hardware part of ultrasonic sensor is interfaced with arduino. This method of measurement is efficient way to measure small distances precisely. The distance of an obstacle from the sensor is measured through ultrasonic sensor. After knowing the speed of sound the distance can be calculated.

# INTRODUCTION
Today’s the developing world shows various adventures in every field. In each field the small requirements are very essential to develop big calculations. By using different sources we can modify it as our requirements and implement in various field. In earlier days the measurements are generally occur through measuring devices. But now a day’s digitalization as is on height. Therefore we use a proper display unit for measurement of distance. We can use sources such as sound waves which are known as ultrasonic waves using ultrasonic sensors and convert this sound wave for the measurement of various units such as distance, speed. This technique of distance measurement using ultrasonic in air includes continuous pulse echo method, a burst of pulse is sent for transmission medium and is reflected by an object kept at specific distance. The time taken for the sound wave to propogate from transmitter to receiver is proportional to the distance of the object. In this distance measurement system we had ultrasonic sensor HC-SR04 interfaced with arduino UnoR3. Programming and hardware part of ultrasonic sensor interfacing with arduino UnoR3. 

# Components Required
* Hardware: ATMEGA32, Power supply (5v), AVR-ISP PROGRAMMER, JHD_162ALCD (16x2LCD), 1000uF capacitor, 10KΩ resistor (2 pieces) , HC-SR04 sensor.

* Software: Atmel studio 7.0, progisp or flash magic.

# Circuit Diagram and Working Explanation
![circuit diagram](https://user-images.githubusercontent.com/91746229/164944385-ee593df1-03b1-4e82-9a39-be323641a1a4.jpg)
* Here we are using PORTB to connect to LCD data port (D0-D7). Anyone who does not want to work with FUSE BITS of ATMEGA32A can not use PORTC, as PORTC contains a special type of communication which can only disabled by changing FUSEBITS.

* In the circuit, you observe I have only took two control pins, this give the flexibility of better understanding. The contrast bit and READ/WRITE are not often used so they can be shorted to ground. This puts LCD in highest contrast and read mode. We just need to control ENABLE and RS pins to send characters and data accordingly.
-> This circuit is developed by interfacing ultrasonic sensor“HC-SR04” with AVR microcontroller. This sensor uses a technique called “ECHO” which is something you get when sound reflects back after striking with a surface.

-> We know that sound vibrations can not penetrate through solids. So what happens is, when a source of sound generates vibrations they travel through air at a speed of 220 meters per second. These vibrations when they meet our ear we describe them as sound. As said earlier these vibrations can not go through solid, so when they strike with a surface like wall, they are reflected back at the same speed to the source, which is called echo.

-> Ultrasonic sensor “HC-SR04” provides an output signal proportional to distance based on the echo. The sensor here generates a sound vibration in ultrasonic range upon giving a trigger, after that it waits for the sound vibration to return. Now based on the parameters, sound speed (220m/s) and time taken for the echo to reach the source, it provides output pulse proportional to distance.

![timing diagram](https://user-images.githubusercontent.com/80596756/164614761-b8127788-cdb2-459a-b95e-d5336896ba63.PNG)

As shown in figure, at first we need to initiate the sensor for measuring distance, that is a HIGH logic signal at trigger pin of sensor for more than 10uS, after that a sound vibration is sent by sensor, after a echo, the sensor provides a signal at the output pin whose width is proportional to distance between source and obstacle.

-> This distance is calculate as, distance (in cm) = width of pulse output (in uS) / 58.

-> Here the width of the signal must be taken in multiple of uS(micro second or 10^-6).

# CONNECTIONS

-> Here we are using PORTB to connect to LCD data port (D0-D7). Anyone who does not want to work with FUSE BITS of ATMEGA328 can not use PORTC, as PORTC contains a special type of communication which can only disabled by changing FUSEBITS.

-> In the circuit, you observe I have only took two control pins, this give the flexibility of better understanding. The contrast bit and READ/WRITE are not often used so they can be shorted to ground. This puts LCD in highest contrast and read mode. We just need to control ENABLE and RS pins to send characters and data accordingly.

The connections which are done for LCD are given below:

PIN1 or VSS to ground

PIN2 or VDD or VCC to +5v power

PIN3 or VEE to ground (gives maximum contrast best for a beginner)

PIN4 or RS (Register Selection) to PD6 of uC

PIN5 or RW (Read/Write) to ground (puts LCD in read mode eases the communication for user)

PIN6 or E (Enable) to PD5 of uC

PIN7 or D0 to PB0 of uC

PIN8 or D1 to PB1 of uC

PIN9 or D2 to PB2 of uC

PIN10 or D3 to PB3 of uC

PIN11 or D4 to PB4 of uC

PIN12 or D5 to PB5 of uC

PIN13 or D6 to PB6 of uC

PIN14 or D7 to PB7 of uC

In the circuit you can see we have used 8bit communication (D0-D7) however this is not a compulsory and we can use 4bit communication (D4-D7) but with 4 bit communication program becomes a bit complex. So as shown in the above table we are connecting 10 pins of LCD to controller in which 8 pins are data pins and 2 pins for control.

The ultrasonic sensor is a four pin device, PIN1- VCC or +5V; PIN2-TRIGGER; PIN3- ECHO; PIN4- GROUND. Trigger pin is where we give trigger to tell the sensor to measure the distance. Echo is output pin where we get the distance in the form of width of pulse. The echo pin here is connected to controller as an external interrupt source. So to get the width of the signal output, the echo pin of sensor is connected to INT0 (interrupt 0) or PD2.
