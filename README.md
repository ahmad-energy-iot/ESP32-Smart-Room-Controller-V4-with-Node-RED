# 00-ESP32 Smart Room Controller V4 with Node-Red

---

# Deutsche Version

## Projektbeschreibung

Dieses Projekt demonstriert ein professionelles Smart-Room-Controller-System mit einem ESP32 Mikrocontroller, OLED Display, PIR-Bewegungssensor, LDR-Lichtsensor, RGB-LED sowie MQTT-basierter Fernsteuerung über Computer und Smartphone.

Das System erkennt automatisch die Umgebungshelligkeit sowie Bewegungen im Raum und steuert die RGB-Beleuchtung intelligent und energieeffizient.

Zusätzlich ermöglicht die MQTT-Kommunikation eine vollständige Fernüberwachung und Steuerung des Systems über MQTT Explorer am Computer oder über ein Smartphone-Dashboard.

Das Projekt kombiniert moderne IoT-Technologien, Smart-Home-Automatisierung, Sensorintegration, MQTT-Kommunikation und Embedded-System-Programmierung mit MicroPython.

---

## Hauptfunktionen

- MQTT Remote Dashboard
- Echtzeit-Systemüberwachung
- OLED Echtzeit-Anzeige
- Automatische Lichtsteuerung
- PIR-Bewegungserkennung
- RGB LED Steuerung
- AUTO MODE
- MANUAL ON MODE
- MANUAL OFF MODE
- Smartphone Fernsteuerung
- MQTT Explorer Steuerung
- Energieeffiziente Beleuchtungslogik
- Live Sensorüberwachung
- Smart Home Integration
- IoT-basierte Fernsteuerung
- Node-RED Dashboard Integration
- WLAN-basierte Steuerung

---

## Verwendete Komponenten

| Komponente | Beschreibung |
|---|---|
| ESP32 DevKit V1 | Hauptcontroller des Systems |
| OLED Display SSD1306 | Echtzeit-Systemanzeige |
| PIR Motion Sensor | Bewegungserkennung |
| LDR Sensor | Umgebungshelligkeit messen |
| RGB LED | Status- und Lichtanzeige |
| Breadboard | Schaltungsaufbau |
| Jumper Kabel | Elektrische Verbindungen |
| Widerstände | Schutz der RGB-LED |
| MQTT Explorer | Computerbasierte Steuerung |
| Smartphone Dashboard | Mobile Fernsteuerung |
| Node-RED | Dashboard und Datenvisualisierung |

---

## Pin-Verbindungen

| Komponente | ESP32 Pin |
|---|---|
| RGB Rot | GPIO14 |
| RGB Grün | GPIO26 |
| RGB Blau | GPIO13 |
| PIR Sensor OUT | GPIO27 |
| LDR Sensor AO | GPIO34 |
| OLED SDA | GPIO32 |
| OLED SCL | GPIO33 |

---

## RGB Farbmodi

| Modus | Farbe | Beschreibung |
|---|---|---|
| Helle Umgebung | AUS | Genug Umgebungslicht vorhanden |
| Dunkle Umgebung ohne Bewegung | Blau | Energiesparender Nachtmodus |
| Dunkle Umgebung mit Bewegung | Weiß | Bewegung erkannt |
| MANUAL ON MODE | Grün | Benutzer aktiviert System |
| MANUAL OFF MODE | Rot | Benutzer deaktiviert System |

---

## Betriebsmodi

### AUTO MODE

Das System arbeitet vollständig automatisch:

- Der LDR misst die Umgebungshelligkeit.
- Der PIR-Sensor erkennt Bewegungen.
- Die RGB-Beleuchtung reagiert automatisch abhängig von Licht und Bewegung.

### MANUAL ON MODE

- Die RGB-LED wird manuell aktiviert.
- Die RGB-LED leuchtet dauerhaft grün.
- Sensorwerte werden ignoriert.

### MANUAL OFF MODE

- Das System wird manuell deaktiviert.
- Die RGB-LED leuchtet rot.
- Automatische Funktionen werden deaktiviert.

---

