# Homebrew_GPS-WiFi-BT_AUX
![Homebrew compact pcb design](./images/HomeBrew-pcb-design2.jpg)
![Homebrew in a compact box](./images/Homebrew.jpg)
![Homebrew inside the compact box](./images/Homebrew-inside.jpg)

# Pinout for PCB v2.0
![ESP32 Pinout](./images/pinout.png)

Added 4K7 pullup resistors on SDA and SCL

### Pin change compared to V1

- D4 (ESP Wifi Off) changed to D36
- D5 (ESP Wifi Mode) changed to D39
- D18 (ESP Restore Defaults) changed to D34
- GPS_RX changed to D33
- GPS_TX changed to D25
- I2C pins
    - SDA (D21)
    - SCL (D22)
- SPI pins:
    - CS (D5)
    - CLK (D18)
    - MISO (D19)
    - MOSI (D23)
    - RST (D13)

# Shared project on OshPark (PCB v2.0)
https://oshpark.com/shared_projects/jyQbF7Wx

When soldering the PCB, make sure you adjust the voltage of the DC step down after soldering both diode, to make sure that the output after the diode is 5V.


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
- 1 DC sep down module (with pin OUT, GND and IN on the same side, in that order - Often marked +VO, GND and IN+)
- Optional: 1x SSD1306 I2C OLED screen (128x64 0.96 inch)

You can find an aliexpress wishlist with the hardware list [here](https://s.click.aliexpress.com/e/_DBdeQVt) (only the RJ12 socket cannot be ordered from Aliexpress)

## Arduino code
An example source code is available here : [Homebrew_GPS-WiFi-BT_AUX.ino](Homebrew_GPS-WiFi-BT_AUX/Homebrew_GPS-WiFi-BT_AUX.ino) 
You can configure certain part by changing the following parameter

| Parameter  | Function |
| ------------- | ------------- |
| VERBOSE  | Display debug information on serial port, turn off after test  |
| BT_ENABLED  | When false, Bluetooth code is completely left out  |
| ETH_ENABLED  | Always false for this project, only set to true if you want to add ethernet  |
| FORCE_WIFI_ON  | When true, wifi is always on and wifi switch is ignored  |
| FORCE_AP_MODE  | When true, Access Point mode is always on, this allow to connect directly to homebrew via wifi  |
| USE_OLED  | When false, OLED code is completely left out  |
