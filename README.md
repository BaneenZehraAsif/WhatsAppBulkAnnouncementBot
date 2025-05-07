
# 📣 WhatsApp Bulk Announcement Bot – by Baneen Zehra Asif

[![MIT License](https://img.shields.io/badge/license-MIT-green)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/python-3.x-blue)](https://www.python.org/)
[![Repo Size](https://img.shields.io/github/repo-size/BaneenZehraAsif/whatsapp-bulk-announcement-bot?color=purple)](https://github.com/BaneenZehraAsif/whatsapp-bulk-announcement-bot)
[![Stars](https://img.shields.io/github/stars/BaneenZehraAsif/whatsapp-bulk-announcement-bot?style=social)](https://github.com/BaneenZehraAsif/whatsapp-bulk-announcement-bot/stargazers)
[![Forks](https://img.shields.io/github/forks/BaneenZehraAsif/whatsapp-bulk-announcement-bot?style=social)](https://github.com/BaneenZehraAsif/whatsapp-bulk-announcement-bot/network/members)

---

## 🌐 Overview

> **WhatsApp Bulk Announcement Bot** is a powerful Python automation tool crafted by **Baneen Zehra Asif** to broadcast personalized messages via WhatsApp. Ideal for community managers, educators, and marketers, it simplifies bulk messaging using an Excel sheet and the `pywhatkit` library.

---

## ✨ Features

- 📋 **Excel Integration** – Load contacts from a `contacts.xlsx` file  
- 💬 **Bulk Messaging** – Send customized messages to each contact  
- ⚙️ **Real-Time Sending** – Powered by `pywhatkit.sendwhatmsg_instantly()`  
- 🕒 **Spam-Safe Delay** – 5-second interval between each message  
- 🖊 **Customizable Format** – Modify message text and links  
- 🔧 **Lightweight Setup** – Minimal dependencies, quick start  

---

## 📦 Requirements

- ✅ Python 3.x  
- ✅ `pywhatkit`, `pandas`, `openpyxl`  
- ✅ A structured Excel file with a column named `PhoneNumbers`  

**Install dependencies:**
```bash
pip install pywhatkit pandas openpyxl
````

---

## 🧾 Project Structure

```
📂 WhatsApp-Bulk-Announcement-Bot/
├── contacts.xlsx                      # 📇 Contact list
├── send_bulk_whatsapp.py             # 🧠 Main script
├── requirements.txt                  # 📜 Dependencies
├── WhatsApp_Bulk_Announcement_Bot.ipynb  # 📘 Jupyter Notebook version
└── README.md                         # 📄 Project documentation
```

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/BaneenZehraAsif/whatsapp-bulk-announcement-bot.git
cd whatsapp-bulk-announcement-bot
```

### 2️⃣ Prepare the Excel File

* Ensure the file is named: `contacts.xlsx`
* Add a column: `PhoneNumbers` with values like `923001234567` (no `+` sign)

### 3️⃣ Customize the Script

* Open `send_bulk_whatsapp.py` or the notebook
* Modify the `message` or `link` as needed

### 4️⃣ Run the Bot

```bash
python send_bulk_whatsapp.py
```

---

## 🧠 Sample Code

```python
import pywhatkit as kit
import pandas as pd
import time

df = pd.read_excel("contacts.xlsx")
link = "https://github.com/BaneenZehraAsif"

for index, row in df.iterrows():
    phone_number = f"+{row['PhoneNumbers']}"
    message = f"""📢📢 Welcome! Join now to stay updated on new data science projects.
    Join now: {link}"""

    try:
        kit.sendwhatmsg_instantly(phone_number, message, wait_time=5)
        print(f"✅ Message sent to {phone_number}")
        time.sleep(5)
    except Exception as e:
        print(f"❌ Failed to send message to {phone_number}: {e}")
```

---

## 🤝 Contribution Guidelines

Contributions are warmly welcomed!
If you’d like to suggest improvements or fixes:

1. Fork the repo
2. Create a new branch
3. Submit a pull request ✨

---

## 📄 License

This project is licensed under the **MIT License**.
See the [LICENSE](LICENSE) file for full details.

---

## 👩‍💻 Author

**Baneen Zehra Asif**
🔗 [GitHub Profile](https://github.com/BaneenZehraAsif)

```

