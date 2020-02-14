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

## Building
{{< figure src="img/00_rig_top.JPG" alt=" ... " caption="[ ... ]" >}}

{{< figure src="img/01_rig_bottom.JPG" alt=" ... " caption="[ ... ]" >}}

{{< figure src="img/02_rig_mounted.JPG" alt=" ... " caption="[ ... ]" >}}

{{< figure src="img/03_bread_board.JPG" alt=" ... " caption="[ ... ]" >}}

## Coding

```c++
/*
  Dead Person Switch

  Turns on an LED if both
  buttons are pressed.

  created 2020
  Noah Kernis
*/

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

{{< figure src="img/04_dead_person_switch.gif" alt=" ... " caption="[ ... ]" >}}

