# Capi - AI Instagram Caption Generator

AI tool that writes business-focused Instagram captions from a product name or a product photo.

## Features
- Photo upload or camera capture: AI reads the photo and writes captions
- 6 languages: Tamil, English, Malayalam, Telugu, Kannada, Hindi
- Tone, caption count and business details
- Copy and Open Instagram buttons

## Tech
FastAPI, Gemini API, plain HTML and JavaScript

## Run
```
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env
```
Add your Gemini API key in `.env`, then:
```
uvicorn app:app --reload
```
Open http://127.0.0.1:8000

## Security
- API key stays server-side in .env (never committed)
- Input validation: caption count limit, language allowlist, image size and type checks
- Prompt rule against instructions hidden inside images