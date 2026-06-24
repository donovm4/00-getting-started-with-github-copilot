# Getting Started

## 1. Project structure (brief)

This repository contains a small FastAPI web app with a static frontend:

- src/app.py
  - Main FastAPI application
  - Serves API routes:
    - GET /activities
    - POST /activities/{activity_name}/signup?email=...
  - Redirects / to the static UI
  - Mounts static files from src/static
- src/static/index.html
  - Frontend page layout
- src/static/app.js
  - Frontend logic to fetch activities and submit signups
- src/static/styles.css
  - Frontend styling
- requirements.txt
  - Python dependencies
- pytest.ini
  - Basic pytest config
- README.md and src/README.md
  - Repository and app-level documentation

## 2. How to run it

From the repository root:

1. Create and activate a virtual environment (recommended)

    python3 -m venv .venv
    source .venv/bin/activate

2. Install dependencies

    pip install -r requirements.txt

3. Start the app

    python src/app.py

4. Open in your browser

- App UI: http://localhost:8000/
- Swagger docs: http://localhost:8000/docs
- ReDoc: http://localhost:8000/redoc

## 3. Optional alternative start command

You can also run with uvicorn directly:

    uvicorn src.app:app --reload

If your working directory is src, use:

    uvicorn app:app --reload

## 4. Run with VS Code Run and Debug (great for Codespaces)

You can start the app from the editor instead of the terminal:

1. Open the Run and Debug view in VS Code.
2. Select a Python launch target for this project (for example, running src/app.py).
3. Click the Run icon.
4. Open the forwarded/local URL at http://localhost:8000/.

In Codespaces, this method is often convenient because VS Code handles debug launch flow and port forwarding UI for you.
