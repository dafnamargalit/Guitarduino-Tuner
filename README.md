# Guitarduino-Tuner

<img src="./guitarduino.jpg" data-canonical-src="guitarduino.jpg" width="200" height="200" />

The Guitarduino tuner does what any guitar tuner should do: tells you if your guitar is in tune or not. The guitar is plugged into the tuner through a 1/4 inch audio jack, and the tuner is turned on by a power switch on the side. The display screen then turns on, with the words “Play a note!”. Once a note is played and a frequency is detected, the display screen shows what note is being played and whether it is flat (b), sharp (#), or in tune. 

# How does it work?

<img src="./tuner-schematic-1024x730.png" data-canonical-src="./tuner-schematic-1024x730.png" width="512" height="365"/>

The Guitarduino Tuner uses a TL-082 Op-Amp to amplify and send the frequency signals to the Arduino. Once the Arduino receives the signal, it converts the signal to a frequency value using an [FFT algorithm](https://www.norwegiancreations.com/2017/08/what-is-fft-and-how-can-you-implement-it-on-an-arduino/), and then uses the value of the most dominant frequency to determine what note is being played.

Here is a video of the signal the op-amp is sending the Arduino shown by an oscilloscope:
https://youtu.be/61w8PFVtrfY
