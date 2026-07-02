# AI Chatbot — Terminal to Web App

A conversational AI chatbot built with LangChain and Google's Gemini API, evolved from a terminal-based prototype into a deployed web app.

🔗 **Live demo:** (https://my-first-ai.streamlit.app/)

<img width="1918" height="907" alt="image" src="https://github.com/user-attachments/assets/0ccee0c1-edb9-4467-ac11-e3c3cedc3f44" />

---

## Project Journey

### Phase 1 — `test.py` (terminal chatbot, self-built)
I built the original chatbot logic myself: connecting to Gemini via LangChain, handling user input in a loop, and getting model responses in the terminal. This is where the core AI integration — the model setup, the invoke call, the conversation loop — was written and understood by me.

### Phase 2 — `app.py` (Streamlit web UI)
I don't have prior experience with Streamlit, so I used Claude (Anthropic's AI assistant) to help convert the terminal logic into a web interface — chat UI, message history, session state, and deployment configuration. The underlying chatbot logic (the LangChain + Gemini integration) is the same logic I wrote in `test.py`; Streamlit was used purely as the UI/deployment layer on top of it.

### Phase 3 — Deployment
Deployed for free on Streamlit Community Cloud, with the API key managed securely via Streamlit Secrets (not hardcoded or committed to the repo).

---

## Tech Stack
- **Python**
- **LangChain** (`langchain-google-genai`) — LLM orchestration
- **Google Gemini 2.5 Flash** — underlying language model
- **Streamlit** — web UI and deployment
- **python-dotenv** — local environment variable management

---

## Files
| File | Purpose |
|---|---|
| `test.py` | Original terminal-based chatbot (self-built) |
| `app.py` | Streamlit web version (AI-assisted UI layer) |
| `requirements.txt` | Python dependencies |
| `.env.example` | Template for required environment variables |

---

## Running Locally
```bash
pip install -r requirements.txt
```
Create a `.env` file in the project root:
```
GOOGLE_API_KEY=your_gemini_api_key_here
```
Then run:
```bash
streamlit run app.py
```

---

## What I Learned
- Integrating an LLM API into a Python application using LangChain
- Managing conversation state and message history
- Securely handling API keys across local and cloud environments
- Deploying a Python web app to a cloud platform
