# OCR Reader Agent

**OCR Reader Agent** (powered by gImageReader) is an advanced, cross-platform graphical frontend for the **Tesseract OCR** engine. It provides an intuitive interface for capturing, processing, recognizing, editing, and exporting text from images and multi-page PDF documents.

---

## 🌟 Key Features

- 📥 **Comprehensive Media Import**
  - Import images (PNG, JPEG, TIFF, BMP, DjVu) and multi-page PDF documents.
  - Direct acquisition from scanning devices via **SANE** (Linux) and **TWAIN** (Windows).
  - Instant paste from system clipboard and live desktop screenshot capture.

- 🎯 **Advanced Recognition & Layout Analysis**
  - Automatic layout detection for complex document structures.
  - Manual definition and fine-tuning of recognition regions and text blocks.
  - Batch recognition across multiple files and pages simultaneously.

- 🔤 **Tesseract OCR Integration**
  - Full support for Tesseract 3.x, 4.x, and 5.x recognition models.
  - Multi-language recognition capability with downloadable language data packs.
  - Output to plain text or structured layout format (**hOCR**).

- ✏️ **Interactive Post-Processing & Editing**
  - Side-by-side view comparing input document visuals directly with recognized text.
  - Built-in real-time spell checking powered by **Enchant** / **Hunspell**.
  - Search and replace, text strip formatting, and character replacement rules.

- 📄 **Export & Document Generation**
  - Export to Plain Text (`.txt`), hOCR (`.html`), or generate **searchable PDF** files with embedded invisible text layers.

- 🖥️ **Dual GUI Support**
  - Native user interface backends for both **Qt** (Qt5 / Qt6) and **GTK3**.

---

## 🏗 Project Architecture

```
OCR-Reader-Agent/
├── CMakeLists.txt        # Primary CMake configuration and dependency resolution
├── common/               # Core OCR engine abstractions, paper sizes, and CCITT encoding
├── gtk/                  # GTK3 graphical interface implementation
├── qt/                   # Qt5 / Qt6 graphical interface implementation
├── data/                 # Icons, desktop entries, appdata, and UI resources
├── docs/                 # User documentation & manual source files
├── packaging/            # Build specs for Linux distributions and Windows installers
└── po/                   # Gettext translation catalogs
```

---

## 🛠 Prerequisites & Dependencies

To build OCR Reader Agent from source, ensure the following tools and libraries are installed:

### Build Tools
- **C++ Compiler** with C++17 support (`gcc`, `clang`, or `MSVC`)
- **CMake** (>= 3.10)
- **PkgConfig** & **Gettext**

### Core Libraries
- **Tesseract OCR** (`libtesseract`)
- **PoDoFo** (`libpodofo`) — for PDF processing
- **DjVuLibre** (`ddjvuapi`) — for DjVu image support
- **Enchant** (`libenchant-2`) — for spell checking
- **SANE** (`sane-backends`) — for scanner support (Linux/Unix)

### GUI Frameworks (Choose one or both)
- **Qt6** / **Qt5** (`qtbase`, `qtimageformats`)
- **GTK3** (`gtkmm-3.0`)

---

## 🚀 Building from Source

### 1. Clone the Repository

```bash
git clone https://github.com/anjaneyulukampalla04-pixel/OCR-Reader-Agent-.git
cd OCR-Reader-Agent-
```

### 2. Configure & Build

#### Build Qt Interface (Default: Qt6)
```bash
mkdir build && cd build
cmake -DINTERFACE_TYPE=qt6 ..
make -j$(nproc)
sudo make install
```

#### Build GTK3 Interface
```bash
mkdir build && cd build
cmake -DINTERFACE_TYPE=gtk ..
make -j$(nproc)
sudo make install
```

---

## 🤝 Contributing

Contributions, bug reports, and feature requests are welcome! Feel free to check out the [issues](https://github.com/anjaneyulukampalla04-pixel/OCR-Reader-Agent-/issues) page.

---

## 📜 License

This project is licensed under the **GNU General Public License v3.0** (GPLv3). See the [COPYING](COPYING) file for full license text.
