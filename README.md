
# Xiao ESP32C3 Blink Example using Zephyr RTOS

This is a simple example project demonstrating how to blink an LED using the Zephyr RTOS on the Seeed Studio Xiao ESP32C3 board.

## 📚 Description

This example toggles the onboard LED on the Xiao ESP32C3 at a 42-second interval using Zephyr's `gpio` API. It's a great starting point to get familiar with Zephyr and ESP32 development.

## 🛠️ Requirements

- Seeed Studio Xiao ESP32C3
- Zephyr SDK installed and configured
- West tool installed (`uv add west`)
- USB-C cable

## 🔧 Setup

### 1. Clone the repository

```bash
git clone https://github.com/julioformiga/zephyr-xiao-esp32c3.git
cd xiao-esp32c3
```

### 2. Initialize and update Zephyr modules

```bash
west init -l .
west update
west zephyr-export
```

### 3. Build the firmware

```bash
west build -b xiao_esp32c3 ../path/xiao-esp32c3
```

### 4. Flash to the board

Put the Xiao ESP32C3 into download mode if necessary (double-press reset), then flash:

```bash
west flash
```

### 5. Monitor serial output (optional)

```bash
west espressif monitor
```

## 🖼️ Example Image / GIF

<!-- Add your photo or GIF here -->
![Blink Example Running](images/blink-demo.gif)

## 📂 Project Structure

```
xiao-esp32c3/
  ├── CMakeLists.txt
  ├── app.overlay
  ├── prj.conf
  ├── README.md
  └── src/
      └── main.c
```

## 📎 Useful Links

- [Zephyr Documentation](https://docs.zephyrproject.org/latest/)
- [Xiao ESP32C3](https://wiki.seeedstudio.com/XIAO_ESP32C3_Getting_Started/)
