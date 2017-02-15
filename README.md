# Density Based Traffic Light Control System
# Objectives:
1.	To control the traffic lights based on the density of the vehicles to reduce traffic congestion.
2.	To develop coding and to implement it in hardware of density based traffic light control system using arduino.

# Introduction:
Due to the heavy traffic in the road many people are suffering. Even though there is traffic signal available at various places it is not easy to control the crowd. In order to avoid traffic problem heavily on the road, we designed and developed a system so called as density based traffic light control system.


![dense traffic](https://cloud.githubusercontent.com/assets/11133613/22974675/a4727666-f3ad-11e6-9e88-dfadb14f9fc4.png) 
![image](https://cloud.githubusercontent.com/assets/11133613/22974709/d29f9a50-f3ad-11e6-94af-284e2e6ee80e.png)

# Circuit Diagram:

![image](https://cloud.githubusercontent.com/assets/11133613/22974772/12c7e682-f3ae-11e6-929e-7c630887e04a.png)

Figure 1: Circuit Diagram of Density Based Traffic Light Control System

# Components:
![screenshot003](https://cloud.githubusercontent.com/assets/11133613/22974977/11540424-f3af-11e6-87b5-bda6243fd1d4.jpg)

# Arduino:
The Arduino Uno is a microcontroller board based on the ATmega328 (datasheet). It has 14 digital input/output pins (of which 6 can be used as PWM outputs), 6 analog inputs, a 16 MHz ceramic resonator, a USB connection, a power jack, an ICSP header, and a reset button. It contains everything needed to support the microcontroller; simply connect it to a computer with a USB cable or power it with a AC-to-DC adapter or battery to get started. 
The Uno differs from all preceding boards in that it does not use the FTDI USB-to-serial driver chip. Instead, it features the Atmega16U2 (Atmega8U2 up to version R2) programmed as a USB-to-serial converter.
"Uno" means one in Italian and is named to mark the upcoming release of Arduino 1.0. The Uno and version 1.0 will be the reference versions of Arduino, moving forward. The Uno is the latest in a series of USB Arduino boards.

![image](https://cloud.githubusercontent.com/assets/11133613/22975113/9db17c58-f3af-11e6-8a0e-55e01269da34.png)
Figure 2:  Arduino Uno R3 Front

# LED:
LED stands for light emitting diode. It’s  operating voltage is around 3-4V. In our project LED is used as traffic light, so we have used red, green and yellow LED.

![image](https://cloud.githubusercontent.com/assets/11133613/22975140/bdc25436-f3af-11e6-8ae0-eae12f9302e9.png)
Figure 3: Red, Yellow and Green LED

# IR Transmitter:
	Symbol and operation of IR transmitter is very similar to ordinary LED
	IR transmitter generates infrared. IR transmitter is made up of Gallium arsenide. 
	If we pass the current to gallium arsenide it produces IR rays.
	Current applied to the sensor is directly proportional to the rays emitted 
	Though IR transmitter can withstand up to 35mA, we have used 5mA due to shortest distance. If the distance is more we have to increase the current flow to the transmitter .


# IR Receiver:
	This circuit is mainly used to for counting application
	Since IR can be used only during proper alignment position
	IR receiver is having reverse characteristics of the IR transmitter
	IR Receiver will conduct as long as the rays falls on it.
	When a car passes between the IR transmitter and IR receiver, the IR light is blocked and as the result the resistance of the photodiode increases. This change in resistance can be converted to electrical pulses, used to control the traffic lights.
	The schematic in the boe bot manual recommends a 1k resistor for the IR led. We chose to use a 330 ohm resistor. With a 330 ohm resistor, this sensor can detect the hand up to about 30cm(1 foot) away. If we use a higher value resistor, then the sensor has less range.

![image](https://cloud.githubusercontent.com/assets/11133613/22975173/ddbdc9b4-f3af-11e6-8d9b-481733fe169f.png)
Figure 4: IR Transmitter and Receiver

# Circuit Operation:
         It operates in two modes : normal mode & density mode.

NORMAL MODE:
         In this mode of operation green , yellow and red  lights change after a fixed time period like a typical traffic signal. Here ,light from  IR transmitter LED  reach IR receiver without any interruption.
         IR sensor senses amount of cars passing through the road .By using Arduino , we can observe the voltage of IR sensor. When light from IR transmitter does not interrupted by vehicles ,value of voltage is low (about 800) .When voltage value is below 800,this mode is operated .


DENSITY MODE:
When amount of cars increases ,light of IR transmitter intersect by cars  to reach the receiver .Then the voltage of IR sensor increases (about above 850) .When voltage is below threshold value , normal mode is on; but above threshold values then the red signal becomes automatically green.

# Flow Chart

![screenshot004](https://cloud.githubusercontent.com/assets/11133613/22975264/51835242-f3b0-11e6-8a07-a23e3723b4fa.jpg)

# Advantages:
	Avoids wastage of time due to the traffic 
	Fully automatic
	Low power consumption
	It provides the easy access in the traffic light
	Low cost to design the circuit, maintenance of the circuit is good
	By using this Arduino Uno we can create many more control to the appliances
	Easy convenience to handle.

# Limitations:
	IR sensors sometimes may absorb normal light also. As a result, traffic system works in improper way.
	IR sensors work only for fewer distances.
	We have to arrange IR sensors in accurate manner otherwise they may not detect the traffic density.

# APPLICATIONS:
	The project is mainly used in the traffic signals in metropolitan cities to provide uniform distribution of traffic.

# Conclusion:
The project may be very well used in where the traffic signals is kept and in many other places where we need to full fill the need of the automation. In this project we have studied the optimization of traffic light controller in a City using IR sensors and Arduino . Figure-4. shows the complete circuit diagram of Arduino board. By using this system configuration we tries to reduce the possibilities of traffic jams, caused by traffic lights, to an extent and we have successfully gets the results.


# Future Work:

	We will implement this system for  traffic controlling in a 4 lane junction.
	We will update this system with when a pedestrian try to cross the road during green signal it will turn on an alarm and warn the pedestrian and traffic police.
	We will update this system with when a vehicle try to move even during red signal it will turn on an alarm to warn the driver of the vehicle and the traffic




