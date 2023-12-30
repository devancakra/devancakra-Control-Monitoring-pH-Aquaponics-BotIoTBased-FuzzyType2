[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/Control-Monitoring-pH-Aquaponics-BotIoTBased-FuzzyType2)
![Thesis-Project](https://img.shields.io/badge/Project-Undergraduate%20Thesis%20-%2D%20Informatics%20UPN%20Veteran%20Jatim-light.svg?style=flat&logo=arduino&logoColor=white&color=%23F7DF1E)


# Aquaponic-pH-Control-Monitoring-with-Type-2-Fuzzy-Method-Based-on-IoT-Bot
<strong>Undergraduate Thesis Project Documentation (S1) - Informatics UPN Veteran Jatim</strong><br><br>
This project is closely related to agricultural technology, where this tool is used to control or monitor changes in water pH at any time in the aquaponics area. This aquaponic system itself is a combined cultivation system between fish and vegetables where the activities are mutually beneficial. This tool is equipped with a decision support system in the form of IT2FL with a Bot of Things (BoT) based interface. This tool has been set up in such a way as to be able to work automatically, but it can also be commanded manually.

<br><br>

## Features / Framework / Tools
| Media | Description |
| --- | --- |
| Board Development | DOIT ESP32 DEVKIT V1 & Arduino Uno |
| Code Editor | Arduino IDE |
| Driver | USB-Serial CP210X |
| IoT Platform | io-t.net |
| IoT Protocol | MQTT |
| IoT Architecture | 4 Layer |
| Telegram | Telegram Bot API |
| Matlab |  Fuzzy Interface System |
| Arduino Library | WiFi, PubSubClient, ESPMQTTClient, OneWire, LiquidCrystal I2C, CTBot, & RTClib |
| Actuators | Submersible pump aquarium, Pneumatic solenoid valve, & Piezo buzzer |
| Sensor | pH Sensor & RTC (real time clock) |
| Display | LCD I2C |
| Switch | Switching power supply, Electrical relay 2 channel, & Round switch |
| Other Components | ESP32 baseboard, PCB Dot Matrix, Terminal PCB block screw, Jumper cable, Socket female jack DC, & Connector male jack DC  |

<br><br>

## Download & Install 
1. Arduino IDE

   ```
   https://www.arduino.cc/en/software
   ```
   <br>

2. USB-Serial CP210X

   ```
   https://bit.ly/CP210X_Driver
   ```

<br><br>

## Project Requirements
<table>
<tr>
<th width="280">Pictorial Diagram</th>
<th width="280">Prototype Design</th>
<th width="280">Main Box Design</th>
</tr>
<tr>
<td><img src="https://user-images.githubusercontent.com/54527592/174567843-176f5f16-fbe3-420d-b50b-0aff1d11714e.jpg" alt="Pictorial-Diagram"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174567696-c3737937-dbdd-4608-a6a2-3b9ec0cb81cd.jpg" alt="Prototype-Design"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174568419-f564693e-d35d-4d85-b967-3144d6671bf9.jpg" alt="MainBox-Design"></td>
</tr>
</table>
<table>
<tr>
<th width="280">Fuzzy Interface System IT2FL</th>
<th width="280">IT2FL Input Variable</th>
<th width="280">IT2FL Output Variable</th>
</tr>
<tr>
<td><img src="https://user-images.githubusercontent.com/54527592/174572131-696fcda6-43fb-477b-9579-a0a40d02c1db.jpg" alt="FIS-IT2FL"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174571816-eefdd5de-c0cd-487d-8d68-eea659a313eb.jpg" alt="VarIn-IT2FL"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174571258-5da4e0d1-e788-41a9-9937-1d9c6eaf7ada.jpg" alt="VarOut-IT2FL"></td>
</tr>
</table>

<br><br>

## Arduino IDE Setup
1. Open the ``` Arduino IDE ``` first, then open the project by clicking: ``` File ``` -> ``` Open ``` -> ``` PH_IT2FL.ino ```.<br><br>
   
2. Fill in the ``` Additional Board Manager URLs ``` in Arduino IDE<br><br>
   • Method: click ``` File ``` -> ``` Preferences ``` -> enter the ``` Boards Manager Url ``` by copying the following link:
   
   ```
   https://dl.espressif.com/dl/package_esp32_index.json
   ```
   
3. ``` Board Setup ``` in Arduino IDE<br><br>
   • Method: click ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Install ``` esp32 ```. Then selecting a Board by clicking: ``` Tools ``` -> ``` Board ``` -> ``` ESP32 Arduino ``` -> ``` DOIT ESP32 DEVKIT V1 ```.<br><br>Regarding the Arduino Uno board in this project it is only used as a voltage regulator. So in this section you do not need to configure the Arduino Uno (just focus on the ESP32 only).<br><br>
   
4. ``` Change the Board Speed ``` in Arduino IDE<br><br>
   • Method: click ``` Tools ``` -> ``` Upload Speed ``` -> ``` 115200 ```.<br><br>
   
5. ``` Install Library ``` in Arduino IDE<br><br>
   • Method: download all the library zip files. Then paste it in the: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```.<br><br>

6. ``` Port Setup ``` in Arduino IDE<br><br>
   • Method: click ``` Port ``` -> Choose according to your device port ``` (you can see in device manager) ```.<br><br>

7. Change the ``` WiFi Name ```, ``` WiFi Password ```, and so on according to what you are currently using.<br><br>

8. Before uploading the program please click: ``` Verify ```.<br><br>

9. If there is no error in the program code, then please click: ``` Upload ```.

<br><br>

## Telegram Bot Setup
1. Open <a href="https://t.me/botfather">@BotFather</a>.

2. Type ``` /newbot ```.

3. Type the desired bot name, for example: ``` phiotnet_bot ```.

4. Type the desired bot username, for example: ``` phiotnet_bot ```.

5. Also do it for bot image settings, bot descriptions, and so on according to your needs.

6. Copy ``` your telegram bot API token ``` -> then paste it into the ``` #define BOTtoken "YOUR_API_BOT_TOKEN" ``` section. For example :

   ```
   #define BOTtoken "2130879110:AAEoY1qtnB3xcspCUjCYsUGImysau3N802U" //API bot telegram
   ```
   
7. If it fails to connect to the Telegram Bot, then the problem may be in the firmware. Please check again.

<br><br>

## Get Started
1. Download and extract this repository.<br><br>
   
2. Make sure you have the necessary electronic components.<br><br>
   
3. Make sure your components are designed according to the diagram.<br><br>
   
4. Create an account for the IoT Platform and its services.<br><br>
    
5. If you don't apply points 2 and 3 for project development purposes, that's fine, but be aware that some things need to be changed according to your needs for the system to work properly.<br><br>

6. Make sure all things have been created.<br><br>

7. Please enjoy [Done].

<br><br>

## Demonstration of Application
Via Telegram: <a href="https://t.me/phiotnet_bot">@phiotnet_bot</a>

<br><br>

## Highlights
<table>
<tr>
<th width="280">Product</th>
<th width="280">IT2FL Decision Support System</th>
<th width="280">Telegram Bot</th>
</tr>
<tr>
<td><img src="https://user-images.githubusercontent.com/54527592/174566236-fbcf5d61-bc8e-4daf-ac06-5d396a5c58b8.jpg" alt="Product"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174578231-f2675b70-ebbf-4e9d-84fa-f0c2a7efa167.jpg" alt="IT2FL-SPK"></td>
<td><img src="https://user-images.githubusercontent.com/54527592/174577321-b1da1af7-ce1b-4ec4-9f87-af616ad9f52b.jpg" alt="Telegram-Bot"></td>
</tr>
</table>

<br>
<strong>More information:</strong> <br><br>
<ul>
   • Undergraduate Thesis: <a href="http://repository.upnjatim.ac.id/id/eprint/7014"><u>Click Here</u></a><br><br>
   • SINTA-type journals: <a href="https://publikasi.mercubuana.ac.id/index.php/Incomtech/article/view/15453"><u>Click Here</u></a><br><br>
   • Non SINTA-type journals: <a href="https://www.researchgate.net/publication/363660330_SISTEM_KONTROL_PH_UP-DOWN_BERBASIS_NODEMCU32_DENGAN_METODE_ON-OFF_CONTROLLER"><u>Click Here</u></a>
</ul>

<br><br>

## Disclaimer
This application has been created by including third-party sources. Third parties here are service providers, whose services are in the form of libraries, frameworks, and others. I thank you very much for the service. It has proven to be very helpful and implementable.

<br><br>

## LICENSE
MIT License - Copyright (c) 2020 - Devan C. M. Wijaya, S.Kom

Permission is hereby granted without charge to any person obtaining a copy of this software and the software-related documentation files to deal in them without restriction, including without limitation the right to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons receiving the Software to be furnished therewith on the following terms:

The above copyright notice and this permission notice must accompany all copies or substantial portions of the Software.

IN ANY EVENT, THE AUTHOR OR COPYRIGHT HOLDER HEREIN RETAINS FULL OWNERSHIP RIGHTS. THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, THEREFORE IF ANY DAMAGE, LOSS, OR OTHERWISE ARISES FROM THE USE OR OTHER DEALINGS IN THE SOFTWARE, THE AUTHOR OR COPYRIGHT HOLDER SHALL NOT BE LIABLE, AS THE USE OF THE SOFTWARE IS NOT COMPELLED AT ALL, SO THE RISK IS YOUR OWN.
