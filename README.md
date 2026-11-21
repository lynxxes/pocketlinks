# PocketLink Swing Meter

An arcade-style mobile golf swing simulator powered entirely by smartphone motion sensors—no AR, cameras, or external hardware required.

**Live Demo:** [https://lynxxes.github.io/pocketlinks/](https://lynxxes.github.io/pocketlinks/)

---

## Overview

PocketLink turns your smartphone into a tactile golf club grip. Hold your thumbs on the on-screen grip bar to address the ball, take a real swing using your phone's accelerometer and gyroscope, feel a haptic vibration and synthesized club-strike crack at peak downswing impact, and inspect your carry yardage and shot dispersion on the 2D fairway radar.

## Features

- **Two-Thumb Club Grip Bar:** Multi-touch hold-to-arm mechanic (`Left Thumb` / `Right Thumb`) that prevents accidental triggers while walking and locks telemetry once a swing completes.
- **Real-Time Swing Telemetry:** Uses the Web `DeviceMotion` API (~60Hz) to calculate total acceleration magnitude ($\sqrt{a_x^2 + a_y^2 + a_z^2}$) and detect peak downswing impact inflection.
- **Multi-Platform Impact Haptics & Audio:**
  - **Android (Chrome):** Double-pulse `navigator.vibrate()` feedback on grip lock and ball impact.
  - **iOS 17.4+ (Safari):** Native Taptic feedback via `<input type="checkbox" switch>` fallback.
  - **Web Audio Synthesizer:** Real-time synthesized club-strike sound effects scaled to swing power.
- **Club Selection & Fairway Radar:** Switch between **Driver (280 yds)**, **5-Iron (195 yds)**, **7-Iron (165 yds)**, and **P-Wedge (115 yds)** with a live 2D trajectory arc and session shot log.
- **Desktop Simulator Mode:** Built-in **Simulate Swing** and **Test Impact** triggers for testing UI, audio, and physics on desktop browsers without motion sensors.

## How to Use

1. Open **[https://lynxxes.github.io/pocketlinks/](https://lynxxes.github.io/pocketlinks/)** on your mobile browser over **HTTPS**.
2. Tap **Enable Motion Sensors** and grant motion/orientation access when prompted.
3. Select your club (**Driver**, **5-Iron**, **7-Iron**, or **P-Wedge**).
4. Grip your phone firmly with both hands, press and hold both thumbs on the **Left Thumb** and **Right Thumb** pads until the bar locks (`GRIP LOCKED — READY TO SWING`), and take a controlled swing.
5. Release your thumbs after impact to review your carry distance, peak G-force, dispersion, and trajectory arc.

## Tech Stack

- **Frontend:** Self-contained single-file HTML5, CSS3, and Vanilla JavaScript (`index.html`)
- **APIs:** `DeviceMotionEvent`, `Navigator.vibrate()`, Web Audio API, HTML5 Canvas (2D Fairway Radar)
- **Hosting:** GitHub Pages (HTTPS required for iOS/Android motion sensor permissions)

## Safety Notice

Always maintain a firm two-handed grip on your device and ensure adequate clearance from ceilings, fans, walls, and people before swinging.
