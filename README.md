# Keylogger Project (Educational Use Only)

## 📌 Description  
A simple educational keylogger written in Python that records keystrokes with timestamps and optionally sends the logs via email. This project is designed to help beginners understand input monitoring, file handling, and email automation in Python.

> ⚠️ **Ethical Notice:**  
> This project is strictly for **educational and ethical use only**. Never use this tool without **explicit permission** from the system owner. Unauthorized use is illegal and unethical.

---

## 📦 Project Structure  
Keylogger-Project/
├── keylogger.py # Captures and logs keystrokes with timestamps
├── send_keylog.py # Sends the log file via email (with optional auto-send)
├── clipboard_logger.py # Captures clipboard content periodically
├── keylog.txt # Stores captured keystrokes
├── README.md # Project documentation
├── INSTALL.md # Installation guide for dependencies
├── LICENSE # MIT License file
└── .gitignore # Git ignore rules

yaml
Copy
Edit

---

## 🚀 How to Set Up and Use

### 1. Requirements  
- Python 3.x  
- Required libraries:  
  ```bash
  pip install pynput pyperclip schedule
2. Run the Keylogger
bash
Copy
Edit
python keylogger.py
Press ESC to stop logging.

Keystrokes are saved in keylog.txt.

3. Automated Periodic Email Sending (New)
bash
Copy
Edit
python send_keylog.py
Sends keylog by email automatically every 10 minutes (adjustable).

4. Optional Clipboard Capture (New)
bash
Copy
Edit
python clipboard_logger.py
Captures clipboard text every 30 seconds and saves to keylog.txt.

🔑 Features
Logs every key pressed with timestamps

Saves logs to a .txt file

Sends logs to email automatically every X minutes

Captures clipboard content optionally

✅ To-Do Ideas for Enhancement
Stealth mode execution

GUI-based configuration

🛡 Legal Disclaimer
This project is intended solely for ethical learning purposes. Unauthorized access, surveillance, or monitoring without consent is strictly forbidden and may violate local and international laws.

Always get explicit permission before deploying or using this tool.

🗺 Project Roadmap
🎯 Phase 1: Core Functionality (Complete)
 Basic keylogging with pynput

 Timestamp logging

 Save logs to a text file

 Manual email sending of logs

🛠 Phase 2: Feature Enhancements (In Progress)
 Automated periodic email sending (every X minutes)

 Optional clipboard capture

 Cross-platform support improvements (Mac/Linux)

🚀 Phase 3: User Experience Improvements
 Add GUI for easier interaction (Tkinter or PyQt)

 Implement stealth mode (background execution)

 Configurable settings (log frequency, email setup)

🧩 Phase 4: Packaging & Deployment
 Convert script to standalone executable (.exe or .app)

 Add installer or one-click setup

 Document ethical guidelines clearly in app UI

📄 LICENSE (MIT License)
text
Copy
Edit
MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
📄 .gitignore
text
Copy
Edit
__pycache__/
*.pyc
*.log
keylog.txt
.env

Made with ❤️ for educational cybersecurity practice.


