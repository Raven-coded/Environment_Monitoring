# **Environment monitoring**

This Project utilizes the **`ESP32` microcontroller** and a **`DHT11` sensor** to display the temperature and humidity readings of an area, and represent the same in a graphical format on the ***Blynk*** mobile app. This IOT device can be placed anywhere with a WIFI connection.



## Features :

- Displays current temperature readings of an area.
- Displays current humidity reading of an area.
- Graphical representation of both the readings.
- Simple and understandable interface.  
- Can be setup in any place with a Power supply and WIFI connectivity. 



## Components Used :

- Esp32 AI thinker (Esp32 CAM).
- DHT11 temperature and humidity sensor.
- USB to TTL programmer (ch340g).
- Jumpers.
- *Blynk* App installed on a mobile device.



## Libraries Used :

- **`WiFi.h`** :This library provides ESP32 specific WIFI methods we are calling to connect to network.
- **`WiFiClient.h`** :Creates a client that can connect to to a specified internet IP address and port as defined in client.
- **`DHT.h`**  :This library is provided by Adafruit and helps to read temperature and humidity which is received from the *DHT11* sensor. To install the library, navigate to the **Sketch > Include Library > Manage Libraries** . Once it opens, search for `DHT sensor`. There should be a couple entries. Look for *DHT sensor library* `by Adafruit`. Click on that entry, and then select Install. The DHT sensor library uses the Adafruit Sensor support backend. So, search the library manager for `Adafruit Unified Sensor` and install that too.
- **`BlynkSimpleEsp32.h`** :This comes inbuilt with the **`Blynk` library** and enables us to establish a connection with the ***Blynk*** servers through our **`ESP device.`**



## Getting Started :

1. Install the above mentioned libraries.(DHT library, Adafruit Unified Sensor and Blynk libraries )
2. Enter your WIFI details in the **`ssid`** and **`password`** variables.
3. Generate the ***Auth Token*** through the *Blynk* App and enter it in the **`auth`** variable.
4. Upload the code to the microcontroller after verifying and checking the connections.



## Hardware Connections :

### *Connections 1:*

| <u>**DHT11 Sensor Pin **</u> | <u>**ESP32-CAM Pin**</u> |
| :--------------------------: | :----------------------: |
|             VCC              |           3.3V           |
|             DATA             |         GPIO 13          |
|             GND              |           GND            |

------

### *Connections 2:*

| **<u>CH340G Pin</u>** | <u>ESP32-CAM Pin</u> |
| :-------------------: | :------------------: |
|          5V           |          5V          |
|          TXD          |    GPIO 3 (U0RXD)    |
|          RXD          |    GPIO 1 (U0TXD)    |
|          GND          |         GND          |



## Working :

After uploading the code to **ESP32**, open ***Serial Monitor*** by pressing `ctrl+shift+I` and set the baud rate to `115200`. Next press the **RST** button on ESP board. If your credentials entered in the variables are correct, a connection will be established to the *Blynk* server and a message will be displayed regarding the same. Finally on the device where Blynk is installed, the reading will be fed wirelessly and updated real-time.



## Images :

A few images of a Properly configured Blynk App :-



<img src="Images\pic1.jpeg" style="zoom:80%;" />

[^Live Reading]: 

<img src="Images\pic2.jpeg" style="zoom:80%;" />

[^Cumulative Reading of an Hour]: 



<img src="Images\pic3.jpeg" style="zoom:80%;" />

[^Expanded Graph View]: 

