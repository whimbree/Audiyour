# Audiyour

Audiyour is a wireless equalizer and mixer used for converting a wired speaker to a wireless one. The device mixes audio inputs from a line-in 3.5mm jack and Bluetooth. The equalizer can be configured remotely using desktop and mobile applications.

## Hardware
Audiyour is built on the [ESP32-LyraT](https://www.espressif.com/en/products/devkits/esp32-lyrat), an open-source development board from Espressif Systems. Embedded source code is in the [embedded](https://github.com/BSpwr/Audiyour/tree/main/embedded) folder.

### Prerequisites
You must have ESP-ADF and ESP-IDF installed.

https://docs.espressif.com/projects/esp-adf/en/latest/get-started/index.html

### Building
To flash the board, run the following command from within the embedded folder. Replace /dev/ttyUSB0 with the name of the port used.

`idf.py -p /dev/ttyUSB0 fullclean flash monitor`

## Desktop App
![](https://raw.githubusercontent.com/BSpwr/Audiyour/main/control_gui.png)

The Audiyour Control app for desktop is built on the Qt5 toolkit and is written in Python. This cross-platform app allows the user to set the equalizer and mixer gains, or disable them entirely. The Qt Python GUI source code is in the [gui_qt](https://github.com/BSpwr/Audiyour/tree/main/gui_qt) folder.

### Prerequisites
- You must have Qt5 Framework (GUI Toolkit) installed.
    - Ubuntu or Debian
        - sudo apt install qt5-default
    - Arch or Manjaro
        - sudo pacman -S qt5-base
    - Windows
        - https://www.qt.io/download-thank-you?os=windows
- Install Python dependencies using `pip install -r requriements.txt`
  - Optionally, create a fresh venv for installing dependencies into
    - Linux
        - `python3 -m venv venv`
        - `source venv/bin/activate`
    - Windows
        - `python3 -m venv venv`
        - `venv/Scripts/Activate.ps1`

### Running the app
Run `python3 main.py` from the gui_qt folder to launch the application.

## Mobile App
The Audiyour Control app for mobile is built using the Flutter SDK and is written in Dart. The Flutter GUI source code is in the [flutter_app](https://github.com/BSpwr/Audiyour/tree/main/flutter_app) folder.

This interface is currently in active development but not yet complete.
