# MiniGames by hack_updt

A collection of classic arcade games optimized for ESP32 with an OLED display, offering a compact and portable gaming experience.

---

## About

**MiniGames by hack_updt** transforms your ESP32 into a retro handheld gaming console. This project features a menu system to select and play various classic arcade games on a small OLED screen, complete with high score saving.

---

## Features

- **Multiple Games**: Play a variety of classic games.  
- **High Score System**: Saves high scores for each game using EEPROM.  
- **Intuitive Menu**: Easy navigation between games.  
- **Compact Design**: Optimized for small OLED displays (128x64 pixels).  
- **Responsive Controls**: Utilizes physical buttons for a true gaming experience.  

---

## Games Included

- **SNAKE**: Navigate a snake to eat food and grow, avoiding walls and its own tail.  
- **TETRIS**: Arrange falling blocks to clear lines.  
- **FLAPPY BIRD**: Tap to make a bird fly through gaps in pipes.  
- **2048** : Merge tiles to reach the 2048 tile.  
- **BREAKOUT**: Control a paddle to bounce a ball and break bricks.  
- **FROGGER**: Guide a frog across a busy road and dangerous river.  
- **HELICOPTER**: Fly a helicopter through a continuously scrolling cave.  
- **PAC-MAN** : Navigate a maze, eat dots, and avoid ghosts.  

---

## Hardware Requirements

To build your **MiniGames ESP32 Gameboy**, you'll need:

- **ESP32 Development Board** (e.g., ESP32 DevKitC)  
- **OLED Display**: 128x64 SSD1306 OLED (I2C interface)  
  - `PIN_SCL`: GPIO 22  
  - `PIN_SDA`: GPIO 21  
- **Buttons**: 4 momentary push buttons  
  - `PIN_BUTTON_UP`: GPIO 4  
  - `PIN_BUTTON_DOWN`: GPIO 5  
  - `PIN_BUTTON_LEFT`: GPIO 15  
  - `PIN_BUTTON_RIGHT`: GPIO 18  
- **Breadboard & Jumper Wires**  
- **Power Supply**: Micro-USB or 5V external

---

## Software Requirements

- **Arduino IDE** or PlatformIO  
- **ESP32 Board Package**  
- **Libraries**:  
  - Adafruit GFX Library  
  - Adafruit SSD1306 Library  
  - `Wire.h` *(built-in)*  
  - `EEPROM.h` *(built-in)*  
  - `Ethnocentric_Rg_It5pt7b.h` *(Custom font, include in your project)*  

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/hack_updt/MiniGames.git
cd MiniGames

````

### 2. Install ESP32 Board Package

* Open Arduino IDE
* Go to **File > Preferences**
* In *"Additional Boards Manager URLs"*, add:

  ```
  https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
  ```
* Go to **Tools > Board > Boards Manager...**
* Search and install: **esp32 by Espressif Systems**

### 3. Install Required Libraries

* Go to **Sketch > Include Library > Manage Libraries...**
* Search and install:

  * Adafruit GFX
  * Adafruit SSD1306
* Ensure `Wire.h` and `EEPROM.h` are available (usually pre-installed)
* Add `Ethnocentric_Rg_It5pt7b.h` to your sketch folder

### 4. Connect Your Hardware

Wire up the ESP32, OLED display, and buttons based on the pin configuration in `config.h`.

### 5. Upload Code

* Open `MiniGames.ino` in Arduino IDE
* Select the board: **ESP32 Dev Module**
* Select the correct port under **Tools > Port**
* Click **Upload**

---

## ▶️ Usage

Once uploaded, the ESP32 will boot into the main menu.

### 📜 Menu Navigation:

* **UP/DOWN**: Scroll through game list
* **RIGHT**: Start the selected game

### 🕹 In-Game Controls:

* Controls vary by game but generally use:

  * **UP/DOWN/LEFT/RIGHT** for movement
* **Game Over/Won screen**:

  * **UP**: Return to menu
  * **RIGHT**: Restart game

---

## 🛠 Customization

* **`config.h`**: Customize pin assignments, game constants, screen size, etc.
* **Game Code (`.cpp`/`.h`)**: Adjust logic, speed, or add new games.
* **`display.cpp` / `input.cpp`**: Modify how the screen and buttons are handled.

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 🙏 Acknowledgments

* **Adafruit** for their GFX and SSD1306 libraries
* The **ESP32 community** for tools, code, and guidance
* Inspired by classic arcade games that brought joy to generations

```

