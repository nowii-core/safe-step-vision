# SafeStep AR

A lightweight, modern, and responsive web application built for simplicity.
An experimental real-time terrain scanner powered by vanilla HTML, CSS, and JavaScript, designed to assist hikers with live step guidance, hazard detection, and distance estimation.

[Overview](#overview) | [Features](#features) | [Quick Start](#quick-start) | [Structure](#structure) | [Development](#development) | [License](#license)

## Overview

**SafeStep AR** is a lightweight web application designed around simplicity, real-time computer vision analysis, and maintainability.
Built with standard web technologies, it keeps the project structure straightforward and easy to understand. It processes camera frames using high-performance HTML5 Canvas gradient detection, integrating mobile motion sensors to calculate distances and flag terrain risks without relying on external libraries or heavy frameworks.

With no build system required for basic development, SafeStep AR provides a simple starting point for experimenting with augmented reality and web-based terrain scanning.

## Features

- **Real-Time Terrain Analysis** — Uses a low-resolution canvas algorithm to detect surface stability and texture gradients in real time.
- **Smart Foot Placement** — Highlights optimal left (`L`) and right (`R`) stepping positions based on surface grip scoring.
- **Hazard Detection** — Automatically flags unstable scree, deep holes, and dangerous ledges with dynamic visual indicators.
- **Sensor-Based Range Finder** — Calculates distance metrics based on device tilt angle (`DeviceOrientation`) and phone height.
- **Integrated Demo Mode** — Allows full testing of the HUD and detection features without requiring camera permissions.
- **Zero Dependencies** — Built with vanilla HTML, CSS, and JavaScript with no external npm packages or heavy frameworks.
- **Responsive HUD Interface** — Inspired by tactical displays, optimized for legibility under bright outdoor conditions.
- **Offline & Mobile Ready** — Optimized for mobile browsers with full touch and wake-lock capabilities.

## Preview

**Live Demo:** [https://nowii-core.github.io/safe-step-vision/](https://nowii-core.github.io/safe-step-vision/)

## Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **HTML5** | Application structure, video stream input, and canvas layers |
| **CSS3** | Modern styling, responsive UI elements, and HUD layout |
| **JavaScript (ES6+)** | Computer vision algorithms, sensory distance calculations, and app state |
| **DeviceOrientation API** | Pitch and inclination measurement for real-time terrain depth mapping |
| **MediaDevices API** | Camera stream access for live video processing |

**Dependencies:** None required.

## Quick Start

### Requirements

- A modern web browser (Chrome, Safari, Firefox, Edge).
- A smartphone or mobile browser (recommended for camera and orientation sensor functionality).
- Visual Studio Code or another code editor for local development.

### Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/nowii-core/safe-step-vision.git
   ```

2. **Enter the project directory**
   ```bash
   cd safe-step-vision
   ```

3. **Open the project**
   ```bash
   code .
   ```

4. **Start the application**
   Open `index.html` using the Live Server extension in Visual Studio Code or host it locally.

> **Note:** Camera access and motion sensor APIs require **HTTPS** or a trusted local environment such as `localhost`.

## Project Structure

```text
safe-step-vision/
└── index.html       # Single-file application combining structure, styling, and logic
```

## Customization

SafeStep AR's straightforward single-file architecture makes it easy to adapt to your needs:

- **Interface & Structure:** Modify the HTML templates inside `index.html` to adjust the HUD elements or control buttons.
- **Visual Styling:** Edit the CSS variables (`--bg`, `--ok`, `--bad`, `--scan`) to change the HUD color palette.
- **Detection Algorithm:** Adjust parameters like `CS` (cell size) or sensitivity thresholds (`thr`) inside the JavaScript section to tweak terrain analysis sensitivity.
- **Sensor Calibration:** Modify `VFOV` (Vertical Field of View) or default camera height (`hCam`) to match specific device profiles.

## Development

SafeStep AR is designed to be easy to work with using a minimal development setup.

### Recommended Workflow

1. Open the project in your preferred editor.
2. Start a local HTTPS/localhost development server.
3. Modify the HTML, CSS, or JavaScript code.
4. Refresh the browser to test changes.
5. Verify sensor responsiveness on a physical mobile device.

## Security & Privacy

SafeStep AR operates **entirely client-side**. Camera streams and orientation data are processed in memory and are never uploaded, stored, or transmitted to external servers.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact & Support

- **Maintainer:** [@nowii-core](https://github.com/nowii-core)
- **Repository:** [https://github.com/nowii-core/safe-step-vision](https://github.com/nowii-core/safe-step-vision)
- **Issues & Feature Requests:** [Submit an Issue](https://github.com/nowii-core/safe-step-vision/issues)

---

<div align="center">
  <sub>Developed by <b>nowii-core</b></sub>
</div>
