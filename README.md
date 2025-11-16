# **HistoWiz — Interactive Histogram Transfer & Curve Mapping Tool**

**Live demo:**
👉 [https://histowiz.smb-h.com](https://histowiz.smb-h.com)

HistoWiz is a modern, client-side tool for **interactive image tone-mapping, histogram manipulation, and transfer-curve editing**.
It runs **entirely in your browser**, with **no server**, enables real-time adjustments, and provides advanced controls such as LUT editing, histogram equalization, and draggable transfer points.

---

## 🚀 Features

### ✅ **Client-Side Only**

* All processing happens **in-browser** via the HTML5 Canvas API.
* No uploads, no backend, fully private.

### 🎨 **Interactive Curve Editor**

* Draggable SVG transfer-curve points.
* Add/remove control points.
* Enforces monotonic mapping.
* Display of (input → output) intensity mapping.

### 🖼️ **Real-Time Image Mapping**

* Apply tone-mapping & LUT transformations immediately.
* Auto-equalize with one click.
* Reset to identity curve.

### 📊 **Histogram Preview**

* Live histogram visualization.
* Shows distribution after mapping.

### 💾 **Export & Save**

* Download transformed image as PNG.
* Works fully offline.

---

## 📦 Installation / Usage

No installation required — it’s a static web app.

### **Clone the repo**

```bash
git clone https://github.com/<your-username>/histowiz.git
cd histowiz
```

### **Serve locally**

You can run it from any static server, e.g.:

```bash
python3 -m http.server 8080
```

Then open:
`http://localhost:8080`

---

## 🧱 Project Structure

```
/histowiz
 ├── index.html        # Main application UI
 ├── favicon.png       # Logo
 ├── assets/           # (optional) Additional icons/images
 ├── README.md         # Documentation
```

Everything is bundled into `index.html` for simplest deployment.

---

## 🛠️ Technology

* **HTML5 Canvas** for image processing
* **SVG** for draggable curve editor
* **Vanilla JS** (no frameworks)
* **CSS Grid & Flexbox** for responsive UI

---

## 📘 How It Works

### 1. Load image → store in canvas

Image is scaled to canvas size; original pixel data is cached.

### 2. Transfer curve → generates 256-entry LUT

Curve points (0–1 range) are piecewise-interpolated to build the lookup table.

### 3. Apply LUT → pixel-wise transform

Each pixel intensity is remapped through the LUT in real-time.

### 4. Histogram → computed on the fly

Displayed below the curve editor.

---

## 🔧 Roadmap (Optional)

* ☐ Multi-channel (RGB-separate) curves
* ☐ Upload/download LUT files
* ☐ GPU acceleration (WebGL)
* ☐ Full theme customization

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 👤 Author

**SMB H**
[https://smb-h.com](https://smb-h.com)
