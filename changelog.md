# Changelog

All notable changes to the **PocketLink Swing Meter** web app are documented in this file.

## [0.2.0] - 2026-11-21

### Added
- **Two-Thumb Club Grip Bar (`#clubGripBar`):** Multi-touch hold-to-swing input requiring simultaneous Left Thumb and Right Thumb contact to arm the accelerometer, preventing false triggers and locking shot telemetry upon completion.
- **Cross-Platform Impact Haptics:** Added `triggerHapticPulse([65, 25, 35], true)` on peak downswing impact using `navigator.vibrate` on Android and a native `<input type="checkbox" switch>` Taptic fallback for iOS 17.4+ Safari.
- **Test Impact Button:** Added a manual trigger to preview impact vibration and synthesized strike audio without swinging.
- **2D Fairway Radar:** Added an HTML5 Canvas trajectory arc displaying live ball flight, carry distance, and left/right shot dispersion.
- **Expanded Club Lineup:** Added **5-Iron (195 yds)** and **P-Wedge (115 yds)** alongside **Driver (280 yds)** and **7-Iron (165 yds)**.

### Changed
- Replaced the single-tap **Ready / Address Ball** button with the hold-to-arm **Two-Thumb Club Grip Bar**.

---

## [0.1.0] - 2026-11-21

### Added
- Initial self-contained single-file web prototype (`index.html`) deployed via GitHub Pages over HTTPS.
- `DeviceMotionEvent` sensor integration with explicit iOS Safari `requestPermission()` flow.
- Real-time peak G-force vector calculation and downswing impact inflection detection.
- Web Audio API synthesized golf-ball impact sound effects.
- Desktop **Simulate Swing** button and recent shot history log.