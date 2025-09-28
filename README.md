# 🧠 IKEA on/off-switch (Zigbee2MQTT) — Blueprint för Home Assistant

**Version:** 1.0.0  
**Författare:** MittSmartaHem https://www.mittsmartahem.nu  
**Kräver:** Home Assistant 2024.6.0 eller senare  
**Kompatibel med:** IKEA E1743 on/off-knapp via Zigbee2MQTT

---

## 🎯 Syfte

Denna blueprint låter dig använda IKEA:s klassiska on/off-knapp (modell E1743) för att trigga valfria funktioner i Home Assistant. Den stödjer både kort och lång tryckning på ON/OFF.

---

## ⚙️ Funktioner

- 🟢 Kort tryck på ON 
- 🔴 Kort tryck på OFF 
- 🔆 Långt tryck på ON
- 🌑 Långt tryck på OFF
- 🧠 Intern logik — inga helpers krävs  
- 📋 Fallback-loggning vid okända kommandon

---

## 🧱 Inputs

| Input              | Beskrivning                                      |
|--------------------|--------------------------------------------------|
| `remote`           | MQTT-sensor som representerar IKEA-knappen       |
| `on_button_short`  | Action vid kort tryck på ON                      |
| `off_button_short` | Action vid kort tryck på OFF                     |
| `on_button_long`   | Action vid långt tryck på ON (brightness up)     |
| `off_button_long`  | Action vid långt tryck på OFF (brightness down)  |

---

## 🚀 Kom igång

1. Gå till **Inställningar > Automations & Scener > Blueprints > Importera Blueprint**
2. Klistra in RAW-länken till blueprint-filen från GitHub
3. Skapa en ny automation baserad på blueprinten

---


## 🛠 Tips

- Se till att Zigbee2MQTT är konfigurerad med `legacy: false` för att `action` ska rapporteras korrekt.
- Du kan återanvända blueprinten för flera knappar — välj bara rätt sensor.
