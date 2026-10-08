# EasyRoll × Home Assistant Integration Guide

Connecting your EasyRoll Smart Blind to **Home Assistant** lets you control it directly at home without the cloud, and use it in HA automations (sunrise/sunset, temperature triggers, etc.).
We recommend the **Hybrid** setup — keep the EasyRoll app and connect HA **in addition**: even if the internet goes down, HA can still control it locally, and even if HA is off you keep control via the app as long as the internet is connected.

---

## Contents

| Step | Description |
|---|---|
| [1. Getting Started · Requirements](01_시작하기_준비물.md) | Integration method · Mosquitto broker |
| [2. Connecting the Device](02_기기_연결하기.md) | **① From the app (Hybrid) ★Recommended** · ② Device setup page by typing the IP |
| [3. Using It in HA](03_HA에서_사용하기.md) | Cards · position slider · automation YAML examples |
| [4. Advanced Commands](04_고급_명령어.md) | Direct MQTT control |
| [Move / Remove Device](06_기기_이전하기.md) | Deleting in the app cleans up HA automatically · HA-only: `EZS_HARESET$` |
| [5. Troubleshooting](05_문제해결.md) | Connection failures · behavior when the broker is down |

---

## Quick Start

1. Install the **Mosquitto broker** add-on in HA → [check the requirements](01_시작하기_준비물.md)
2. **Register the device with the EasyRoll app** (skip if already in use) → [Register Device](../easyroll/02_앱_등록하기.md)
3. In the app, tap ⚙ next to the zone name → **[구역 기기 설정] → [Home Assistant 연결]** → select devices + enter the broker info → **[연결하기]** → [details](02_기기_연결하기.md)
4. It registers automatically in HA — use **both the app and HA** right away!

## Highlights

- **Local connection** — works at home even when the internet is down
- **Automatic registration** (MQTT Discovery) — no manual YAML required
- **Automatic online/offline status**
- **App + HA at the same time (Hybrid)** — **control from both the EasyRoll app and HA simultaneously.** Even if the internet goes down, HA can still control it locally, and even if HA is off you keep control via the app as long as the internet is connected (firmware V3.2.0+)

---

For general usage, see the [User Manual](../easyroll/index.md).
<div class="er-contactbar" markdown>

:material-phone-in-talk: **Customer Center** 031-358-1016 · Weekdays 09:00 – 18:00

:material-web: **Website** [easyroll.kr](https://easyroll.kr) · Community → Q&A board

</div>