## OLED Display Funktionen

Das OLED Display zeigt in Echtzeit:

- Aktuellen Betriebsmodus
- Lichtwert
- Bewegungsstatus
- RGB Status
- Systeminformationen

Dadurch kann der Benutzer das gesamte System lokal überwachen.

---

## MQTT Dashboard Funktionen

Funktionen des MQTT Dashboards:

- Anzeige aller Live-Daten
- Fernsteuerung aller Betriebsmodi
- Smartphone Fernzugriff
- MQTT Explorer Steuerung
- Benutzerfreundliche Oberfläche
- Echtzeit-Synchronisierung
- Live Sensorwerte
- MQTT Topic Kommunikation
- Node-RED Visualisierung

---

## MQTT Kommunikation

### Publish Topics

- ahmadazroun/esp32v4/light
- ahmadazroun/esp32v4/motion
- ahmadazroun/esp32v4/state
- ahmadazroun/esp32v4/rgb
- ahmadazroun/esp32v4/mode

### Subscribe Topic

- ahmadazroun/esp32v4/control

### Unterstützte Befehle

- AUTO
- ON
- OFF

---

## Systemlogik

1. Das System verbindet sich mit dem WLAN.
2. Der ESP32 verbindet sich mit dem MQTT Broker.
3. Sensorwerte werden permanent überwacht.
4. Das OLED Display aktualisiert Live-Daten.
5. Die RGB-Beleuchtung reagiert abhängig von Licht und Bewegung.
6. Benutzer können das System über MQTT Explorer oder Smartphone steuern.
7. Alle Zustände werden in Echtzeit über MQTT synchronisiert.

---

## Praktische Anwendungen

Dieses Projekt kann in vielen realen Anwendungen eingesetzt werden:

- Smart-Home-Beleuchtungssysteme
- Energieeffiziente Raumsteuerung
- Automatische Nachtbeleuchtung
- IoT-basierte Gebäudeautomatisierung
- Intelligente Smart-Building-Systeme
- Embedded- und IoT-Lernplattformen
- Prototypen für Smart-Energy-Systeme
- Sicherheitsbeleuchtung
- Intelligente Flurbeleuchtung
- Garagenautomatisierung
- Bewegungsgesteuerte Beleuchtung
- Smart-City Anwendungen
- Industrie-Überwachungssysteme

---

## Verwendete Technologien

- ESP32 Microcontroller
- MicroPython
- MQTT Communication
- EMQX Broker
- Embedded Systems
- WiFi Networking
- IoT Systems
- Sensor Integration
- OLED Display Communication
- Smart Home Automation
- Node-RED Dashboard

---

## Benötigte Bibliotheken

- machine
- network
- time
- ssd1306
- umqtt.simple

Zusätzlich müssen folgende Dateien auf den ESP32 hochgeladen werden:

- ssd1306.py
- umqtt/simple.py

---

## Entwickler

### Ahmad Azroun

Renewable Energy Manager | IoT & Smart Energy Systems Developer

---

# English Version

## Project Description

This project demonstrates a professional Smart Room Controller system using an ESP32 microcontroller, OLED display, PIR motion sensor, LDR light sensor, RGB LED, and MQTT-based remote monitoring and control.

The system automatically detects ambient brightness and room motion while intelligently controlling RGB lighting in an energy-efficient way.

Additionally, MQTT communication enables complete remote monitoring and control through MQTT Explorer on a computer or through a smartphone dashboard.

The project combines modern IoT technologies, smart home automation, MQTT communication, sensor integration, and embedded systems programming using MicroPython.

---

## Main Features

- MQTT Remote Dashboard
- Live System Monitoring
- OLED Real-Time Display
- Automatic Lighting Control
- PIR Motion Detection
- RGB LED Control
- AUTO MODE
- MANUAL ON MODE
- MANUAL OFF MODE
- Smartphone Remote Control
- MQTT Explorer Control
- Energy-Efficient Lighting Logic
- Live Sensor Monitoring
- Smart Home Integration
- IoT-Based Remote Access
- Node-RED Dashboard Integration
- WiFi-Based Control

