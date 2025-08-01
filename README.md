# 🔐 Secure Image Encryption
### Using Reverse Pixel Shifting and AES-based Symmetric Cryptography

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![GUI](https://img.shields.io/badge/GUI-Tkinter-orange)
![Encryption](https://img.shields.io/badge/Encryption-AES-green)
![Status](https://img.shields.io/badge/Status-Final%20Year%20Project-brightgreen)

---

## 📌 Project Overview

A secure, GUI-based image encryption system that combines **reverse pixel shifting** and **AES encryption** using `Fernet`. It includes drag-and-drop input, file integrity checks, entropy analysis, secure log viewing, and dark/light themes — perfect for secure transmission or academic use.

---

## 🚀 Features

| Feature               | Description |
|-----------------------|-------------|
| 🔄 Pixel Shifting     | Obfuscates image by reversing pixels |
| 🔐 AES Encryption     | Uses PIN-based key with Fernet (AES-CBC) |
| 🖼 Image Preview       | Shows image after decryption |
| 📊 Entropy Analytics  | Visual graph of entropy before/after |
| 📦 File Size Chart    | Compare original vs encrypted file size |
| 🌗 Light/Dark Mode    | Toggle themes using ttk |
| 📁 Drag & Drop        | Drop images directly into GUI |
| 🔑 PIN Strength Hint  | Shows strength of PIN entered |
| 🔍 SHA256 Hash Check  | Detects tampered or invalid files |
| 📜 Secure Log Viewer  | Login-protected CSV viewer |

---

## 🗂️ Folder Structure

```
image_encryption_project/
├── encryption.py
├── decryption.py
├── key_utils.py
├── pixel_shift.py
├── main_gui.py
├── .env                   # login credentials (ignored in Git)
├── logs/
│   └── activity_log.csv   # secure logs
├── requirements.txt
└── README.md
```

---

## ⚙️ How It Works

### 🔐 Encryption
1. Select or drag image → `.jpg`, `.png`, etc.
2. Pixels are reversed horizontally.
3. Enter PIN → used to create AES key.
4. Image is encrypted using `Fernet`.
5. `.enc` and `.meta` (hash) files are generated.
6. Charts show entropy and file size.

### 🔓 Decryption
1. Load `.enc` file + enter correct PIN.
2. Decrypt bytes using same Fernet key.
3. SHA256 of decrypted image is matched with `.meta`.
4. If match ✅ → reverse shift → preview image.
5. Charts show restored entropy and size.

---

## 📦 Setup Instructions

### 🧪 Install Dependencies

```bash
pip install -r requirements.txt
```

### ▶️ Run the GUI App

```bash
python main_gui.py
```

---

## 🔐 Log Access

- Logs are stored in: `logs/activity_log.csv`
- Viewing logs requires login.
- Credentials are stored in `.env` like:
  ```
  LOG_USERNAME=admin
  LOG_PASSWORD=1234
  ```

✅ Make sure `.env` is **NOT uploaded** to GitHub — add it to `.gitignore`.

---

## 📄 Requirements

- Python 3.9+
- `cryptography`
- `Pillow`
- `matplotlib`
- `python-dotenv`

---

## 🔍 Sample Use Case

> Srinivas encrypts his college ID image with PIN `Secure@123`.  
> Sends `.enc` and `.meta` via email.  
> Receiver opens in this app, enters the same PIN, and gets the original image.  
> If tampered or wrong PIN — a warning appears.

---

## 👨‍💻 Developed By

**Varigonda Lakshmi Srinivas**  
Final Year B.Tech Project  
🔗 [GitHub Profile](https://github.com/Srinivas-18)

---

## 🌟 If you found this useful, leave a ⭐ on GitHub!
