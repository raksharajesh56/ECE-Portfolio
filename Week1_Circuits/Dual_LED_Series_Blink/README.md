# Project 3: Dual LED Series Blink with Arduino

## Overview
Built a series circuit with 2 LEDs controlled by Arduino Uno. Both LEDs blink simultaneously at the same frequency using a single Arduino pin.

## Circuit Diagrams are attached in the same folder

## Code

```cpp
void setup() {
  pinMode(13, OUTPUT);
  pinMode(11, OUTPUT);  // Set pin 13 as output
}

void loop() {
  digitalWrite(13, HIGH);  // Both LEDs ON
  delay(500);
  digitalWriter(13,LOW);
  delay(500);
  digitalWriter(13,HIGH);
  delay(500);              // Wait 0.5 seconds
  digitalWrite(13, LOW);   // Both LEDs OFF
  delay(500);              // Wait 0.5 seconds
}
```

## What I Learned

- **Series circuits**: Components connected one after another in same current path
- **Current sharing**: Same current flows through all components
- **Voltage division**: Voltage drops across each LED (~2V each)
- **Resistor sizing**: Need higher resistor (470Ω) for multiple LEDs in series
- **Synchronized blinking**: Series LEDs blink together (same timing)
- **Brightness trade-off**: Series LEDs slightly dimmer than individual LEDs (voltage divides)

## Components Used

- Arduino Uno microcontroller
- USB cable (Type-B)
- Breadboard
- 2x 5mm LEDs (any color, can be different colors)
- 1x 470Ω resistor (1/4W) ← KEY: Higher than single LED!
- Jumper wires (red, black)

## Circuit Explanation

**Why Series?**
- Single current path through both LEDs
- Both LEDs get same current → same brightness
- Both receive HIGH/LOW signal at exact same time → synchronized blinking
- Uses only 1 Arduino pin (pin 13)

**Why 470Ω Resistor?**
- Single LED: 220Ω (drops ~2V)
- Two LEDs: 470Ω (drops ~4V total = 2V each)
- Formula: Voltage drop across LEDs ÷ Current = Resistor needed

**Voltage Distribution:**
