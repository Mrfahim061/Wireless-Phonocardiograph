# Wireless Phonocardiograph – Web Application

A browser-based interface for recording, visualizing, and listening to heart sounds (phonocardiogram, PCG) in real time from a low-cost Bluetooth wireless stethoscope.

This web app is part of the work presented in:

> **Development of a Low-Cost Wireless Phonocardiograph using Bluetooth Module with a User Friendly Smartphone Application**
> M. R. Fahim, A. S. Chowdhury, A. Ghosh, A. Hossan
> 2024 6th International Conference on Electrical Engineering and Information & Communication Technology (ICEEICT), MIST, Dhaka, Bangladesh.
> DOI: [10.1109/ICEEICT62016.2024.10534563](https://doi.org/10.1109/ICEEICT62016.2024.10534563)

## Overview

Cardiovascular disease (CVD) is a leading cause of death worldwide, and early screening is especially important in resource-limited settings. The hardware in this project combines a conventional stethoscope chest-piece, a sensitive condenser microphone, and a Bluetooth module (CSR8640) in a 3D-printed casing. Once paired with a laptop or smartphone, it works as a wireless audio input, and this web app turns that input into a simple phonocardiograph.

## Features

- **Real-time visualizer**: live waveform of the heart sound while recording (WaveSurfer.js)
- **Real-time listening**: hear the heart sound live through headphones or speakers while positioning the chest-piece
- **Recording and playback**: record, replay, and download the recording as an audio file
- **Patient information form**: fields for personal and patient details (name, ID, age, weight, height, etc.)
- **No backend required**: everything runs in the browser, so it can be hosted as a static page (e.g., GitHub Pages)

## How It Works

1. Pair the wireless stethoscope with your laptop or phone via Bluetooth.
2. Open the web app and allow microphone access.
3. Select the Bluetooth device as the audio input in your system or browser settings.
4. Press **Record** to start the live waveform visualization and recording.
5. Use **Start / Stop** under *Real-time listening* to hear the heart sound live.
6. After stopping, use **Play** to review the recording and **Download recording** to save it for further analysis (e.g., filtering and heart-rate estimation in MATLAB).

## Getting Started

### Run locally

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

Browsers only allow microphone access on `https://` or `localhost`, so opening the file directly may not work. Serve it with a local server instead:

```bash
# Python 3
python -m http.server 8000
```

Then open `http://localhost:8000` in Chrome or Edge.

### Host on GitHub Pages

1. Push `index.html` (and `icon.jpg`) to the repository.
2. Go to **Settings → Pages**.
3. Under *Source*, choose the `main` branch and the root folder, then save.
4. Your app will be available at `https://<your-username>.github.io/<your-repo>/`.

## Project Structure

```
├── index.html    # Web application (HTML, CSS, JavaScript)
├── icon.jpg      # Header icon
└── README.md
```

## Tech Stack

- HTML, CSS, JavaScript
- [WaveSurfer.js v7](https://wavesurfer.xyz/) with the Record plugin (loaded from a CDN)
- Web Audio / MediaRecorder APIs

## Requirements

- A modern browser (Chrome, Edge, or Firefox)
- Microphone permission
- Internet connection on first load (for the WaveSurfer.js CDN)
- Bluetooth wireless stethoscope paired as an audio input (a built-in or USB microphone also works for testing)

## Results

The device was tested on 30 healthy adult volunteers (15 male, 15 female). Heart rates obtained from the recordings were closely aligned with those from a BIOPAC MP36 reference system. See the paper for details.

## Limitations

- Best performance in a quiet environment; noise and improper chest-piece placement can affect signal quality.
- Fetal heart sound recording is affected by maternal heart sounds.
- This tool is intended for research and educational purposes, **not** for clinical diagnosis.

## Citation

```bibtex
@inproceedings{fahim2024wirelesspcg,
  title     = {Development of a Low-Cost Wireless Phonocardiograph using Bluetooth Module with a User Friendly Smartphone Application},
  author    = {Fahim, Mahabur Rahman and Chowdhury, Abu Shahid and Ghosh, Avishek and Hossan, Arif},
  booktitle = {2024 6th International Conference on Electrical Engineering and Information \& Communication Technology (ICEEICT)},
  year      = {2024},
  doi       = {10.1109/ICEEICT62016.2024.10534563}
}
```

## Authors

- Mahabur Rahman Fahim
- Abu Shahid Chowdhury
- Avishek Ghosh
- Arif Hossan

Khulna University of Engineering & Technology (KUET), Khulna, Bangladesh.

## License

Add a license of your choice (e.g., MIT) in a `LICENSE` file.
