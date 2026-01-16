# 🤖 Auto Reply AI Chatbot

An intelligent, automated chatbot powered by Google Generative AI (Gemini) that analyzes chat history and generates witty, roasting responses in Hindi and English. Seamlessly integrates with WhatsApp Web via GUI automation for real-time interactions. 📱💬

## ✨ Features
- 🔍 **Real-Time Monitoring**: Continuously scans chat history for new messages.
- 😂 **Humorous Responses**: Delivers funny roasts as "Naruto," a coder from India, blending Hindi and English.
- 🖱️ **Automated Interactions**: Uses pyautogui for seamless GUI-based replying.
- 🔧 **Customizable**: Easily adjust sender detection and response logic.

## 📋 Prerequisites
- 🐍 Python 3.8 or higher
- 🔑 Google Generative AI API key (obtain from [Google AI Studio](https://makersuite.google.com/app/apikey))
- 🌐 Chrome browser with WhatsApp Web open and positioned correctly

## 🚀 Installation
1. 📦 Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
2. 🔧 Set your Google API key as an environment variable: `export GOOGLE_API_KEY=your_api_key_here` (or use a `.env` file with `python-dotenv`).

## 🎯 Usage
1. 📱 Open WhatsApp Web in Chrome and position the window as per the coordinates in `bot.py`.
2. ▶️ Run `python bot.py`.
3. 🤖 The bot will monitor for new messages from the specified sender and auto-reply.

## ⚙️ Configuration
- 📍 Adjust coordinates in `bot.py` for your screen setup.
- 👤 Modify the sender name in `is_last_message_from_sender()` if needed.

## ⚠️ Disclaimer
This tool uses GUI automation, which may violate terms of service or be unethical. Use responsibly and at your own risk. Ensure compliance with platform policies. 🛡️