# Voice-Controlled AI Assistant (Jarvis)

A Python-based voice assistant that listens for commands, responds with text-to-speech, and automates common tasks like web searches, system control, messaging, weather updates, and calendar reminders. It also supports an AI chat mode using Google Gemini.

## Features
- **Voice interaction & AI chat** (speech recognition + Gemini AI responses)
- **Web & search** (Google, YouTube, Google Maps directions)
- **System control** (open/close apps, shutdown/restart/sleep, task manager)
- **Messaging & email** (Messenger/WhatsApp automation, Gmail checks)
- **Brightness control** (screen brightness adjustments)
- **Weather & date info** (current weather, forecast, sunrise/sunset, time/date)
- **Media casting & playback control** (Google Cast, YouTube controls)
- **Run custom scripts** via voice
- **Calendar & scheduling** via keyboard automation

## Requirements
- Python 3.9+ (Windows recommended)
- A working microphone
- Google Gemini API key
- OpenWeatherMap API key

### Python Libraries
```
SpeechRecognition
pyttsx3
pyautogui
pyowm
imaplib
screen_brightness_control
pygetwindow
pywin32
google-generativeai
```

## Setup
1. Clone the repo:
   ```bash
   git clone https://github.com/mAhsanZafar/voice-controlled-AI-assistant.git
   cd voice-controlled-AI-assistant
   ```
2. Install dependencies:
   ```bash
   pip install SpeechRecognition pyttsx3 pyautogui pyowm screen_brightness_control pygetwindow pywin32 google-generativeai
   ```
3. Add your API keys in `Jarvis.py`:
   - `gemini_api_key = ('ur_api_key')`
   - `owm = pyowm.OWM('YOUR_OPENWEATHERMAP_KEY')`
4. Update any OS-specific paths in `open_apps()` and script paths in `scripts()`.

## Usage
Run the assistant:
```bash
python Jarvis.py
```
Speak commands like:
- "google python speech recognition"
- "youtube search lo-fi music"
- "directions from new york to boston"
- "brightness increase"
- "weather today"
- "email"
- "open spotify"
- "send messenger new john hello from jarvis"
- "ai mode" (enters AI chat)

## Notes
- Many automation features use `pyautogui` and depend on screen focus and OS-specific shortcuts.
- Some commands are Windows-specific (Task Manager, shutdown/restart, app paths).
- Update email credentials in `check_mail()` if you plan to use Gmail checks.

## License
See [LICENSE](LICENSE).