# AgriGuard AI — Precision Crop Pest Identification System

An ultra-modern, deep learning-powered crop pest diagnosis and Integrated Pest Management (IPM) platform built with **HTML5, Modern CSS (Glassmorphism & Green Theme), JavaScript (ES6+)**, **Python Flask**, and **TensorFlow / Keras (EfficientNetB4)**.

---

## 🌟 Modern Features & Upgrades

- **🌿 Modern Green Theme with Dark & Light Mode**:
  - High-tech emerald and mint palette with glassmorphism surfaces (`backdrop-filter: blur(16px)`), subtle glowing ambient lights, and micro-elevations.
  - Interactive theme switcher in the navbar with local storage persistence.
- **⚡ Multiple Image Input Channels**:
  - Drag & drop or click-to-browse with live drag highlights.
  - Mobile & webcam direct camera capture (`capture="environment"`).
  - Instant clipboard paste (<kbd>Ctrl+V</kbd>) from screenshots or camera.
  - **Quick Test Presets**: Test Aphids, Bollworm, Grasshopper, Thrips, Whitefly, and Healthy Leaf with 1 click.
- **🔬 Laser Scanning & Real-Time Diagnostics**:
  - Animated futuristic laser bar sweeps the preview during neural processing.
  - Circular animated SVG confidence gauge dynamically color-coded by certainty (Mint > 80%, Amber 50-80%, Coral < 50%).
  - Severity risk triage pill (🔴 Critical Hazard, 🟡 High Hazard, 🔵 Moderate, 🟢 Safe).
- **📋 Categorized IPM Protocols & Tabs**:
  - **Bio-Profile**: Scientific classification, life-cycle traits, host crops.
  - **Symptoms**: Visible foliar damage and insect activity checklist.
  - **IPM Treatment**: Cultural, biological (natural predators), and chemical controls.
  - **Prevention**: Field sanitation, trap cropping, and border barriers.
- **🔊 Practical Field Utilities**:
  - **Listen (Text-to-Speech)**: Speaks diagnosis and treatments aloud for hands-free field consultation.
  - **Print / PDF Export**: Clean, dedicated printable format for agronomist inspection records.
  - **Copy Report Summary**: Instant clipboard copy formatted for SMS, WhatsApp, or email.
- **📖 Interactive Pest Knowledge Library**:
  - Searchable and browsable card catalog of all 6 target classes with 1-click "Test Sample" buttons.
- **🛡️ Robust Dual-Mode Resilience**:
  - Operates as a full live Flask backend (`python app.py`) with real EfficientNetB4 inference.
  - Operates standalone on static hosting (GitHub Pages, Netlify) with intelligent sample simulation from `pest_info.json`.
  - Graceful fallback: If TensorFlow is missing or weights are pending, the server safely runs in Simulation Mode rather than crashing.

---

## 📁 Project Structure

```text
PestIdentificationSystem/
├── index.html               # Diagnostic scanner and pest identification hub
├── about.html               # Mission, team, deep learning architecture & pillars
├── contact.html             # Agronomy advisory desk, inquiry form & FAQs
├── app.py                   # Hardened Flask backend and EfficientNetB4 inference API
├── pest_info.json           # Comprehensive botanical profiles, symptoms & IPM treatments
├── requirements.txt         # Python dependencies
├── model/
│   ├── config.json          # EfficientNetB4 architecture configuration (optional if weights present)
│   ├── metadata.json        # Keras version metadata
│   ├── model.weights.h5     # Trained model weights (69 MB)
│   └── class_names.json     # 6 trained class labels
└── static/
    ├── css/
    │   └── style.css        # Modern green styling, animations, and print CSS
    └── js/
        └── script.js        # Modern ES6 interactive controller & audio engine
```

---

## 🚀 Quick Start Guide

### Option 1: Run Locally with Python Flask

1. **Install Python 3.10, 3.11, or 3.12 (64-bit)**.
2. Open terminal in the project directory and create a virtual environment:
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Start the server:
   ```bash
   python app.py
   ```
5. Open **`http://localhost:5000`** in your browser. The status badge will indicate runtime health.

---

### Option 2: Deploy to GitHub Pages (Static Preview)

1. Upload all contents of `PestIdentificationSystem/` to your GitHub repository (so `index.html` is at root).
2. Go to **Repository Settings → Pages**.
3. Under **Build and deployment**, set source to **Deploy from a branch** (`main` / `/ root`), and save.
4. Open your GitHub Pages URL — the application will automatically activate **GitHub Pages Preview Mode** with full interactive sampling, image upload preview, and IPM catalog inspection.
