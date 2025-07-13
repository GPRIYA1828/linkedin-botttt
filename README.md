# linkedin-botttt

# 📌 LinkedIn Bot Automation API

A **modular, stealth-enabled LinkedIn automation API** built with `FastAPI` and `Selenium` (`undetected_chromedriver`) to automate LinkedIn tasks like login, visiting profiles, sending connection requests, and messaging — while bypassing bot detection.

---

## 🚀 Features

- 🔐 Secure login using username and password
- 🧠 Maintains browser session across API requests
- 🕵️‍♂️ Uses stealth browser to bypass detection
- 🔍 Navigate to any LinkedIn profile via URL
- ✅ Detect if already connected
- 🤝 Send a connection request if not connected
- 💬 Send a first message if already connected
- ❌ Gracefully closes the browser session when done

---

## 🛠️ Tech Stack

- `Python 3.11+`
- `FastAPI` for building the API
- `Selenium` + `undetected-chromedriver` for browser automation
- `Uvicorn` for running the API server

---

## 📂 API Endpoints

| Method | Endpoint     | Description                          |
|--------|--------------|--------------------------------------|
| POST   | `/login`     | Logs into LinkedIn                   |
| POST   | `/connect`   | Visits profile and sends a request   |
| POST   | `/message`   | Sends a message if already connected |
| POST   | `/close`     | Ends the session                     |

---

## ⚙️ Setup Instructions

```bash
git clone https://github.com/Harini24-G/linkedinbot.git
cd linkedinbot

# Create and activate virtual environment
python -m venv venv
venv\Scripts\activate    # On Windows
# source venv/bin/activate  # On Mac/Linux

# Install dependencies
pip install -r requirements.txt

# Run the API
uvicorn linkedin_automation_service:app --reload
