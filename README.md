# Homebrew_GPS-WiFi-BT_AUX
![Homebrew compact pcb design](./images/HomeBrew-pcb-design2.jpg)
![Homebrew in a compact box](./images/Homebrew.jpg)
![Homebrew inside the compact box](./images/Homebrew-inside.jpg)

# Pinout for v2.0
![ESP32 Pinout](./images/pinout.png)

#### Added 4K7 pullup resistors on SDA and SCL

### Pin changes

- D4 (ESP Wifi Off) changed to D36
- D5 (ESP Wifi Mode) changed to D39
- D18 (ESP Restore Defaults) changed to D34
- GPS_RX changed to D33
- GPS_TX changed to D25

### I2C pins: SDA (D21), SCL (D22)

### SPI pins: CS (D5), CLK (D18), MISO (D19), MOSI (D23), RST (D13)

# Shared project on OshPark (PCB v2.0)
https://oshpark.com/shared_projects/jyQbF7Wx


## 3D Printing box design
https://www.thingiverse.com/thing:4806408

https://www.tinkercad.com/things/dk77gXFjQE0-homebrewgps-wifi-btaux

## Hardware list
- Amphenol RJ12 socket 54601-906WPLF
- Beitian BN-180 GPS
- 1x 74HC125 (Sometimes called 74HC125N)
- 2x 50kΩ resistor (or 51kΩ)
- 3x 330Ω resistor
- 2x 4,7KΩ (4700Ω) resistor
- 2 diode (any will do, something like 1N5819 or 1N5822)
- Optional: 1x SSD1306 I2C OLED screen (128x64 0.96 inch)

You can find an aliexpress wishlist with the hardware list [here](https://s.click.aliexpress.com/e/_DBdeQVt) (only the RJ12 socket cannot be ordered from Aliexpress)

## PCB ##
You can order the PCB (v2) from oshpark here: [ESP32-Wifi-BT-GPS-v2.0](https://oshpark.com/shared_projects/jyQbF7Wx)
