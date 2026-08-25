# VxH Jarvis

**Advanced AI Personal Assistant** — A powerful, voice-controlled, multi-modal AI agent inspired by Iron Man's JARVIS.

VxH Jarvis brings intelligent automation, computer control, real-time web capabilities, and persistent memory to your desktop.

![Python](https://img.shields.io/badge/Python-3.11%2B-blue)
![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey)
![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-green)

---

## Features

- **Voice & Text Interaction** — Seamless hybrid input with natural conversation
- **Computer Control** — Open apps, control desktop, manage files, take screenshots
- **Web Intelligence** — Search the web, find flights, get weather, YouTube transcripts
- **Code Assistance** — Help with coding tasks and development workflows
- **Persistent Memory** — Remembers your preferences, projects, and context
- **File Processing** — Analyze PDFs, images, source code on the fly
- **Cross-Platform** — Works on Windows, macOS, and Linux
- **OpenRouter + Gemini** — Optimized free-tier model routing for higher limits

---

## Quick Start

### Prerequisites
- Python 3.11 or 3.12
- Microphone (for voice mode)
- Free [Google Gemini API key](https://aistudio.google.com/app/apikey)
- Free [OpenRouter API key](https://openrouter.ai/keys)

### Installation

```bash
# Clone the repository
git clone https://github.com/roardiamond/VxH-Jarvis.git
cd VxH-Jarvis

# Install dependencies
pip install -r requirements.txt
playwright install

# (Optional) Run setup helper
python setup.py
```

### Configuration

1. Create a config folder and API keys file:
   ```bash
   mkdir -p config
   ```
2. Add your API keys to `config/api_keys.json`:
   ```json
   {
     "gemini_api_key": "YOUR_GEMINI_API_KEY",
     "openrouter_api_key": "YOUR_OPENROUTER_API_KEY"
   }
   ```

### Run

```bash
python main.py
```

---

## Project Structure

```
VxH-Jarvis/
├── main.py                 # Entry point
├── ui.py                   # Adaptive UI
├── or_client.py            # OpenRouter client
├── setup.py                # Installation helper
├── requirements.txt
├── actions/                # Tool modules
│   ├── browser_control.py
│   ├── computer_control.py
│   ├── file_processor.py
│   ├── web_search.py
│   └── ...
├── agent/                  # Planning & execution
│   ├── planner.py
│   ├── executor.py
│   └── ...
├── memory/                 # Persistent memory system
├── core/
│   └── prompt.txt          # System prompt
└── config/
```

---

## How It Works

1. **Input** → Voice (Gemini Live) or text
2. **Planner** → Breaks tasks into actionable steps
3. **Executor** → Calls the right tools (desktop, web, files, etc.)
4. **Memory** → Stores and retrieves personal context
5. **Response** → Natural language + actions performed

---

## Requirements

| Component       | Details                          |
|----------------|----------------------------------|
| OS             | Windows 10/11, macOS, Linux     |
| Python         | 3.11 or 3.12                    |
| Microphone     | Required for voice              |
| API Keys       | Gemini + OpenRouter (free tier) |

> **Note:** Some OS-specific packages (e.g. `pycaw`, `pywinauto` on Windows) may need manual installation if missing.

---

## License

Personal and non-commercial use only.  
Licensed under [Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/).

---

## Credits

Based on the excellent **VxH Jarvis** project by [YASHXCHI](https://github.com/roardiamond).

Enhanced and maintained as **VxH Jarvis**.

⭐ Star the repo if you find it useful!
