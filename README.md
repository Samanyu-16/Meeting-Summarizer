# 📝 Meeting Minutes → Action Items Agent

An AI-powered meeting summarizer that converts raw meeting notes into structured outputs including summaries, decisions, action items, and a follow-up email.

Built using Groq (LLaMA 3) / Google Gemini, with a simple Gradio UI for interaction.

---

## 🚀 Features

- Converts raw meeting notes into:
  - 3-point summary
  - Key decisions
  - Action items (with owner, due date, priority)
  - Ready-to-send follow-up email
- Automatic due date normalization (e.g., “next Friday” → actual date)
- Supports multiple LLM providers:
  - Groq (LLaMA 3.1)
  - Google Gemini (1.5 Flash)
- Export action items as CSV
- Clean web interface using Gradio

---

## 🛠️ Tech Stack

- Python  
- Gradio  
- Groq API (LLaMA 3.1)  
- Google Generative AI (Gemini)  
- Pandas  
- Dateparser  

---

## 📦 Installation

```bash
pip install gradio groq google-generativeai pandas python-dateutil dateparser

🔑 API Setup

Set at least one API key before running:
import os

os.environ["GROQ_API_KEY"] = "your_groq_key"
# OR
os.environ["GEMINI_API_KEY"] = "your_gemini_key"

🧠 How It Works
Enter meeting title, date/time, and raw notes
The system sends a structured prompt to the LLM
LLM returns structured JSON
Outputs include:
Summary
Decisions
Action items
Email draft
Results are displayed and downloadable as CSV
