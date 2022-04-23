# INTRODUCTION
* Distance calculator of an object in front or by the side of the moving entity is required in large number of devices. These devices may be small or large and can be quite simple or complicated. Distance calculator has important applications in automotive and industrial applications.
* The distance calculator through sensors is useful in detecting obstacles. It is the distance calculator feature that allowed to imagine about self-driving cars and robots. The distance calculator application is also used in industries to check fuel levels in aircrafts and commercial transport vehicles .These uses various kinds of sensors and systems. In this project we have implemented such a measurement system which uses a ultrasonic sensor, arduino and server motor. Ultrasonic means of distance measurement is a convenient method compared to traditional one using measurement scales. Ultrasonic sound waves are useful both the air and underwater. Ultrasonic sensors are versatile for the distance measurement and it is quite fast for the common application. The transmitted waves are reflected back from the object and received by the sensor again.
* This provide for cheapest solution. Any distance calculator application has a sensor circuit and an actuator or display circuit (to perform path change according to the obstacle detection or display the distance reading respectively). In this project we have used RF module to control the robot to demonstrate the project. The limitation of this system is it can detect the range between 2m-4m. 

# SWOT ANALYSIS

#### STRENGTH:

 -> Not affected by color or transparency of objects Ultrasonic sensors reflect sound off of objects, so the color or transparency have no effect on the sensor’s reading.
 
 -> Can be used in dark environments Unlike proximity sensors using light or cameras, dark environments have no effect on an ultrasonic sensor’s detection ability.

 -> Low-cost option .They come fully calibrated and ready to use. We strive to give a low cost, high-quality product suited for specific needs.

 -> They have greater accuracy than many other methods at measuring thickness and distance to a parallel surface
 
 #### WEAKNESS:
  -> Cannot work in a vacuum Because ultrasonic sensors operate using sound, they are completely nonfunctional in a vacuum as there is no air for the sound to travel through.
  
  -> Not designed for underwater use.
  
  -> Sensing accuracy affected by soft materials Objects covered in a very soft fabric absorb more sound waves making it hard for the sensor to see the target.
  
  -> Have a limited detection range .At the moment, the longest range sensors have a maximum range of 10 meters, now our cargo sensor detects up to 16.5m.

#### OPPORTUNITIES:

 -> They are used within food and beverage to measure liquid level in bottles, they can be used within manufacturing for an automated process and control maximising efficiency on the factory floor.
 
 -> Their high frequency, sensitivity, and penetrating power make it easy to detect external or deep objects.
 
 #### THREATS:
 -> If we are using in foggy conditions Then the values might be change.
 
 -> if there any inteernal malfunction occur it may show wrong values.
 
 
 # 4W’s &IH
 
 #### WHO:
 This device can be used in vechiles and aircrafts To determine surrounding objects.
 
 #### WHAT:
 This device is used for measuring exact distance from the object.
 
 #### WHEN:
 This device is used during night time in travelling.
 
 #### WHERE:
 It is mandatory to all vehicles and used in medical purpose and military purpose.

# HIGH LEVEL REQUIREMENTS
 ![image](https://user-images.githubusercontent.com/80596756/164877751-3c319402-519f-4633-9026-8aada8c72aaa.png)

 
# LOW LEVEL REQUIREMENTS
 ATMEGA328
 
Power supply (5v)

Hd44780 (16x2LCD) 

1000uF capacitor

10KΩ resistor (2 pieces) 

HC-SR04 sensor.
