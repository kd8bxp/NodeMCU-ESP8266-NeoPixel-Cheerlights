# NodeMCU (ESP8266) Neopixel Cheerlights

[Project Github Page](https://github.com/kd8bxp/NodeMCU-ESP8266-NeoPixel-Cheerlights).



## Info

Cheerlights is a world wide light show, all controlled by sending tweets to twitter to change the color! People build various projects for the light show. Generally it's around Christmas time, but really Cheerlights spread the cheer all year long.

This is the beginning of a Halloween cheerlight project.
The final project will make spooky noises when the colors change.
And put in either a pumpkin or a skull (not sure yet).
(This could be easy to change to X-Mas music for Christmas holiday.)

In the past I've done projects using the ethernet shield for the Arduino UNO, so I was limited to where the projects could be put.
Not finding a ESP8266 sketch that I could get to work correctly, I set out to make my own. Luckily I found making a few changes to my ethernet sketches, was easy to do.
For more Info on [Cheerlights](http://cheerlights.com).
To see pictures and fritzing, click on pictures above.

I used a Neopixel 16 pixel ring, a nodemcu v.9 board. Arduino IDE 1.6.10 for Linux 64bit, the following libraries are required:

ESP8266WiFi.h - This library gets installed when you add the ESP8266 boards to the Arduino IDE. Information and Setup can be found [here](http://www.esp8266.com/wiki/doku.php?id=start-with-esp-12-arduino).

Adafruit_NeoPixel.h - [Found Here](https://github.com/adafruit/Adafruit_NeoPixel)
 This may or may not be the best library for this project, but it is one that I've used in the past, and I understand how to make it work.

Finally - The TimedAction.h library - [Found Here](http://playground.arduino.cc/Code/TimedAction). Note: I had to make a change to this library to get it to work with the new IDE. That is beyond the scope of this documentation.

##Known Issue:

I am finding that from time to time, (it appears random), the NodeMCU board locks up.  And nothing happens, when this does happen the only thing I can do is unhook it from power, and restart it.

It has something to do with the stack. But it's beyond my knowledge at this time.
So if anyone know how to fix it, please let me know.


##Other Notes:

NodeMCU has limited power on it's 5v line - while it looks like more than one LED is on - truelly only 1 LED is on at a time.
I've also dimmed the brightness down.
I've read that it is capable of driving 6 to 8 of the LEDs at one time, but why risk it.

It should also be noted that the NodeMCU boards pin maps are a bit weird. Pin 2 in the IDE is really D4 on the board.  IF you wanted to use "Pin 2" you'd need to say "D2" in the IDE then it would be maped to pin4 of the esp8266. Google it, there are a number of things about it.

I own a NodeMCU v.9 board, the Fritzing picture shows a NodeMCU v1.0 board, there are some pin differences - v.9 has a 5v pin in place of the VIN pin on the v1.0

