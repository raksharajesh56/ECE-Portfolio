# Project 2: Arduino Single LED Blink

## Overview
Wrote Arduino code to control a single LED using digitalWrite() and delay() functions. LED blinks on and off repeatedly.

## Circuit Diagram
## Code

```cpp
void setup() {
  pinMode(13, OUTPUT);  // Set pin 13 as output
}

void loop() {
  digitalWrite(13, HIGH);  // Turn LED ON
  delay(1000);             // Wait 1 second
  digitalWrite(13, LOW);   // Turn LED OFF
  delay(1000);             // Wait 1 second
}
```

## What I Learned

- **pinMode()**: Configures a pin as input or output
- **digitalWrite()**: Sends HIGH (5V) or LOW (0V) to a pin
- **delay()**: Pauses execution for milliseconds
- **Pin 13**: Has built-in LED on Arduino Uno
- **Loop function**: Code runs repeatedly forever
- **Current limiting**: Resistor protects LED from too much current

## Components Used

- Arduino Uno microcontroller
- USB cable (Type-B) for programming
- Breadboard (optional for external LED)
- 1x 5mm LED (red color)
- 1x 220Ω and 330Ω resistor
- Jumper wires (red, black)

## How It Works

1. **setup()** runs once when Arduino powers on
   - Configures pin 13 as an output pin
   
2. **loop()** runs continuously
   - Sends 5V to pin 13 → LED turns ON
   - Waits 1000ms (1 second)
   - Sends 0V to pin 13 → LED turns OFF
   - Waits 1000ms
   - Repeats forever

## Blink Frequency

Current code: 1 second ON + 1 second OFF = **0.5 Hz blink rate**

To change speed:
- Smaller delay = faster blink
- Larger delay = slower blink

Example: `delay(500)` = 0.5 second = faster blink

## Status

✅ **WORKING!** LED blinks perfectly at 1-second intervals.

## Date Completed

May 15, 2026

## Skills Demonstrated

- Arduino IDE usage
- USB driver installation (FTDI)
- Pin configuration
- Digital output control
- Timing with delay()
- Circuit design with current limiting

## Next Steps (Progressive Difficulty)

1. Change blink speed (modify delay values)
2. Control brightness with PWM (analogWrite instead of digitalWrite)
3. Use potentiometer for variable speed
4. Add second LED (series or parallel)
5. Create traffic light pattern

## Troubleshooting

**LED doesn't light up?**
- Check LED polarity (long leg to power)
- Check resistor connection
- Verify USB connection

**LED very dim?**
- Resistor might be too large
- Try 220Ω or 330Ω instead

**Code won't upload?**
- Check port selection in Tools menu, i initially had trouble with the port section under tools menu.
  later had to install a USB driver (FTDI)
- cross verify with the arduino board for specifiC USB Drives.
- Verify board is "Arduino Uno"
- Try different USB cable (last option)

## References

- Youtube : https://youtu.be/9uHZB7-T_XA?si=xbwStAnOl8JKM14s (Paul McWhorter)
- blogs : to rectify USB installaltion issues

