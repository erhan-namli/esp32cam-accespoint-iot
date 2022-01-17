# IoT-AccesPoint-ESP32CAM
 
![Screenshot](accespointmethod.png)

## Setting Up a Acces Point with WEMOS D1 mini

```C++
#include <Arduino.h>
#include <ESP8266WiFi.h>
#include <Hash.h>
#include <ESPAsyncTCP.h>
#include <ESPAsyncWebServer.h>

const char* ssid     = "ESP8266-Access-Point";   
const char* password = "123456789";

AsyncWebServer server(80);

void setup(){

  Serial.begin(115200);
  
  Serial.print("Setting AP (Access Point)…");
  
  WiFi.softAP(ssid, password);

  IPAddress IP = WiFi.softAPIP();
  Serial.print("AP IP address: ");
  Serial.println(IP);

  // Print ESP8266 Local IP Address
  Serial.println(WiFi.localIP());

  // Start server
  server.begin();
}
 
void loop(){  

}

```

## Connect to Acces Point with ESP32-CAM 

```C++
#include <WiFi.h>

const char* ssid = "ESP8266-Access-Point";
const char* password = "123456789";
// Declaring which Access Point to connect
void setup() {
  
 WiFi.begin(ssid, password); 
}

void loop() {
  delay(1);
}
```

## Camera Live Stream with ESP32-CAM on Access Point

- You can find the codes for ESP32 in the Camera Web Server folder.
- Don't forget to change the SSID and Password according to your project if you want.


