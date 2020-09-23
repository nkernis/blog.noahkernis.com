+++
slug = "04_final_project_you_them_clock_breadboard"
title = "Final Project You Them Clock - Breadboard"
date = "2020-04-03T13:20:10-04:00"
author = "Noah Kernis"
tags = ["itp", "homemade_hardware"]
description = "Making the clock with breakout boards"
showFullContent = false
+++

## Assignment

Create a functional prototype for your final project:

- Use breadboards, pre-made breakout boards, and other things that you did not make yourself
- It should do what you say it should do. This means you'll need software running (if it's not fully analog)  
- Real interaction/experience happening with your prototype.
- Use the actual components/chips/parts that you plan to use for your final. 
	- For example, if you're project uses WiFi, then your prototype should use the same exact WiFi chip that you will use in your final PCB.
- Record a video of the prototype working, and make a blog post of the parts you used to put it together.

## Breadboard

{{< figure src="img/IMG_8950.JPG" alt="Parts on board" caption="[ Parts on Board ]" >}}

{{< figure src="img/IMG_8952.JPG" alt="Using new RTC" caption="[ Using New RTC ]" >}}

## Code

[RELATIVE_CLOCK - Github](https://github.com/nkernis/RELATIVE_CLOCK/tree/pcb_board)

## Functionality

Instead of using the ATtiny84 I had to use the Arduino Nano IoT.

The accelerometer is currently the one that comes with the Arduino Nano IoT.

The RTC breakout is the [Adafruit PCF8523 Real Time Clock Assembled Breakout Board](https://www.adafruit.com/product/3295)

The display is a [0.96 Inch OLED Display Module IIC I2C SSD1306](https://www.amazon.com/gp/product/B07QW95L1B/ref=ppx_yo_dt_b_asin_title_o02_s02?ie=UTF8&psc=1)
