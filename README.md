# 🤖 AI Chat Automation Bot (Gemini + PyAutoGUI)


## 📋 Overview
This project is an automated chat assistant that integrates **Python desktop automation** with **Google's Gemini AI**. 

Instead of relying on browser APIs (which are often restricted), this bot uses "Screen Scraping" techniques to interact with chat applications (like WhatsApp Web) exactly like a human would. It reads chat history visually, processes the context using a custom LLM persona, and types out a response automatically.

## ✨ Key Features
* **Computer Vision Simulation:** Uses `PyAutoGUI` to simulate mouse movements, clicks, and drag-selections.
* **Generative AI Integration:** Connects to `google.generativeai` (Gemini 1.5 Flash) to generate intelligent, context-aware responses.
* **Custom Persona Engine:** The bot is prompted to act as "Naruto," a coder from India who replies in a mix of Hindi and English with a witty, roasting style.
* **Chat History Analysis:** Reads previous conversation context to ensure replies are relevant to specific senders (e.g., "Rohan Das").

## 🛠️ Tech Stack
* **Language:** Python 3.x
* **Automation:** `PyAutoGUI` (Mouse/Keyboard control)
* **Clipboard Management:** `Pyperclip`
* **AI Model:** Google Gemini API (1.5 Flash)
* **OS Interaction:** `os`, `time`

## ⚙️ Installation

1.  **Clone the Repository**
    ```bash
    git clone [https://github.com/T786-eng/Ai-Autoreply-ChatBot]
   
    ```

2.  **Install Dependencies**
    ```bash
    pip install pyautogui pyperclip google-generativeai
    ```

3.  **Set up API Key**
    You need a Google Gemini API key. Set it as an environment variable:
    ```bash
    export GOOGLE_API_KEY="your_api_key_here"
    # Or for Windows PowerShell:
    # $env:GOOGLE_API_KEY="your_api_key_here"
    ```

## ⚠️ Configuration (Crucial Step)
**Note:** This script relies on screen coordinates (X, Y) which depend on your specific screen resolution and window placement. Before running, you must calibrate the coordinates in `main.py`:

1.  Open your chat application (e.g., WhatsApp Web) and place it on one side of the screen.
2.  Use the following Python snippet to find the coordinates of your *Chrome Icon*, *Text Selection Area*, and *Text Input Box*:
    ```python
    import pyautogui
    import time
    while True:
        print(pyautogui.position())
        time.sleep(1)
    ```
3.  Update lines `18`, `24`, `25`, `29`, and `48` in the script with your specific coordinates.

## 🚀 Usage
1.  Open the target chat application.
2.  Run the script:
    ```bash
    python main.py
    ```
3.  The bot will automatically:
    * Click the browser.
    * Select and copy the recent chat history.
    * Check if the last message belongs to the target sender.
    * Generate a "roast" response and send it.

## 🔮 Future Improvements
* **OCR Integration:** Replace drag-and-select with Optical Character Recognition (Tesseract) to read text without moving the mouse.
* **Dynamic Element Finding:** Use image recognition to find the "Send" button and "Input Box" regardless of screen resolution.

## 📄 License
This project is open-source.