+++
slug = "00_dead_person_switch"
title = "Dead Person Switch"
date = "2020-02-14T12:58:54-05:00"
author = "Noah Kernis"
tags = ["itp", "homemade_hardware"]
description = "Learning to Program an ATtiny85"
showFullContent = false
+++

## About The Piece

For this assignment, we were asked to 1. make an ATtiny85 programming jig, 2. create an interaction/project with the ATtiny85, along with any sensor and/or output you choose.

I decided to make a simple "Dead Person's Switch" ([dead man's switch](https://en.wikipedia.org/wiki/Dead_man%27s_switch)). Two momentary push buttons need to be pressed at the same time in order for an LED to turn on.

## Building

#### Programming Jig

Following the instructions provided to us ([programming an ATtiny85](http://www.homemadehardware.com/guides/programming-an-attiny85/#jig)), I created the programming jig. The jig is intedned to be used by pluggiing it into an Arduino UNO. The Arduino UNO acts as a programmer for the ATtiny85.

{{< figure src="img/00_rig_top.JPG" alt="Top view of programming jig." caption="[ Programming Jig - Top ]" >}}

{{< figure src="img/01_rig_bottom.JPG" alt="Bottom view of programming jig." caption="[ Programming Jig - Bottom ]" >}}

{{< figure src="img/02_rig_mounted.JPG" alt="Programming jig mounted on Aruino UNO" caption="[ Programming Jig - Mounted on Arduino ]" >}}

#### Breadboard

{{< figure src="img/03_bread_board.JPG" alt="ATtiny85 on breadboard with LED and two push buttons." caption="[ Dead Person's Switch ]" >}}

## Code

The code on the ATtiny85.

```c++
const int leftButtonPin = 3;
const int rightButtonPin = 4;
const int ledPin = 1;

int leftButtonState = 0;
int rightButtonState = 0;

void setup() {
  pinMode(leftButtonPin, INPUT);
  pinMode(rightButtonPin, INPUT);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  leftButtonState = digitalRead(leftButtonPin);
  rightButtonState = digitalRead(rightButtonPin);

  if (leftButtonState == HIGH && rightButtonState == HIGH) {
    digitalWrite(ledPin, HIGH);
  } else {
    digitalWrite(ledPin, LOW);
  }
}
```

## The Final Thing

{{< figure src="img/04_dead_person_switch.gif" alt="Using the Dead Person's Switch to turn on an LED" caption="[ Using the Dead Person's Switch ]" >}}
