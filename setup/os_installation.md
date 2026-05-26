# Arduino IDE Installation

This guide explains how to install the Arduino IDE for programming Arduino boards using the C language.

---

# 📌 What is Arduino IDE?

Arduino IDE is the official software used to:
- Write code
- Compile programs
- Upload code to Arduino boards
- Monitor serial communication

---

# 💻 Supported Operating Systems

Arduino IDE supports:
- Windows
- Linux
- macOS

---

# 🛠 System Requirements

## Minimum Requirements

| Component | Requirement |
|---|---|
| RAM | 4 GB |
| Storage | 500 MB |
| Processor | Dual Core |
| USB Port | Required |

---

# ⬇ Download Arduino IDE

Visit the official Arduino website and download the IDE for your operating system.

### Recommended Version
Arduino IDE 2.x

---

# 🪟 Windows Installation

## Step 1: Download Installer

Download:
```text
Windows Win 10 and newer
```

---

## Step 2: Run Installer

Open the installer and click:
```text
Next → Install
```

---

## Step 3: Install Drivers

Allow USB drivers to install when prompted.

---

## Step 4: Launch Arduino IDE

After installation:
```text
Open Arduino IDE
```

---

# 🐧 Linux Installation

## Ubuntu/Debian

Update packages:

```bash
sudo apt update
```

Install Arduino IDE:

```bash
sudo apt install arduino
```

Launch IDE:

```bash
arduino
```

---

# 🍎 macOS Installation

## Step 1
Download macOS version from Arduino website.

## Step 2
Open `.dmg` file.

## Step 3
Drag Arduino IDE into Applications folder.

---

# 🔌 Connecting Arduino Board

Connect Arduino using a USB cable.

---

# ⚙ Selecting the Board

Go to:

```text
Tools → Board
```

Select:
- Arduino UNO
- Arduino Nano
- Arduino Mega

---

# 🔍 Selecting COM Port

Go to:

```text
Tools → Port
```

Choose the correct port.

---

# 📤 Testing Installation

Upload the Blink Program:

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

If the onboard LED blinks:
✅ Installation Successful

---

# 🧰 Recommended Extensions

Optional tools for advanced development:
- VS Code
- PlatformIO
- Serial Monitor Extensions

---

# 🚀 Next Steps

After installing Arduino IDE:
1. Learn basic C programming
2. Understand Arduino structure
3. Build simple circuits
4. Start sensor interfacing

---

# 📚 Common Errors

| Error | Solution |
|---|---|
| Board not detected | Install drivers |
| COM port missing | Reconnect USB |
| Upload failed | Select correct board |
| Permission denied | Run with administrator rights |

---

# ✅ Conclusion

Arduino IDE provides a beginner-friendly environment for embedded systems programming.

You are now ready to:
- Write Arduino programs
- Upload code
- Build hardware projects
- Learn embedded systems