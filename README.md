# Twilight  Assistant

**Twilight Assistant** is a Python-based voice and text assistant powered by **Ollama**, **pyttsx3**, and **speech recognition**. It supports wake word detection, file operations, and dialog state tracking. You can interact with it via voice commands or text input. To get started, you'll need to set up model file paths and obtain a Picovoice access key.
---
## Setup and Installation

Follow these steps to set up and run the Twilight Assistant on your system.

### 1. Create a Python Environment in VS Code

1. Open your project folder in VS Code.
2. Open the Command Palette (`Ctrl+Shift+P` or `Cmd+Shift+P`).
3. Search for **"Python: Create Environment"** and select it.
4. Choose **"Venv"** (or **"Virtualenv"** if preferred).
5. Select the Python interpreter for your project. VS Code will create a virtual environment (usually in a `.venv` folder).
6. Activate the environment: VS Code should do this automatically. Check the bottom-left corner of the window to confirm (e.g., `(.venv) Python 3.9.x`). If not, use the Command Palette to select the `.venv` interpreter.

---

### 2. Install Llama 3 via Ollama

1. Install **Ollama** by following the instructions on the [Ollama website](https://ollama.ai/).
2. Open your terminal and run the following command to download the Llama 3 model:

   ```bash
   ollama pull llama3
   ```

---

### 3. Set Up Picovoice for Wake Word Detection

1. Go to the [Picovoice Console](https://console.picovoice.ai/) and create an account or log in.
2. Navigate to the **Porcupine** section.
3. Create and train a wake word model (e.g., name it **"Twilight"**).
4. Download the trained model (`.ppn` file) and place it in your project directory.

---

### 4. Configure the Python Code

1. Create a Python file (e.g., `assistant.py`) in your project directory.
2. Paste the provided code into `assistant.py`.
3. Update the following in the code:
   - `MODEL_PATH`: Path to your Porcupine model file (e.g., `"twilight_en_windows_v3_0_0.ppn"`).
   - `KEYWORD_PATH`: Same as `MODEL_PATH`.
   - `access_key`: Replace with your Picovoice access key (found in the Picovoice Console).
   - `model`: Ensure this matches the model name you used in Ollama (default is `llama3`).
---
### 5. Install Required Libraries

Install the necessary Python libraries using `pip`:

```bash
pip install pyttsx3 speech_recognition pyaudio pvporcupine langchain langchain_ollama
```

If you encounter issues with **PyAudio**, refer to its documentation for additional system dependencies.

---

### 6. Run the Assistant

1. Open a terminal and activate your Python environment.
2. Start Ollama:

   ```bash
   ollama run llama3
   ```

3. In a separate terminal (with the environment activated), run the assistant:

   ```bash
   python assistant.py
   ```

4. Choose your interaction mode:
   - **Text Mode**: Type `text` and press Enter. Type your messages to interact with the assistant.
   - **Voice Mode**: Type `voice` and press Enter. The assistant will listen for the wake word and respond to your voice commands.
---
## Interacting with the Assistant
### Text Mode
1. Type your message at the `You:` prompt and press Enter.
2. The assistant's response will appear under `Twilight:`.
3. To exit, type `exit` and press Enter.
### Voice Mode
1. The assistant listens for the wake word (e.g., "Twilight").
2. Once detected, speak your command clearly.
3. The assistant will respond verbally (if configured) and display the response in the terminal.
4. To exit, say **"exit"** after the wake word.
- Ensure all required libraries are installed. Use `pip` if any are missing.
- If wake word detection isn’t working, double-check your Picovoice configuration and model training.
- Replace placeholders like `<Your Picovoice Access Key>` with your actual values.
- The Porcupine model file (`.ppn`) should be in the same directory as your script unless specified otherwise.

---

Enjoy using **Twilight Assistant**! For any issues, refer to the documentation or reach out for support.
