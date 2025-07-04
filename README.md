# Keylogger Project (Educational Use Only)

## 📌 Description
A simple educational keylogger written in Python that records keystrokes with timestamps and optionally sends the logs via email. This project is designed to help beginners understand input monitoring, file handling, and email automation in Python.

> ⚠️ **Ethical Notice:**
> This project is strictly for **educational and ethical use only**. Never use this tool without **explicit permission** from the system owner. Unauthorized use is illegal and unethical.

---

## 📦 Project Structure:
```
Keylogger-Project/
├── keylogger.py          # Captures and logs keystrokes with timestamps
├── send_keylog.py        # Sends the log file via email
├── keylog.txt            # Stores captured keystrokes
└── README.md             # Project documentation
```

---

## 🚀 How to Set Up and Use

### 1. Requirements
- Python 3.x
- Required libraries:
  ```bash
  pip install pynput
  ```

### 2. Run the Keylogger
```bash
python keylogger.py
```
- Press **ESC** to stop logging.
- Keystrokes are saved in `keylog.txt`.

### 3. Send the Log File by Email
1. Enable **2-Step Verification** on your Gmail account.
2. Generate an **App Password** from: [https://myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords)
3. Replace placeholders in `send_keylog.py` with your email and app password.
4. Run:
```bash
python send_keylog.py
```

---

## 🔑 Features
- Logs every key pressed
- Adds timestamps to each key press
- Saves logs to a `.txt` file
- Sends logs to any email address via secure SMTP

---

## ✅ To-Do Ideas for Enhancement
- Automatically email logs every X minutes
- Capture clipboard contents
- Stealth mode execution

---

## 🛡 Legal Disclaimer
This project is intended solely for **ethical learning purposes**. Unauthorized access, surveillance, or monitoring without consent is strictly forbidden and may violate local and international laws.

Always get **explicit permission** before deploying or using this tool.

---

Made with ❤️ for educational cybersecurity practice.