---

## Components Used

| Component | Description |
|---|---|
| ESP32 DevKit V1 | Main system controller |
| OLED Display SSD1306 | Real-time system display |
| PIR Motion Sensor | Motion detection |
| LDR Sensor | Ambient light sensing |
| RGB LED | Lighting and status indication |
| Breadboard | Circuit assembly |
| Jumper Wires | Electrical connections |
| Resistors | RGB LED protection |
| MQTT Explorer | Computer-based control |
| Smartphone Dashboard | Mobile remote control |
| Node-RED | Dashboard and visualization |

---

## Pin Connections

| Component | ESP32 Pin |
|---|---|
| RGB Red | GPIO14 |
| RGB Green | GPIO26 |
| RGB Blue | GPIO13 |
| PIR Sensor OUT | GPIO27 |
| LDR Sensor AO | GPIO34 |
| OLED SDA | GPIO32 |
| OLED SCL | GPIO33 |

---

## RGB Lighting Modes

| Mode | Color | Description |
|---|---|---|
| Bright Environment | OFF | Enough ambient light detected |
| Dark without Motion | Blue | Energy-saving night mode |
| Dark with Motion | White | Motion detected |
| MANUAL ON MODE | Green | User manually activated system |
| MANUAL OFF MODE | Red | User manually disabled system |

---

## Operating Modes

### AUTO MODE

The system operates fully automatically:

- The LDR sensor measures ambient brightness.
- The PIR sensor detects motion.
- The RGB lighting automatically reacts to environmental conditions.

### MANUAL ON MODE

- The RGB LED is manually activated.
- The RGB LED glows green continuously.
- Sensor values are ignored.

### MANUAL OFF MODE

- The system is manually disabled.
- The RGB LED glows red.
- Automatic functions are disabled.

---

## OLED Display Functions

The OLED display shows real-time information:

- Current operating mode
- Light sensor values
- Motion status
- RGB status
- System information

This allows local system monitoring directly from the hardware.

---

## MQTT Dashboard Features

Dashboard features:

- Live system data display
- Full operating mode control
- Smartphone remote access
- MQTT Explorer control
- User-friendly interface
- Real-time synchronization
- Live sensor monitoring
- MQTT topic communication
- Node-RED visualization

---

## MQTT Communication

### Publish Topics

- ahmadazroun/esp32v4/light
- ahmadazroun/esp32v4/motion
- ahmadazroun/esp32v4/state
- ahmadazroun/esp32v4/rgb
- ahmadazroun/esp32v4/mode

### Subscribe Topic

- ahmadazroun/esp32v4/control

### Supported Commands

- AUTO
- ON
- OFF

---

## System Logic

1. The system connects to WiFi.
2. The ESP32 connects to the MQTT broker.
3. Sensor values are continuously monitored.
4. The OLED display updates live information.
5. The RGB lighting reacts automatically based on brightness and motion.
6. Users can remotely control the system through MQTT Explorer or smartphone dashboard.
7. All system states are synchronized in real time using MQTT.

---

## Practical Applications

This project can be used in many real-life applications:

- Smart Home lighting systems
- Energy-efficient room automation
- Automatic night lighting
- IoT-based building automation
- Intelligent smart-building systems
- Embedded and IoT learning platforms
- Smart energy system prototypes
- Security lighting systems
- Intelligent hallway lighting
- Garage automation
- Motion-based lighting systems
- Smart City applications
- Industrial monitoring systems

---

## Technologies Used

- ESP32 Microcontroller
- MicroPython
- MQTT Communication
- EMQX Broker
- Embedded Systems
- WiFi Networking
- IoT Systems
- Sensor Integration
- OLED Display Communication
- Smart Home Automation
- Node-RED Dashboard

---

## Required Libraries

- machine
- network
- time
- ssd1306
- umqtt.simple

Additionally, the following files must be uploaded to the ESP32 board:

- ssd1306.py
- umqtt/simple.py

---

## Developer

### Ahmad Azroun

Renewable Energy Manager | IoT & Smart Energy Systems Developer
