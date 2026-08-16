# LEGO Control System — v2 (voorstel)

Een open-source, modulair systeem om je LEGO-stad te automatiseren: schakelaarbediening, verkeerslichten en huisverlichting bedienen zonder ze aan te raken.

## Wat is dit
LEGO Control System biedt eenvoudige hardware‑ en softwaremodules waarmee je knoppen, servomotoren en verlichting op afstand kunt aansturen. Het doel is een praktische, toegankelijke basis voor hobbyisten en makers (ook voor wie hulp nodig heeft bij bouwen).

## Doelstellingen
- Modulaire hardware: elk module‑type is klein, makkelijk te bouwen en te vervangen.  
- Gebruiksvriendelijke besturing: eenvoudige interface op een hoofdunit (TFT + knoppen) en optionele web-/MQTT‑interface.  
- Toegankelijkheid: duidelijke bouwinstructies en voorbeelden zodat ook minder ervaren bouwers kunnen meedoen.

## Overzicht — Main Control Box
- TFT display (status + menu)  
- 20 fysieke knoppen (1 knop → 1 module, of meerdere knoppen per module)  
- Microcontroller: compatibel met veel boards (bijv. ESP32, Raspberry Pico) — keuze vrij te bepalen per build  
- Voeding: 5V DC, voldoende stroom voor servomotoren en LEDs  
- Communicatie: seriële, I2C of Wi‑Fi/MQTT (optioneel)

## Modules (eerste set)
- Main module (core): configuratie, routing en centrale communicatie.  
- Train switch module:
  - Tot 2 servomotoren (stappen/positieinstelling mogelijk)
  - Tot 4 lichtmasten (aan/uit + dim)
  - Eenvoudige aansluiting: 3‑ of 4‑pin connectoren voor servo’s en verlichting
- Light module (later): meerdere LEDs/strip‑uitgangen per module

## Hardware specificaties (voorbeeld — aan te passen)
- Servo voeding: gescheiden 5V rail aanbevolen voor servomotoren  
- Signaal: standaard PWM voor servo’s  
- Connectoren: JST‑3/4 pin of vergelijkbaar voor makkelijke montage  
- PCB‑footprint: kleine modulesize (bv. 40×25 mm) met schroefbevestiging

## Software overzicht
- Firmware: modulair, updatebaar per module (voorbeeldprojecten voor ESP32 beschikbaar)  
- Communicatieprotocollen: eenvoudige tekst‑API over seriële of MQTT‑topicstructuur  
- UI: lokaal op TFT + knoppen; optioneel webinterface of mobiele app via MQTT

## Roadmap (v2)
1. Documentatie uitbreiden
   - Gedetailleerde README (dit voorstel)
   - Wiring diagrams en connector-annotaties
2. Hardware ontwerpen
   - Eenvoudige Eagle/ KiCad‑schetsen voor train switch module
   - Prototype PCB en 3D‑behuizing
3. Firmware voorbeelden
   - ESP32 voorbeeld: servo + LED controle via MQTT en seriële commando’s
   - Basale calibratie‑routine voor wissels
4. GUI / Control UI
   - Basismenu op TFT
   - Optionele web‑UI voor afstandsbediening via Wi‑Fi
5. Tests & releases
   - Hardware testchecklist
   - 1.0 release met voorbeeld‑build en bill of materials (BOM)
6. Community & toegankelijkheid
   - NL/EN documentatie
   - Stappenplan voor bouwers met beperkte ervaring

## Hoe bijdragen
- Issues voor bugs, verbeteringen of ideeën. Gebruik labels: enhancement, bug, docs.  
- Pull requests: fork → branch → PR. Voeg in PR een korte beschrijving en testinstructies toe.  
- Code style: duidelijke, gedocumenteerde commits; hardware‑bestanden in /hardware; firmware in /firmware.

## Versiebeheer
- Dit document is voorstel “v2” — maak gerust opmerkingen of vraag om aanpassingen voordat ik het commit.

## Licentie
Zie LICENSE in de repository — gebruik dezelfde licentie als de rest van dit project.

---
Contact: open een issue of stuur hier een bericht in de repo voor vragen of wensen.
