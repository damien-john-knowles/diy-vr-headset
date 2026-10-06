# Roadmap

## Phase 0: Research
- [ ] Survey existing open projects (Relativty, OSVR, Monado, ESP32/RP2040 VR trackers)
- [ ] Pick display(s): single 2.9" 1440x1440 per eye, or one 5.5" 2560x1440 panel
- [ ] Pick lenses: aspheric 40-50 mm or Fresnel

## Phase 1: 3-DoF prototype
- [ ] IMU (BNO085 / ICM-42688) on an RP2040 or ESP32-S3
- [ ] Sensor fusion and USB HID report
- [ ] Cardboard or foam-board enclosure to validate optics

## Phase 2: SteamVR integration
- [ ] OpenVR driver that reads the HID pose
- [ ] Lens distortion correction and IPD configuration
- [ ] Latency measurement

## Phase 3: Printed enclosure
- [ ] Parametric CAD enclosure with adjustable IPD
- [ ] Face gasket and head strap
- [ ] Cooling and cable management

## Phase 4: 6-DoF tracking
- [ ] Evaluate inside-out (camera + SLAM via Monado) versus lighthouse sensors
- [ ] Controllers
