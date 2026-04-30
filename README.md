# 📄 Origami

**Origami** is a professional-grade, high-performance document scanner and PDF utility application. Designed with a focus on **Premium UX**, **Glassmorphic Aesthetics**, and **Efficiency**, Origami provides a seamless experience for digitizing documents, managing PDFs, and performing advanced image processing on mobile devices.

<div align="center" style="display: flex; gap: 10px; justify-content: center;">
  <img src="https://github.com/user-attachments/assets/572759de-47f1-4749-b784-1119896da7bf" width="30%" height="400"/>
  <img src="https://github.com/user-attachments/assets/82cf8cec-df17-4a5b-9dea-12aa7c1172e7" width="30%" height="500"/>
  <img src="https://github.com/user-attachments/assets/ca26a261-4960-49ae-9d6b-553888c05bdb" width="30%" height="400"/>
</div>

---

## 🎨 Design Philosophy: "The Pro Experience"
Origami isn't just a tool; it's a statement. The application utilizes:
- **Glassmorphism:** Frosted glass effects and vibrant gradients for a modern, airy feel.
- **Micro-Animations:** Powered by `framer-motion` for fluid view transitions and interactive feedback.
- **Contextual UI:** Adaptive interfaces that change based on the document type and processing state.
- **Zero-Placeholder Policy:** Every element is functional and visually polished from the first launch.

---

## 🛠️ Core Technology Stack

### **Frontend & Mobile**
- **React 19:** The backbone of the application's reactive UI.
- **Vite:** Next-generation frontend tooling for blazing-fast development and builds.
- **Capacitor 8:** Providing native bridge capabilities to access device hardware (Camera, Filesystem, Share).
- **Framer Motion 12:** Delivering high-end animations and layout transitions.

### **Document & Image Processing**
- **OpenCV.js:** Used for real-time edge detection and perspective warping (Auto-crop functionality).
- **Tesseract.js:** Integrated OCR (Optical Character Recognition) engine used to extract text from document images during PDF to Word conversion.
- **jsPDF & pdf-lib:** Industrial-strength PDF generation and manipulation.
- **Docx:** Enabling the creation of structured Word documents from extracted OCR text.
- **PDF.js:** High-fidelity PDF rendering for previews and page manipulation.

---

## 🚀 Key Features

### **1. Professional Document Scanner**
- **Native Camera Integration:** High-resolution capture via `@capacitor-community/camera-preview`.
- **Intelligent Edge Detection:** Automatic document boundary identification using OpenCV.
- **Perspective Warping:** Rectify skewed images into perfectly flat document pages.
- **Batch Scanning:** Capture multiple pages in a single session with rapid-fire capability.
- **Image Enhancement:** Real-time filters (B&W, Grayscale, Magic Color) and manual adjustments (Brightness, Contrast, Saturation).

### **2. Advanced PDF Suite**
- **Merge & Split:** Combine multiple documents or extract specific pages with ease.
- **Smart Compression:** Reduce file size for easy sharing while maintaining readability.
- **Watermarking:** Add custom text overlays to protect your documents.
- **Reordering:** Drag-and-drop page organization.
- **Format Conversion:** Convert PDFs to high-quality JPGs or editable Word documents.

### **3. Zero-Processing Memory Architecture**
To ensure stability on devices with limited RAM (4GB or less), Origami implements:
- **Disk-Based Thumbs:** High-resolution images are stored in the native cache immediately.
- **Memory Eviction:** Only the active page's thumbnail is kept in RAM; others are loaded on-demand from the filesystem.
- **Asynchronous Processing:** Heavy PDF generation occurs in chunks to prevent UI blocking.

---

## 📂 Project Structure

```text
origami/
├── android/               # Native Android project files (Capacitor)
├── assets/                # Global static assets and splash screens
├── src/
│   ├── components/        # UI Components
│   │   ├── tools/         # Individual PDF utility views (Merge, Split, etc.)
│   │   ├── Scanner.jsx    # OpenCV-powered camera interface
│   │   ├── Editor.jsx     # Post-scan refinement and filtering
│   │   └── Home.jsx       # Document dashboard and tool gallery
│   ├── services/          # Core logic engines
│   │   └── ImageProcessor.js # OpenCV edge detection & warping logic
│   ├── utils/             # Helper functions
│   │   ├── pdfUtils.js    # PDF generation, saving, and sharing
│   │   └── fileUtils.js   # Native filesystem interactions
│   ├── App.jsx            # Main application controller & state
│   └── index.css          # Global design system (Glassmorphism)
└── capacitor.config.json  # Native bridge configuration
```

---

## ⚡ Installation & Development

### **Prerequisites**
- Node.js (Latest LTS)
- Android Studio (for native builds)
- Capacitor CLI

### **Setup**
1. **Install dependencies:**
   ```bash
   npm install
   ```
2. **Run in development mode:**
   ```bash
   npm run dev
   ```
3. **Build for Android:**
   ```bash
   npm run build
   │ npx cap sync android
   │ npx cap open android
   ```

---

## 🛡️ Privacy & Security
Origami processes all documents **locally on the device**. No data is ever uploaded to a server, ensuring 100% privacy for sensitive documents.

---

## 👨‍💻 Developer
Developed with ❤️ for the community.
