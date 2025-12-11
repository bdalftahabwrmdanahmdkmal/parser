# 📚 EPUB Parser
This is a fully client-side EPUB parsing tool built with **HTML, JavaScript, and JSZip**.
It allows users to upload an EPUB file, automatically remove all occurrences of **“OceanofPDF.com”**, and download a cleaned version — all without uploading anything to a server.

✔ No server required
✔ 100% privacy — processing happens in the browser
✔ Dark mode
✔ Drag-and-drop support
✔ Progress bar
✔ Automatic filename cleanup

---

## 🚀 Features

### 👜 **Drag & Drop EPUB Upload**

Just drop the file on the upload zone or click to browse.

### ✂️ **Automatic Removal of “OceanofPDF.com”**

The script scans all EPUB contents and removes every match of:

```
OceanofPDF.com
```

### 📦 Built with JSZip

Reads, modifies, and re-packages EPUB files directly in the browser.

### 🌙 **Dark Mode**

One-click toggle to switch between light and dark themes.

### 📊 **Progress Indicator**

Shows real-time progress while processing large EPUB files.

### 🔒 100% Client-Side

Your EPUB never leaves your device.

---

## 🧠 How It Works

1. User uploads an EPUB file.
2. JSZip loads the EPUB archive.
3. For each file in the EPUB:

   * If it’s **text/XML/HTML**, occurrences of `OceanofPDF.com` are removed.
   * If it’s **image or binary**, it is preserved as-is.
4. JSZip regenerates a cleaned EPUB file.
5. The browser automatically downloads the sanitized result.

---

## 📂 File Types Processed

| Type                                              | Action              |
| ------------------------------------------------- | ------------------- |
| `.html`, `.xhtml`, `.opf`, `.xml`, `.css`, `.txt` | Text search/replace |
| `.jpg`, `.png`, `.svg`, `.gif`                    | Copied unchanged    |
| Directories                                       | Ignored/skipped     |

---

## 📥 Usage

Open the HTML file in your browser:

```
index.html
```

Then:

1. Drag an EPUB file into the drop zone
2. Wait for processing
3. Download the cleaned EPUB

---

## 🧪 Regex-Based Filename Cleaning

The parser attempts to restore the original EPUB filename using:

```js
/_OceanofPDF\.com(.+)_-_.+\.epub$/
```

If the pattern is detected, it extracts the true book name.

---

## 🧱 Code Overview

### Key Components:

* **EPUB Upload Handler**
* **JSZip File Parsing**
* **Content Sanitization**
* **Progress Tracking**
* **Dark Mode Toggle**
* **Clean Filename Extraction**

---

## 🧩 Technologies Used

* **HTML5 / CSS3**
* **Vanilla JavaScript**
* **JSZip 3.7.1**

CDN:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/jszip/3.7.1/jszip.min.js"></script>
```
