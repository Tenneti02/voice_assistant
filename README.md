

# 🌙 Twilight Assistant  

Meet **Twilight Assistant**, your AI-powered voice and text assistant! 🚀 Whether you prefer speaking or typing, Twilight is here to assist you with smart voice recognition, wake word detection, and seamless interactions.  

🎤 **Say the wake word and let the magic happen!**  

---

## 🛠️ Getting Started  

Setting up **Twilight Assistant** is easy! Follow these steps to get it up and running.  

### 🔹 1. Create a Python Environment in VS Code  

📌 **Why?** A virtual environment keeps dependencies organized and avoids conflicts.  

1. Open your **project folder** in VS Code.  
2. Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) to open the Command Palette.  
3. Search for **"Python: Create Environment"** and select it.  
4. Choose **"Venv"** (or **"Virtualenv"**).  
5. Select the **Python interpreter** (recommended: Python 3.9+).  
6. Activate the environment: Look for `(.venv)` in the bottom-left corner of VS Code. If missing, manually activate it via the Command Palette.  

---

### 🔹 2. Install Llama 3 via Ollama  

📌 **Why?** Llama 3 is the brain behind Twilight Assistant’s AI responses!  

1. Install **Ollama** from [here](https://ollama.ai/).  
2. Open your terminal and download the Llama 3 model:  

   ```bash
   ollama pull llama3
   ```

---

### 🔹 3. Set Up Picovoice for Wake Word Detection  

📌 **Why?** Picovoice lets Twilight Assistant listen for its wake word.  

1. Sign up or log in to the [Picovoice Console](https://console.picovoice.ai/).  
2. Head to the **Porcupine** section.  
3. Create a wake word (e.g., `"Twilight"`).  
4. Download the trained model (`.ppn` file) and place it in your project folder.  

---

### 🔹 4. Configure the Python Code  

📌 **Why?** Customizing these settings makes the assistant work as expected.  

1. Create `assistant.py` in your project directory.  
2. Update the following in your script:  
   - `MODEL_PATH = "twilight_en_windows_v3_0_0.ppn"` (Path to your wake word model)  
   - `access_key = "<Your Picovoice Access Key>"`  
   - `model = "llama3"` (Matches your downloaded Ollama model)  

---

### 🔹 5. Install Required Dependencies  

📌 **Why?** These libraries make Twilight Assistant function smoothly.  

Run the following command:  

```bash
pip install pyttsx3 speech_recognition pyaudio pvporcupine langchain langchain_ollama
```

⚠️ **Troubleshooting PyAudio?** If installation fails, check its documentation for system-specific fixes.  

---

### 🔹 6. Run the Assistant  

📌 **You're all set! Now, let's bring Twilight Assistant to life.**  

1. **Start Ollama** (AI model server):  

   ```bash
   ollama run llama3
   ```

2. **Run Twilight Assistant** in a separate terminal:  

   ```bash
   python assistant.py
   ```

---

## 🎙️ How to Use Twilight Assistant  

Twilight Assistant works in **two modes**:  

### ✨ **Text Mode**  
💬 Prefer typing? No problem!  

1. Type `text` and press **Enter**.  
2. Type your query when prompted.  
3. Get an instant AI-powered response!  
4. Type `exit` to quit.  

### 🎤 **Voice Mode**  
🎙️ Want to go hands-free? Just say **"Twilight"** and speak!  

1. The assistant listens for the wake word.  
2. Once detected, speak clearly.  
3. Twilight will respond with both **text and speech**.  
4. To stop, say **"exit"** after the wake word.  

---

## 🛠️ Troubleshooting  

### ❓ **Not getting responses?**  
✅ Ensure all required libraries are installed (`pip install ...`).  
✅ Restart the terminal and re-run `python assistant.py`.  

### 🔊 **Wake word not working?**  
✔️ Double-check your **Picovoice Access Key**.  
✔️ Make sure the **Porcupine model file** (`.ppn`) is in the correct directory.  

---

## 🎉 Enjoy Using Twilight Assistant!  

🚀 Whether you're chatting via text or voice, **Twilight Assistant** is here to assist you!  

Need help? Check the [Picovoice Docs](https://picovoice.ai/docs/) or [Ollama Docs](https://ollama.ai/).  

