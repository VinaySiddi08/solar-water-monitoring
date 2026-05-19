# Solar-Powered Smart Water Monitoring System

An off-grid IoT system that monitors water quality in real time using solar power, with cloud dashboards for remote visibility.

## Problem

Water quality in rural and off-grid settings is often unmonitored because traditional monitoring requires grid power and wired infrastructure. This project builds a **self-powered**, **cloud-connected** monitoring node that can be deployed where neither power nor wired networking is available.

## How it works

1. **Sensors continuously measure** turbidity, pH, and Total Dissolved Solids (TDS) in a water source.
2. **A microcontroller** reads the analog signals, applies calibration curves, and aggregates readings.
3. **Solar panel + battery** provides 24/7 operation, with the panel sized for the expected duty cycle.
4. **Wi-Fi connectivity** pushes readings to the **Blynk cloud platform**, where they're displayed on a real-time dashboard.
5. **Threshold alerts** notify users when any parameter crosses safe limits.

## Hardware

- Microcontroller (ESP-based for built-in Wi-Fi)
- Turbidity sensor
- Analog pH sensor with probe
- TDS sensor
- 6V/10W solar panel
- Li-ion battery + charge controller

## Software

- **Arduino C++** for sensor read loops and calibration
- **Blynk** platform for cloud dashboards and mobile app integration
- **MQTT** for telemetry

## What I learned

- **Sensor calibration is the project.** pH and TDS sensors drift with temperature and use; calibrating against known buffer solutions is essential.
- **Solar sizing is unintuitive.** I oversized the first iteration based on peak draw rather than average duty cycle, which wasted weight and cost.
- **Cloud-based dashboards lower the cost of a working demo.** Blynk handled visualization, alerts, and authentication, which let me focus on the sensing and power problems.

## Status

Working prototype demonstrated as part of undergraduate project work. Field-tested over a 2-week deployment.

---

**Author:** Vinay Siddi
**Contact:** vsiddi@albany.edu
