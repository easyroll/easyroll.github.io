# EasyRoll × Home Assistant Integration Guide

Connecting your EasyRoll Smart Blind to **Home Assistant** lets you control it directly at home without the cloud, and use it in HA automations (sunrise/sunset, temperature triggers, etc.).
We recommend the **Hybrid** setup — keep the EasyRoll app and connect HA **in addition**: if the server is down you still control via HA, and if HA is off the app still works.

---

## Contents

| Step | Description |
|---|---|
| [1. Getting Started · Requirements](01_시작하기_준비물.md) | Integration method · Mosquitto broker · checklist |
| [2. Connecting the Device](02_기기_연결하기.md) | **Hybrid (app + HA together) ★Recommended** · HA only |
| [3. Using It in HA](03_HA에서_사용하기.md) | Cards · position slider · automation YAML examples |
| [4. Advanced Commands](04_고급_명령어.md) | Direct MQTT control · switching servers |
| [Move / Remove Device](06_기기_이전하기.md) | Move to another home/HA (clear HA connection) |
| [5. Troubleshooting](05_문제해결.md) | Connection failures · behavior when the broker is down |

---

## Quick Start

1. Install the **Mosquitto broker** add-on in HA → [check the requirements](01_시작하기_준비물.md)
2. **Register the device with the EasyRoll app** (skip if already in use) → [Register Device](../easyroll/02_앱_등록하기.md)
3. In a browser open `http://<blind IP>:20318/hasetup` → enter the HA info + **tick [Easyroll 앱과 함께 사용]** → save → [details](02_기기_연결하기.md)
4. It registers automatically in HA — use **both the app and HA** right away!

## Highlights

- **Local connection** — works at home even when the internet is down
- **Automatic registration** (MQTT Discovery) — no manual YAML required
- **Automatic online/offline status**
- **App + HA at the same time (Hybrid)** — local HA control if the server is down, and the app still works if HA is off (firmware V3.2.0T4+)

---

For general usage, see the [User Manual](../easyroll/index.md).
<div class="er-contactbar" markdown>

:material-phone-in-talk: **Customer Center** 031-358-1016 · Weekdays 09:00 – 18:00

:material-web: **Website** [easyroll.kr](https://easyroll.kr) · Community → Q&A board

</div>
