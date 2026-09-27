# 🎙️ Audio Transcriber

Record or upload audio and get instant transcriptions — powered by **Google Gemini's native audio understanding**.

> **Attribution:** This project is based on [leopoldpoldus/streamlit_whisper_transcription](https://github.com/leopoldpoldus/streamlit_whisper_transcription) (MIT License). The original app used OpenAI's Whisper API; I migrated the transcription engine to Google Gemini while keeping the same Streamlit UX.

## What it does

- 🎤 Record audio directly in the browser
- 📤 Upload audio files (`.mp3`, `.mp4`, `.wav`, `.m4a`)
- ⚡ Transcribe in real time with Gemini
- 💾 Save and download transcriptions as text files

## What changed from the original

- Replaced the OpenAI Whisper API with **Gemini native audio understanding** (`google-genai` SDK)
- Reads the API key from a `.env` file (`GOOGLE_API_KEY`) — no hardcoded keys
- Configurable model via `GEMINI_MODEL` env var (default: `gemini-2.5-flash`)
- Automatic MIME-type detection for uploads

## Quick start

```bash
pip install -r requirements.txt
cp .env.example .env   # then put your Gemini API key in .env
streamlit run app.py
```

`.env` format:

```
GOOGLE_API_KEY=your-key-here
GEMINI_MODEL=gemini-2.5-flash
```

## License

MIT — see [LICENSE](LICENSE) (original license by Leopold Poldus, preserved).
