# DIY VR Headset

An open-source, build-it-yourself virtual reality headset: off-the-shelf displays and lenses, a 3D-printed enclosure, microcontroller-based IMU tracking, and a SteamVR/OpenXR driver.

> **Status:** early planning. Nothing here is a finished, tested design yet.

## Goals

- Cheap to build from parts you can buy online, ideally under $250
- 3D-printable enclosure and face gasket
- 3-DoF rotational tracking first, then 6-DoF (inside-out or lighthouse)
- Works with SteamVR via an OpenVR driver, with OpenXR support later
- Fully documented so a hobbyist can build one start to finish

## Planned architecture

```
┌─────────────┐  USB HID   ┌──────────────────┐      ┌─────────┐
│ MCU + IMU   │ ─────────▶ │ PC driver        │ ───▶ │ SteamVR │
│ (firmware/) │            │ (software/driver)│      │ OpenXR  │
└─────────────┘            └──────────────────┘      └─────────┘
┌─────────────┐  HDMI/DP
│ Display(s)  │ ◀───────── GPU
└─────────────┘
```

## Repository layout

| Path | Contents |
|------|----------|
| [`docs/`](docs/) | Build guide, roadmap, design notes |
| [`hardware/`](hardware/) | Bill of materials, electronics schematics, optics notes |
| [`cad/`](cad/) | Enclosure, lens mounts, and strap models (STEP/STL plus source files) |
| [`firmware/`](firmware/) | Microcontroller code for IMU sensor fusion and USB HID |
| [`software/`](software/) | PC-side driver, lens distortion and calibration tools |

## Getting started

1. Read the [roadmap](docs/ROADMAP.md)
2. Check the [bill of materials](hardware/BOM.md)
3. Follow the [build guide](docs/BUILD_GUIDE.md) (in progress)

## Contributing

Contributions are welcome. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Safety

Use this at your own risk. Poor tracking latency or mismatched lens/IPD settings can cause motion sickness and eye strain. Never look into a display without lenses at close range for long periods, and take breaks.

## License

Software and firmware: [MIT](LICENSE). Hardware designs are intended to be shared under CERN-OHL-P v2.
