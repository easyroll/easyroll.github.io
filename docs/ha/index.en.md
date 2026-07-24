# EasyRoll × Home Assistant Integration Guide

Connecting your EasyRoll Smart Blind to **Home Assistant** lets you control it directly at home without the cloud, and use it in HA automations (sunrise/sunset, temperature triggers, etc.).

---

## Contents

| Step | Description |
|---|---|
| [1. Getting Started · Requirements](01_시작하기_준비물.md) | Integration method · Mosquitto broker · checklist |
| [2. Connecting the Device](02_기기_연결하기.md) | Connect with just a browser (no app needed) |
| [3. Using It in HA](03_HA에서_사용하기.md) | Cards · position slider · automation YAML examples |
| [4. Advanced Commands](04_고급_명령어.md) | Direct MQTT control · switching servers |
| [5. Troubleshooting](05_문제해결.md) | Connection failures · behavior when the broker is down |

---

## Quick Start

1. Install the **Mosquitto broker** add-on in HA → [check the requirements](01_시작하기_준비물.md)
2. Power ON the blind → connect your phone to the device Wi-Fi → open `192.168.4.1` → choose **[Home Assistant]** → [details](02_기기_연결하기.md)
3. It registers automatically in HA — ready to use!

## Highlights

- **Local connection** — works at home even when the internet is down
- **Automatic registration** (MQTT Discovery) — no manual YAML required
- **Automatic online/offline status**

---

For general usage, see the [User Manual](../easyroll/index.md).
Questions: **Customer Center 031-358-1016** (weekdays 09:00–18:00) · Website **[easyroll.kr](https://easyroll.kr)**
