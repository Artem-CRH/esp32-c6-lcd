# ESP32-C6-LCD mit ESPHome

Initiales Testprojekt fuer ein `esp32-c6-lcd` (Waveshare 1.47in ST7789V).

## 1) ESPHome Umgebung laden

```bash
cd /home/artem/git/esp32-c6-lcd
source .venv/bin/activate
```

## 2) WLAN Daten in `secrets.yaml` eintragen

Datei ist bereits angelegt:

- `wifi_ssid`
- `wifi_password`
- `wifi_ap_password`

## 3) Konfiguration pruefen

```bash
esphome config esp32-c6-lcd.yaml
```

## 4) Flashen (USB)

```bash
esphome run esp32-c6-lcd.yaml --device /dev/ttyACM0
```

Wenn kein `/dev/ttyACM0` existiert, den richtigen Port pruefen:

```bash
ls -l /dev/ttyACM* /dev/ttyUSB*
```

## 5) Home Assistant

`api:` ist bereits aktiv, damit taucht das Geraet in Home Assistant (ESPHome Integration) auf.

## Display-Test

Auf dem Display werden angezeigt:

- Titel `Display-Test`
- Laufzeit in Sekunden (grosser gruener Wert)
- Text `Sekunden seit Start`
