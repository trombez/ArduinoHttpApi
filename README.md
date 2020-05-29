# ArduinoHttpApi
Simple HttpApi Class for Arduino
It was born for a simple project in combination with https://github.com/trombez/NotificationGateway.

## Envinroment
I used https://platformio.org/ with Visual Studio Code

## Configuration
The library take all the network information from a txt file in the SD Card of the Ethernet Shield, and save in the EEPROM.
If there isn't SD Card, the library load the settings from the EEPROM.
In the Resources folder you can find the SETTINGS.TXT with an example of settings.
The meaning of each row is detailed in the EEPROM file in the same directory.

## Code
ApiClient.Cpp/h : Class with Methods to call an HTTP API with the Ethernet Shield. It's important to observe that the model is for the Notification Gateway project. You have to customize the model for your rest endpoint.

ApiSettings.Cpp/h : Class to read the settings from a File (the format is on the Resources Folder), and save to EEPROM (only if there is file on SD card).

main.cpp : simple program that call the HTTP API when a button is pressed.
