# Your Text, Your Style – Auto-Generate a Presentation


Create a web app that turns long-form text/markdown into a fully formatted PowerPoint that matches an uploaded template (.pptx/.potx). The app:


- Accepts bulk text + optional one-line guidance
- Accepts a user-supplied LLM API key (OpenAI / Anthropic / Gemini)
- Accepts a .pptx/.potx template or existing deck to mimic style
- Analyzes text → slide structure (titles, bullets, speaker notes)
- Reuses layout, colors, fonts, and images from the uploaded template
- Outputs a new .pptx for download — **no AI image generation**


## Demo (Self-Host)
- Backend: FastAPI (Python, `python-pptx`)
- Frontend: Next.js + Tailwind


### Quick Start


#### 1) Backend
```bash
cd backend
python -m venv .venv && source .venv/bin/activate # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
uvicorn main:app --host 0.0.0.0 --port 8000
```


#### 2) Frontend
```bash
cd ../frontend
npm install
echo "NEXT_PUBLIC_API_BASE=http://localhost:8000" > .env.local
npm run dev
