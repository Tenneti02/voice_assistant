# 🌙 Meet Twilight Assistant  

Hey there! 👋 Meet **Twilight Assistant**, your AI-powered buddy that can respond to both voice and text commands. Whether you're chatting with it or giving voice commands, Twilight is here to help! It can detect wake words, perform tasks, and keep up with conversations, all thanks to **Ollama**, **pyttsx3**, and **speech recognition**.  

🚀 **Let’s get it up and running!**  



## 🛠️ Setting Things Up  

Getting Twilight Assistant ready won’t take long! Follow these simple steps.  

### 🔹 1. Set Up Your Python Environment  

To keep things organized, let’s create a **virtual environment** in VS Code.  

1. Open your project folder in **VS Code**.  
2. Hit `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) to open the Command Palette.  
3. Search for **"Python: Create Environment"** and select it.  
4. Choose **"Venv"** (or **"Virtualenv"**).  
5. Pick the Python version (Python 3.9+ is recommended).  
6. VS Code should automatically activate the environment. If it doesn’t, manually select the `.venv` interpreter from the Command Palette.  

---

### 🔹 2. Install Llama 3 via Ollama  

💡 **Why?** Twilight Assistant needs Llama 3 to process your queries.  

1. Install **Ollama** from [here](https://ollama.ai/).  
2. Open your terminal and type:  

   ```bash
   ollama pull llama3
   ```

---

### 🔹 3. Enable Wake Word Detection with Picovoice  

Twilight Assistant listens for a wake word (like “Twilight”) before responding. To set that up:  

1. Go to the [Picovoice Console](https://console.picovoice.ai/) and sign in.  
2. Head over to **Porcupine** (Picovoice’s wake word engine).  
3. Create a new wake word model (e.g., **"Twilight"**).  
4. Download the `.ppn` file and place it in your project directory.  

---

### 🔹 4. Adjust the Settings in Your Python Code  

Now, let’s tweak the assistant’s settings to match your setup.  

1. Create a file called **`assistant.py`** in your project folder.  
2. Update the following variables in the script:  
   - `MODEL_PATH = "twilight_en_windows_v3_0_0.ppn"` (Path to your wake word file)  
   - `access_key = "<Your Picovoice Access Key>"`  
   - `model = "llama3"` (This should match your Ollama model name)  

---

### 🔹 5. Install the Required Libraries  

Twilight Assistant relies on a few Python packages to work. Install them with:  

```bash
pip install pyttsx3 speech_recognition pyaudio pvporcupine langchain langchain_ollama
```

⚠️ **Having trouble installing PyAudio?** Check its documentation for platform-specific fixes.  

---

### 🔹 6. Run Twilight Assistant  

Alright, time to fire it up! 🚀  

1. **Start Ollama** (this keeps the AI model running):  

   ```bash
   ollama run llama3
   ```

2. **Run Twilight Assistant** in a separate terminal:  

   ```bash
   python assistant.py
   ```

---

## 🎙️ How to Use Twilight Assistant  

Twilight works in **two modes**—pick the one that suits you!  

### ✨ **Text Mode**  
👨‍💻 Prefer typing?  

1. Type `text` and hit **Enter**.  
2. Ask a question or type a command.  
3. The assistant will respond instantly!  
4. Type `exit` when you're done.  

### 🎤 **Voice Mode**  
🎙️ Want a hands-free experience?  

1. Say **"Twilight"** (or your custom wake word).  
2. Speak your command clearly.  
3. Twilight will **talk back** and display responses on-screen.  
4. To stop, just say **"exit"** after the wake word.  

---

## 🛠️ Troubleshooting  

### ❓ **Not getting responses?**  
✅ Make sure all libraries are installed (`pip install ...`).  
✅ Restart your terminal and try running `python assistant.py` again.  

### 🔊 **Wake word not working?**  
✔️ Double-check your **Picovoice Access Key**.  
✔️ Ensure the **Porcupine model file** (`.ppn`) is in the correct directory.  

---

## 🎉 Enjoy Using Twilight Assistant!  

Now you’re all set! Have fun chatting with Twilight—whether by voice or text. If you run into any issues, check out the [Picovoice Docs](https://picovoice.ai/docs/) or [Ollama Docs](https://ollama.ai/).  

