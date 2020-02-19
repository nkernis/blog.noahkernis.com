+++
slug = "relative-clock"
title = "Relative Clock"
date = "2020-02-03T11:44:06-05:00"
author = "Noah Kernis"
tags = ["itp", "tangible_device"]
description = "Time is always relative... duh."
showFullContent = false
+++

<!-- 
* TODO:
* - Add photos of nano, circuits, and the rest
-->

<!--
* Any construction drawings you made for laser cutting, CNC, etc.
* Circuit diagram/Schematic
* System diagram
-->

## Assignment

For this project I was asked to make a clock with the following requirements: 

	- Make the controls for a desk or bedside clock or timer
		- Your controls should be clear enough that the user can figure out how to set the time without a manual
	- At minimum this should include controls to set the hour and minute
	- Automated time setting is not permitted for this assignment. 
	- You should add at least one extra feature to your clock. 
	- Your clock’s display should be as simple as possible (serial output to a computer, p5.js, LED or LED screen)

## Think

When I first sat down to think about this project the first thought to come to my head was a *relative clock*. I didn't have a specific idea in mind, but I liked the concept of a clock thats shows time relative to something. 

Researching *relative clock* didn't yield much, but I did find [Jonathan Chomko's "Relative Clock"](https://jonathanchomko.com/Relative-Clocks):

> The Relative Clocks are a set of clocks which show how far various spacecraft have travelled in time, relative to earth.

<div style="text-align:center">
	<iframe src="https://player.vimeo.com/video/190896012" class="center" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
</div>
<br/>

I spent some more time thinking about concepts for a *relative clock* but didn't come up with much. It wasn't until I was watching "The Office" later that night that I figured it out. In this episode two of the main characters (Pam and Jim) were discussing how one of them has to travel half the week for work and that it was straining the relationship. I started to think about a way for the characters to have a moment where they remembered each other throughout their respective days. 

I came up with a cube/box looking desk clock. The time is displayed with a small screen. The clock has buttons on the back to set the time. When the clock is is flipped upside-down, the display rotates 180 degrees and shows a different time. The new time is +/- hours relative to the original time. The new time is meant to represent the time of ones work or romantic partner who is in a different time zone. 

Originally I thought of it looking more like a chess clock, but felt both the design and interaction were a little bland.

{{< figure src="img/012.JPG" alt="2 possible design sketches" caption="[ Design Sketches ]" >}}

I ended up designing the clock to look like an hourglass. This design worked well because with real hourglass's, you have to invert them to start the timer. For my clock, to get the alternate time to appear, one also has to invert the clock. The appearance helped to indicate a potential action. 

{{< figure src="img/013.JPG" alt="Final design sketch" caption="[ Hourglass Sketche ]" >}}


## Code

The code was written for the Nano 33 IoT, using the Arduino IDE.

The source code can be found on Github: 
[Relative Clock - Github](https://github.com/nkernis/RELATIVE_CLOCK)

### References

I used the RTC Library for keeping time. I used the Arduino documentation: 
[RTC Library](https://www.arduino.cc/en/Reference/RTC)

For double-clicks I used the OneButton Library. I used the following example code: 
[SimpleOneButton.ino](https://github.com/mathertel/OneButton/blob/master/examples/SimpleOneButton/SimpleOneButton.ino)

I used an OLED 128x64 I2C display. I used the following tutorial to learn how to use the module: 
[OLED I2C Display Arduino Tutorial](https://startingelectronics.org/tutorials/arduino/modules/OLED-128x64-I2C-display/)

The module above uses the Adafruit GFX Graphics Library. I used the following article to learn about the APIs:
[Adafruit GFX Graphics Library](https://learn.adafruit.com/adafruit-gfx-graphics-library/graphics-primitives)

I used the LSM6DS3 Library for the Nano 33 IoT's built-in gyroscope. I used the following example code:
[SimpleAccelerometer.ino](https://github.com/arduino-libraries/Arduino_LSM6DS3/blob/master/examples/SimpleAccelerometer/SimpleAccelerometer.ino)

<!-- 
REFS:
3
* https://github.com/PaulStoffregen/Time 
-->

## Build

## Final Thing

## Thoughts & Concerns

- Physical
- Simple text to remind
- Small moment in day

{{< figure src="img/010.gif" alt="..." caption="[ ... ]" >}}
{{< figure src="img/010.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/020.gif" alt="..." caption="[ ... ]" >}}
{{< figure src="img/020.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/030.gif" alt="..." caption="[ ... ]" >}}
{{< figure src="img/030.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/040.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/050.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/060.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/070.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/080.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/090.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/100.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/110.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/120.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/130.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/140.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/150.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/160.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/170.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/180.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/190.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/200.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/210.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/220.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/230.JPG" alt="..." caption="[ ... ]" >}}
{{< figure src="img/240.JPG" alt="..." caption="[ ... ]" >}}
