# LEGO Control System — v2 (proposal)



An open-source, modular system to automate your LEGO city: control switches, traffic lights, and house lights without touching them.

## What this is
LEGO Control System provides simple hardware and software modules to remotely control buttons, servos, and lighting. The goal is a practical, accessible foundation for hobbyists and makers (including people who need extra help building).

## Objectives
- Modular hardware: each module type is small, easy to build, and replaceable.  
- User-friendly control: a simple main-unit interface (TFT + buttons) and optional web/MQTT interface.  
- Accessibility: clear build instructions and examples so less-experienced builders can participate.

## Overview — Main Control Box
- TFT display (status + menu)  
- 20 physical buttons (1 button → 1 module, or multiple buttons per module)  
- Microcontroller: compatible with many boards (e.g., ESP32, Raspberry Pi Pico) — choice flexible per build  
- Power: 5V DC, sufficient current for servos and LEDs  
- Communication: serial, I2C or Wi‑Fi/MQTT (optional)

## Modules (initial set)
- Main module (core): configuration, routing and central communication.  
- Train switch module:
  - Up to 2 servos (step/position control possible)
  - Up to 4 light poles (on/off + dim)
  - Simple connector: 3- or 4-pin connectors for servos and lights
- Light module (later): multiple LED/strip outputs per module

## Hardware specifications (example — adjustable)
- Servo power: separate 5V rail recommended for servos  
- Signal: standard PWM for servos  
- Connectors: JST 3/4-pin or similar for easy assembly  
- PCB footprint: small module size (e.g., 40×25 mm) with screw mounting

## Software overview
- Firmware: modular, updatable per module (example projects for ESP32 available)  
- Communication protocols: simple text API over serial or MQTT topic structure  
- UI: local on TFT + buttons; optional web interface or mobile control via MQTT

## Roadmap (v2)
1. Expand documentation
   - Detailed README (this proposal)
   - Wiring diagrams and connector annotations
2. Design hardware
   - Simple Eagle/KiCad sketches for the train switch module
   - Prototype PCB and 3D enclosure
3. Firmware examples
   - ESP32 example: servo + LED control via MQTT and serial commands
   - Basic calibration routine for switches
4. GUI / Control UI
   - Basic menu on TFT
   - Optional web UI for remote control over Wi‑Fi
5. Tests & releases
   - Hardware test checklist
   - 1.0 release with example build and bill of materials (BOM)
6. Community & accessibility
   - NL/EN documentation
   - Step-by-step guides for builders with limited experience

## How to contribute
- Open issues for bugs, improvements or ideas. Use labels: enhancement, bug, docs.  
- Pull requests: fork → branch → PR. Include a short description and test instructions in the PR.  
- Code style: clear, documented commits; hardware files in /hardware; firmware in /firmware.

## Versioning
- This document is proposal “v2” — feel free to request changes before I commit it.

## License
See LICENSE in the repository — use the same license as the rest of this project.

---
Contact: open an issue or send a message in the repo for questions or requests.
