# AI Document Summarizer

A Python web app that summarizes text and documents using Streamlit
and a local Ollama model.

## Features

- Paste text or upload PDF, DOCX, and UTF-8 TXT files
- Choose Short, Medium, or Detailed summaries
- Download summaries as TXT files
- Keep the last summary during the current session
- Run AI locally without a paid API

## Requirements

- Python 3.10+
- Ollama installed and running
- Enough storage and memory to run qwen3:4b-instruct

## Setup on macOS / Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

Download the model:

```bash
ollama pull qwen3:4b-instruct
```

Keep Ollama running, then start the app:

```bash
python -m streamlit run app.py
```

## Limitations

- Scanned PDFs require OCR, which is not included.
- DOCX extraction currently reads paragraphs, not tables.
- Input is limited to 12,000 characters.
- AI summaries may contain errors; verify important facts.
- Summaries are stored in session memory, not permanently.
- The configured Google Font requires an internet connection.

## Built With

Python, Streamlit, Ollama, pypdf, and python-docx.