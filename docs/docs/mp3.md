# NodeMCU (ESP8266) Neopixel Cheerlights

[Project Github Page](https://github.com/kd8bxp/NodeMCU-ESP8266-NeoPixel-Cheerlights).

MP3 version is in directory - 'Cheerlights_ESP8266_Neopixels_v4.1_with_sound'

Why? Because I was testing this and saved it into a different directory with out thinking about it.

It's probably better that way. One sketch with sound, one sketch without.

## Info

I used a cheap MP3 player I found on eBay. Catalex Serial MP3 player. [eBay Link](http://www.ebay.com/itm/UART-Control-Serial-MP3-YX5300-Music-Player-Module-For-New-Arduino-PIC-AVR-ARM-/141929519081?hash=item210ba897e9:g:33AAAOSwIgNXiJ2l)
These players are around $5 or $6 U.S. dollars. Documentation can be a little hard to time, but not impossable. (ask the seller they should have a link to it)

I found 8 or 9 free "Halloween Sound effects" downloaded them and put them on a SD card. 
NOTE: I renamed each file to just numbers (scream.wav - became 01.wav, wolf.wav - became 02.wav, etc.) Not really needed for this to work, but any file name longer then 8 character will need to be renamed.

##Updated Sketch:

The updated sketch, not only added support for the MP3 player, but also changed the API used from thingspeak. 
The new API will return the site headers, plus a RGB number in HEX.
The 1st thing I had to do was to remove the header, but just having the HEX color made the code smaller and able to display any color that was sent.


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

