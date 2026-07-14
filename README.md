# STM32F103 Board Design

## Überblick

Hardware-Referenzdesign und Firmware für ein Entwicklungsboard auf Basis des **STM32F103C8T6** mit CAN, USB, I²C (BME280) und weiterer Peripherie.

Das Repository enthält:

* KiCad-Schaltplan und PCB-Design
* Gerber- und Fertigungsdaten
* Stückliste (BOM)
* STM32CubeIDE Firmware-Projekt
* Tauri Desktop-Anwendung zur Kommunikation mit dem Board

---

## Hardware

### Schaltplan

<p align="center">
  <a href="https://github.com/user-attachments/assets/53ac5396-df05-4695-8c12-381431206e39">
    <img src="https://github.com/user-attachments/assets/53ac5396-df05-4695-8c12-381431206e39"
         alt="STM32F103 Schaltplan"
         width="900">
  </a>
</p>

<p align="center">
  Vollständiger Schaltplan des STM32F103-Boards mit CAN, USB, Spannungsversorgung und BME280-Sensor.
</p>

### 3D-Ansicht der Platine

<p align="center">
  <a href="https://github.com/user-attachments/assets/49a3485b-9462-442f-9252-74b04783f217">
    <img src="https://github.com/user-attachments/assets/49a3485b-9462-442f-9252-74b04783f217"
         alt="3D PCB Rendering"
         width="800">
  </a>
</p>

<p align="center">
  3D-Vorschau der fertig bestückten Leiterplatte aus KiCad.
</p>

---

## Projektstruktur

| Ordner                 | Beschreibung                               |
| ---------------------- | ------------------------------------------ |
| `kicad/`               | Schaltplan, PCB-Layout und Fertigungsdaten |
| `firmware/`            | STM32CubeIDE-Projekt                       |
| `tauri-app/`           | Desktop-Anwendung (Rust + Frontend)        |

---

## Hauptfunktionen

### Mikrocontroller

* `STM32F103C8T6` (LQFP48)

### Kommunikation

* CAN-Bus über `TJA1051`
* USB Micro-B Device Interface

### Sensorik

* `BME280` (I²C)

  * Temperatur
  * Luftdruck
  * Luftfeuchtigkeit

### Spannungsversorgung

* `AMS1117-3.3`
* Onboard 3.3V-Regler

### Debugging & Programmierung

* SWD Header
* ST-Link kompatibel
* STM32CubeProgrammer kompatibel

npm run tauri dev
```
