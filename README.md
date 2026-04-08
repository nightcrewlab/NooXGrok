## 🎮 Support Development

This project is developed independently.  
If you'd like to support future updates and new features:

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Support-orange?style=for-the-badge&logo=buymeacoffee)](https://buymeacoffee.com/nooxrii)

Your support helps keep development going 🚀

## 📥 Download Latest Version
[![Download Latest](https://img.shields.io/github/v/release/nightcrewlab/NooXGrok?label=Download%20EXE&style=for-the-badge&color=orange)](https://github.com/nightcrewlab/NooXGrok/releases/latest)

# 🎙️ NooXGrok — Desktop Wrapper

`NooXGrok` is a lightweight Windows desktop wrapper for **Grok** (`https://grok.com/`) built with **PyQt6 + Qt WebEngine**.
It runs in the system tray, supports a global hotkey for show/hide, and can optionally start with Windows.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🪟 **Frameless Always-on-Top Window** | Clean borderless UI that stays on top |
| 🌐 **Embedded Grok Browser** | Uses Qt WebEngine to load `https://grok.com/` |
| 🧠 **Persistent Profile** | Stores WebEngine profile data under `grok_profile/` |
| ⌨️ **Global Hotkey** | Toggle show/hide with configurable hotkey (default: `<alt>+<space>`) |
| ⚙️ **Settings Dialog** | Change hotkey + toggle “start with Windows” |
| 📌 **System Tray Integration** | Tray menu: show/hide, settings, quit |
| 🚀 **Startup Registration** | Adds/removes itself from Windows startup (HKCU Run) |

---

## 🛠️ Running from Source (with Virtual Environment)

### Requirements

- Windows 10/11
- Python 3.10+

### Create & activate venv

PowerShell:

```bash
py -m venv .venv
.\.venv\Scripts\Activate.ps1
```

CMD:

```bash
py -m venv .venv
.\.venv\Scripts\activate.bat
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run

```bash
python main.py
```

---

## ⚙️ Configuration

At first run, the app creates files next to the executable/script:

- `config.json`: hotkey + startup setting
- `grok_profile/`: Qt WebEngine persistent profile storage

---

## 📦 Build executable (optional)

If you want to bundle as an `.exe`:

```bash
pip install pyinstaller
pyinstaller --noconsole --onefile --icon icon.ico main.py

```

or while in active venv;

```bash

pyinstaller nooxgrok.spec --clean

```

The output will be in `dist/`.

---

## 🤝 Contributing

Feel free to fork the project and open pull requests for features or bug fixes.

---

*Developed by NooXRii*
