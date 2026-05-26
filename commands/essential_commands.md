# Essential Commands

This guide covers the essential commands and functions used in Arduino programming and embedded C development.

These commands are fundamental for:
- Input and Output Control
- Serial Communication
- Timing
- Analog Operations
- Interrupt Handling

---

# 📌 Arduino Program Structure

Every Arduino program contains two main functions:

```c
void setup() {

}

void loop() {

}
```

---

# ⚙ setup()

The `setup()` function runs only once when the Arduino starts.

### Example

```c
void setup() {
    pinMode(13, OUTPUT);
}
```

### Common Uses
- Initialize pins
- Start serial communication
- Configure modules

---

# 🔄 loop()

The `loop()` function runs continuously forever.

### Example

```c
void loop() {
    digitalWrite(13, HIGH);
}
```

### Common Uses
- Read sensors
- Control outputs
- Execute repeated tasks

---

# 📤 pinMode()

Configures a pin as input or output.

### Syntax

```c
pinMode(pin, mode);
```

### Modes
- `INPUT`
- `OUTPUT`
- `INPUT_PULLUP`

### Example

```c
pinMode(13, OUTPUT);
```

---

# 💡 digitalWrite()

Sets a digital pin HIGH or LOW.

### Syntax

```c
digitalWrite(pin, value);
```

### Values
- `HIGH`
- `LOW`

### Example

```c
digitalWrite(13, HIGH);
```

---

# 🔍 digitalRead()

Reads the state of a digital pin.

### Syntax

```c
digitalRead(pin);
```

### Example

```c
int buttonState = digitalRead(2);
```

---

# 🎚 analogRead()

Reads analog voltage from a pin.

### Syntax

```c
analogRead(pin);
```

### Example

```c
int sensorValue = analogRead(A0);
```

### Output Range
```text
0 → 1023
```

---

# ⚡ analogWrite()

Outputs PWM signal.

### Syntax

```c
analogWrite(pin, value);
```

### PWM Range
```text
0 → 255
```

### Example

```c
analogWrite(9, 128);
```

---

# ⏱ delay()

Pauses the program for a specified time.

### Syntax

```c
delay(milliseconds);
```

### Example

```c
delay(1000);
```

### Output
Pauses for 1 second.

---

# 🕒 millis()

Returns the number of milliseconds since Arduino started.

### Syntax

```c
millis();
```

### Example

```c
unsigned long currentTime = millis();
```

---

# 🖥 Serial.begin()

Starts serial communication.

### Syntax

```c
Serial.begin(baud_rate);
```

### Example

```c
Serial.begin(9600);
```

---

# 📨 Serial.println()

Prints data to Serial Monitor.

### Syntax

```c
Serial.println(data);
```

### Example

```c
Serial.println("Hello Arduino");
```

---

# 📩 Serial.print()

Prints data without a new line.

### Example

```c
Serial.print("Value: ");
```

---

# 🔔 tone()

Generates sound on a buzzer.

### Syntax

```c
tone(pin, frequency);
```

### Example

```c
tone(8, 1000);
```

---

# 🔕 noTone()

Stops sound generation.

### Example

```c
noTone(8);
```

---

# ⚠ attachInterrupt()

Attaches an interrupt to a pin.

### Syntax

```c
attachInterrupt(digitalPinToInterrupt(pin), ISR, mode);
```

### Example

```c
attachInterrupt(digitalPinToInterrupt(2), blink, RISING);
```

---

# 🚨 detachInterrupt()

Disables interrupts.

### Example

```c
detachInterrupt(digitalPinToInterrupt(2));
```

---

# 📚 Complete Blink Example

```c
void setup() {
    pinMode(13, OUTPUT);
}

void loop() {
    digitalWrite(13, HIGH);
    delay(1000);

    digitalWrite(13, LOW);
    delay(1000);
}
```

---

# 📊 Commonly Used Commands

| Command | Purpose |
|---|---|
| setup() | Runs once |
| loop() | Runs repeatedly |
| pinMode() | Configure pin |
| digitalWrite() | Output HIGH/LOW |
| digitalRead() | Read digital input |
| analogRead() | Read analog value |
| analogWrite() | PWM output |
| delay() | Pause execution |
| millis() | Get elapsed time |
| Serial.begin() | Start serial communication |
| Serial.println() | Print data |

---

# 🚀 Recommended Practice

Practice these commands by building:
- LED Blink
- Push Button
- PWM LED Brightness
- Sensor Reading
- Buzzer Alarm

---

# 🧠 Important Notes

✅ Digital Pins:
```text
HIGH or LOW
```

✅ Analog Input:
```text
0 → 1023
```

✅ PWM Output:
```text
0 → 255
```

---

# 📚 Conclusion

These commands form the foundation of Arduino programming and embedded systems development.

Mastering them will help you:
- Control hardware
- Read sensors
- Build automation systems
- Develop embedded applications