# Short Description (for the GitHub "About" field)

Pick one of these:

> **Option 1:** A web application for real-time visualization, listening, recording, and storing of heart sound (PCG) data from a low-cost wireless phonocardiograph device via Bluetooth.

> **Option 2:** Low-cost wireless phonocardiograph web app — record, visualize, and listen to heart sounds in real time for early CVD screening. (IEEE ICEEICT 2024)

---

# README.md

Copy the content below into a file named `README.md`:

```markdown
# 🫀 Wireless Phonocardiograph — Web Application

A browser-based application for **real-time visualization, listening, recording,
and storing of phonocardiogram (PCG) data**, developed for a low-cost wireless
phonocardiograph device built from a stethoscope chest-piece, a condenser
microphone, and a Bluetooth module.

## 📋 Overview

Cardiovascular diseases (CVDs) are the leading cause of death worldwide.
Phonocardiography (PCG) records heart sounds non-invasively and offers a
promising, low-cost approach for early CVD detection — especially in
resource-limited settings.

This web application connects to the wireless PCG device over Bluetooth and
allows the user to:

- 📝 Enter and store patient information
- 🎧 Listen to heart sounds in real time
- 📈 Visualize the live heart sound waveform
- 💾 Record and download PCG data for further analysis (e.g., MATLAB filtering)

## ✨ Features

- **Patient data entry** — personal and medical details (name, ID, age, gender, weight, height, contact info)
- **Real-time visualizer** — live waveform rendering using [WaveSurfer.js v7](https://wavesurfer.xyz/) (Record plugin)
- **Real-time listening** — instant audio playback via the browser's audio APIs
- **Recording & storage** — record, replay, and download heart sound recordings
- **Fully wireless** — works with any Bluetooth-paired laptop or smartphone
- **No installation** — runs entirely in the browser; can be hosted free on GitHub Pages

## 🛠️ Technology Stack

| Component             | Technology                                          |
|-----------------------|-----------------------------------------------------|
| Structure             | HTML5                                               |
| Styling               | CSS3                                                |
| Interactivity         | JavaScript (ES6 modules)                            |
| Waveform visualization| WaveSurfer.js v7 — Record plugin                    |
| Audio capture         | MediaRecorder API / `getUserMedia`                  |
| Companion hardware    | Bluetooth module (CSR8640), condenser microphone, stethoscope chest-piece |
| Post-processing       | MATLAB (noise filtering, amplification, heart-rate estimation) |

## 🚀 Getting Started

### Prerequisites
- A modern browser (Chrome, Edge, Firefox, Safari)
- Microphone or Bluetooth audio input permission
- The wireless PCG device paired with your computer/smartphone
  (any microphone can be used for testing without the device)

### Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/wireless-phonocardiograph-webapp.git
   ```
2. Open `index.html` in your browser (a local server is recommended).
3. Allow microphone access when prompted.
4. Press **Record** to start capturing heart sounds.

> ⚠️ **Note:** Browsers only allow microphone access in a secure context
> (HTTPS or `localhost`). Use GitHub Pages or a local server for full functionality.

## 🩺 How It Works
1. The chest-piece + microphone capture heart sounds acoustically.
2. Audio is transmitted wirelessly over Bluetooth to the smart device.
3. The web app records, visualizes, and plays the signal in real time.
4. Recordings are downloaded and post-processed in MATLAB
   (moving-average filtering, 1.5× amplification, peak-detection heart-rate counting).

## 📊 Validation

The system was tested on **30 subjects (15 male, 15 female)** and compared with a
**BIOPAC MP36** data acquisition unit. Heart rates measured by both modalities were
closely aligned, confirming the reliability of the low-cost setup.

## 📄 Related Publication

M. R. Fahim, A. S. Chowdhury, A. Ghosh, and A. Hossan,
*"Development of a Low-Cost Wireless Phonocardiograph using Bluetooth Module with
a User Friendly Smartphone Application,"* in **2024 6th International Conference on
Electrical Engineering and Information & Communication Technology (ICEEICT)**,
Dhaka, Bangladesh, 2024.
DOI: [10.1109/ICEEICT62016.2024.10534563](https://doi.org/10.1109/ICEEICT62016.2024.10534563)

## 📁 Repository Structure
```
├── index.html   # Main web application
├── icon.jpg     # Application icon
└── README.md    # Project documentation
```

## 🤝 Acknowledgments

Department of Biomedical Engineering and Department of Electronics and
Communication Engineering, Khulna University of Engineering & Technology (KUET),
Bangladesh.

## 📜 License

This project is intended for academic and research purposes.
```

---

# Quick Steps to Upload to GitHub

1. **Create a new repository** on GitHub (e.g., `wireless-phonocardiograph-webapp`).
2. Paste the short description into the **Description** field.
3. Click **Add file → Upload files** and upload:
   - `index.html`
   - `icon.jpg` *(required — your HTML references it)*
   - `README.md` (the file above)
4. Click **Commit changes**.
5. *(Optional)* Enable **Settings → Pages → Deploy from branch** to host it live on GitHub Pages — this matches the "GitHub Page Hosting" step in your paper's software flow diagram. 🔗

**One tip:** since your README and app are public, make sure your IEEE paper's posting terms allow sharing — the ©2024 IEEE notice generally permits hosting the *application* but not the full PDF of the paper.
