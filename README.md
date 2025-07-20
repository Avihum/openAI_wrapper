# 🧠 openAI_wrapper
A minimal FastAPI-based backend that wraps OpenAI's Chat Completions API using asynchronous HTTP calls.  
Ideal for building lightweight AI-powered apps with simple, secure local integration.


## 🚀 Features
- ✅ FastAPI-powered async REST API
- ✅ `/chat` endpoint using OpenAI's `gpt-3.5-turbo`
- ✅ `.env`-based API key management with `python-dotenv`
- ✅ Swagger UI auto-generated at `/docs`
- ✅ Fully ready for deployment or frontend integration


## 🗺️ Project Structure
├── app.py # Main FastAPI app
├── config.py # Loads OPENAI_API_KEY from .env
├── pyproject.toml # Poetry dependency manager
├── test_config.py # Sanity check for config loading
└── .gitignore # Excludes secrets & venv

## 🧪 How to Use

1. Install dependencies
#bash
poetry install

2. Add your .env
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

3. Run the API
poetry run uvicorn app:app --reload

4. Open http://localhost:8000/docs to test it live.

📬 Example Request
POST /chat
{
  "message": "Tell me a joke"
}

Response
{
  "reply": "Why couldn't the bicycle stand up by itself? Because it was two-tired!"
}


📦 Built With
- FastAPI
- httpx
- python-dotenv
- OpenAI API


📌 Notes
Do not commit your .env or API keys.
The app uses httpx.AsyncClient for efficient async requests.
You can easily extend it with frontend logic (HTMX, Jinja2, etc.) or deploy to platforms like Render.

🧑‍💻 Author: Avihu Marco
