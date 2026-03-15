# CodeReviewAgent

**CodeReviewAgent** is an AI-powered full-stack application that automatically performs code reviews.  
It uses **FastAPI** and **LangGraph** on the backend to analyze code, find issues, and generate structured reports.  
The frontend is built with **Next.js** and connects to the backend for a smooth developer experience.

---

## Features

- Upload code via API and receive:
  - Initial analysis of purpose and structure
  - List of specific issues
  - Final code review report
- Fast and modular workflow powered by **LangGraph**
- Easy integration with any frontend or CI/CD pipeline

---

## Tech Stack

**Backend:**

- Python 3.10+
- FastAPI
- LangGraph
- LangChain Ollama
- Pydantic
- Python-dotenv
- Uvicorn

**Frontend:**

- Next.js 16
- Tailwind CSS
- Shadcn/ui

**Other:**

- GitHub for version control
- Ollama for LLM inference

---

## Project Structure

CodeReviewAgent/
├── backend/
│ ├── app.py # Main FastAPI backend
│ ├── requirements.txt
│ └── venv/ # Local Python environment (ignored)
├── frontend/
│ ├── package.json
│ └── .next/ # Build folder (ignored)
├── .gitignore
└── README.md


---

## Getting Started

### Backend

1. Go to the backend folder:

```bash
cd backend
Create and activate a virtual environment:

Windows (PowerShell):

python3 -m venv venv
.\venv\Scripts\Activate.ps1
Mac/Linux:

python3 -m venv venv
source venv/bin/activate
Install dependencies:

pip install -r requirements.txt
Run the server:

uvicorn app:app --reload
The API will be available at: http://127.0.0.1:8000/docs (Swagger UI)

Frontend
Go to the frontend folder:

cd ../frontend
Install dependencies:

npm install
Run the development server:

npm run dev
The frontend will run at: http://localhost:3000

Usage
Send a POST request to:

POST http://127.0.0.1:8000/review
With a JSON body like:

{
  "code": "print('Hello world')"
}
Response:

{
  "analysis": "Short description of the code",
  "issues": ["- issue1", "- issue2"],
  "report": "Final code review report"
}
Notes
Make sure Ollama is installed and running for LLM inference.

.env files can be used for API keys or environment variables.

.next/ and node_modules/ are ignored in Git and should not be committed.

Future Improvements
Streaming responses for faster reviews

Web UI for drag-and-drop code review

CI/CD integration for automatic PR analysis

Support for multiple programming languages

License
MIT License
