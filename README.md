# 🌿 KS LAB – Natural Photo Editor

> A beautiful, browser-based photo editor that auto-retouches images at **full resolution** with natural, realistic enhancements.

![KS LAB](https://img.shields.io/badge/KS%20LAB-Natural%20Photo%20Editor-a8e063?style=for-the-badge&labelColor=0e0f0d)
![HTML](https://img.shields.io/badge/HTML-Single%20File-e34c26?style=for-the-badge&logo=html5&logoColor=white)
![No Backend](https://img.shields.io/badge/Backend-None%20Required-56ab2f?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-brightgreen?style=for-the-badge)

---

## ✨ Features

- 📸 **Full Resolution Processing** — No downscaling, original pixel dimensions preserved
- 🎨 **Auto Smart Retouch** — Brightness, contrast, sharpness, skin smoothing, saturation
- 💾 **Lossless PNG Download** — Zero quality loss output saved to your Downloads folder
- 🖼️ **Before / After Preview** — Side-by-side comparison
- 🌿 **Bokeh Background UI** — Photoshop-style blurred bokeh with grain overlay
- 🐒 **Monkey Mascot** — Animated KS mascot above the upload card
- 📱 **Responsive** — Works on desktop and mobile
- ⚡ **Zero Dependencies** — Pure HTML + CSS + JavaScript, no npm, no build step

---

## 🚀 Live Demo

> **GitHub Pages:** `https://<your-username>.github.io/kslab/`

---

## 📁 Project Structure

```
kslab/
├── index.html      ← The entire app (single file)
└── README.md       ← This file
```

---

## 🛠️ How to Use

### Option 1 — Open Locally
1. Download `index.html`
2. Double-click it → opens in any browser
3. Upload a photo → auto-edited instantly
4. Click **"Download Full Quality"** → saved as PNG

### Option 2 — GitHub Pages (Recommended)
1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Visit `https://<your-username>.github.io/kslab/`

---

## 🔧 How It Works

```
Upload Photo
    │
    ▼
┌─────────────────────────────────┐
│  1. Load at FULL resolution     │
│  2. Brightness + Contrast       │  ← Pixel-level Canvas API
│  3. Unsharp Mask (Sharpening)   │
│  4. Selective Skin Smoothing    │
│  5. Export as lossless PNG      │
└─────────────────────────────────┘
    │
    ▼
Download PNG (original resolution, zero compression loss)
```

### Edit Pipeline Details

| Step | Technique | Effect |
|------|-----------|--------|
| Brightness | Pixel offset based on avg luminance | Intelligent auto-level |
| Contrast | S-curve `(pixel - 128) × factor + 128` | Natural punch |
| Saturation | Luminance-based colour boost | Vivid but realistic |
| Sharpening | Unsharp mask (blur → difference → blend) | Crisp details |
| Skin Smooth | Selective blur on warm-tone pixels only | Natural skin, sharp edges |

---

## 🎨 Tech Stack

| Technology | Usage |
|---|---|
| **HTML5 Canvas API** | Full-resolution pixel processing |
| **CSS3** | Bokeh background, glassmorphism, animations |
| **Vanilla JavaScript** | Image pipeline, download trigger |
| **Google Fonts** | Playfair Display + Outfit |

---

## 📦 Deployment

### GitHub Pages (Free Hosting)

```bash
# 1. Create a new GitHub repo named "kslab"
# 2. Clone it
git clone https://github.com/<your-username>/kslab.git
cd kslab

# 3. Add the files
cp /path/to/index.html .
cp /path/to/README.md .

# 4. Push
git add .
git commit -m "🌿 Initial release – KS LAB Natural Photo Editor"
git push origin main

# 5. Enable GitHub Pages in repo Settings → Pages → main branch
```

---

## 📸 Screenshot

```
┌────────────────────────────────────────┐
│  🌿 KS LAB          Natural Photo Editor│
├────────────────────────────────────────┤
│                                        │
│           🐒  (monkey mascot)          │
│                                        │
│  ┌──────────────────────────────────┐  │
│  │   Drop your photo here           │  │
│  │                                  │  │
│  │      [ ⬆ Choose Photo ]          │  │
│  └──────────────────────────────────┘  │
│                                        │
└────────────────────────────────────────┘
```

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

<p align="center">Made with 💚 by <strong>KS LAB</strong></p>
