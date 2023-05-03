Download Link: https://assignmentchef.com/product/solved-cs341-lab6-driveway-light
<br>



<strong> </strong>In this lab, you will learn how to use a motion sensor and a light sensor. Using their input you will turn on a light bulb. The starter code can be found on GitHub under Lab 6.

Some Background Info

A photosensitive resistor (PSR) has a resistance value that depends on the amount of light striking its sensor surface.  When you connect a PSR in series with a standard fixed resistor between a voltage source and ground, the amount of current flowing and hence the voltage across the fixed resistor will change with the level of light.  This allows an Arduino program to detect the light level based on an analog input connected to the junction between the PSR and the fixed resistor.

The Parallax Passive Infrared Motion Sensor (PIR) allows an Arduino program to detect motion by returning HIGH when a change in heat occurs and LOW otherwise. If something giving off a lot of heat comes into view (such as a person or car) the sensor should pick it up.

Analog pins (labeled A0 through A5 on the Uno) read an electrical input from 0V to 5V which then gets interpreted as an integer between 0 and 1023 inclusive.

Example usage:

pinMode(A2, INPUT); //we’re going to read from analog pin 2 int examp = analogRead(A2); //reads an input and stores it as an int

Serial.println(examp); //  prints out a value between 0 and 1023

<h2>The Circuit</h2>




CS 341 – Lab 4, Page 1 of 3




<h2>The Logic</h2>

Your light bulb should only turn on when motion is detected, and the light level is below 200. Make use of Serial.println() and the debugger if necessary.




Loop() {   if (motion) {            if (light &lt; 200) {

// light bulb on

}

} else {

//turn the light off if there’s no motion

}

delay(200);

}