# PPT2
Features
Paste long text/markdown + optional one-line guidance (e.g., “investor pitch deck”).
Upload a .pptx or .potx template — styles, colors, fonts, and layouts are respected via placeholders.
BYO LLM API key: OpenAI / Anthropic / Gemini (keys are not stored or logged).
Intelligent slide splitting + bulleting via LLM with JSON-structured output.
Reuse any images discovered in the template/presentation (tastefully placed on some slides).
Download a brand new .pptx generated from your template.
Stack
Backend: FastAPI + python-pptx
Frontend: Plain HTML/CSS/JS
Providers: OpenAI (Responses API), Anthropic (Messages API), Gemini (google-genai).
Run locally
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
uvicorn app:app --reload
# open http://localhost:8000
Deploy
Render / Railway / Fly / Heroku / Hugging Face Spaces (provided Procfile).
Docker:
docker build -t presentify .
docker run -p 8000:8000 presentify
Privacy
API keys are accepted in the form and used only for that request in memory.
Keys are not stored and not logged. Please self-host for maximum privacy.
