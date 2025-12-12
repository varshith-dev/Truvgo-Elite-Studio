# Truvgo Studio Elite (VTXS)

[![Release](https://img.shields.io/github/v/release/varshith-dev/Truvgo-Elite-Studio?style=for-the-badge&color=blue)](https://github.com/varshith-dev/Truvgo-Elite-Studio/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%20(64%20bit)-blueviolet?style=for-the-badge&logo=windows)](https://github.com/varshith-dev/Truvgo-Elite-Studio/releases)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Built With](https://img.shields.io/badge/Built%20With-Python%20%2B%20Eel-yellow?style=for-the-badge&logo=python)](https://github.com/python-eel/Eel)

> **Development Reimagined.** A lightweight, desktop-based IDE for modern web workflows. Experience a VS Code-like environment without the browser overhead.

---

## ⚡ Overview

**Truvgo Studio Elite** (Internal Codename: *VTXS*) is a standalone desktop IDE tailored for web development. It bridges the gap between lightweight text editors and heavy IDEs.

Built using a hybrid **Python + Web stack**, it leverages **Eel** to interface a Python backend (for file I/O and terminal operations) with a modern HTML/JS frontend (for the UI and Ace Editor). It is packaged as a native Windows executable, offering a seamless "install-and-code" experience.

---

## 🚀 Key Features

### 🖥️ Professional Code Editor
* **Ace Editor Integration:** Full syntax highlighting for JS, CSS, HTML, and Python.
* **Dark Mode UI:** A custom-designed interface inspired by VS Code.
* **Smart History:** Undo/Redo (Ctrl+Z/Ctrl+Y) and Zoom controls.

### 🔥 Firebase Deployment
* **Integrated CLI:** Deploy your web apps directly to Firebase Hosting without opening a separate terminal.
* **Live Logs:** CLI output is piped directly into the application's log console.

### 🛡️ Local Version Control
* **Auto-Backup:** The `.vtxs_store` system automatically timestamps and backs up files on every save.
* **Safety Net:** Restore previous versions of your code instantly.

### 📂 Advanced File Management
* **Tree & Grid Views:** Toggle between a standard file tree and a visual grid for media.
* **System Operations:** Create, rename, delete, and move files using native Python OS calls.

---

## 🛠️ Tech Stack & Architecture

Truvgo Studio Elite uses a unique architecture to combine performance with flexibility.

| Component | Technology | Description |
| :--- | :--- | :--- |
| **Backend** | Python 3.x | Handles File I/O, OS operations, and Terminal commands. |
| **Frontend** | HTML5 / JS | UI rendering and Ace Editor logic. |
| **Bridge** | Eel | Communicates between Python (Backend) and JS (Frontend). |
| **Packaging** | PyInstaller | Compiles the engine into a frozen `.exe`. |
| **Installer** | Inno Setup | Creates the production `setup.exe` installer. |

### "Under the Hood" Fixes
* **Dynamic Port Binding:** Automatically finds an open port if `8000` is busy.
* **Path Resolution:** Uses `sys._MEIPASS` to correctly locate assets inside the compiled PyInstaller bundle.
* **Native Feel:** Blocks browser refresh keys (F5) to maintain application state.

---

## 📥 Installation

### For Users
1.  Go to the [**Releases Page**](https://github.com/varshith-dev/Truvgo-Elite-Studio/releases).
2.  Download the latest `TruvgoStudio_Setup.exe`.
3.  Run the installer and follow the on-screen instructions.

### For Developers (Running from Source)
If you want to contribute or modify the source code:

```bash
# Clone the repository
git clone [https://github.com/varshith-dev/Truvgo-Elite-Studio.git](https://github.com/varshith-dev/Truvgo-Elite-Studio.git)

# Navigate to directory
cd Truvgo-Elite-Studio

# Install dependencies
pip install eel pyinstaller

# Run the application
python main.py
