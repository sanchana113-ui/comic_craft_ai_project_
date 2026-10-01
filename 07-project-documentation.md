# 7. Project Documentation

## Prerequisites

- Python available in a terminal.
- Packages listed in [`requirements.txt`](../requirements.txt).
- Internet access for remote Gemini and Pollinations.ai generation.
- Gemini API key for Gemini-backed text generation; procedural text fallbacks are used when it is missing or unavailable.
- `POLLINATIONS_TOKEN` is optional for image generation.

## Install

From the repository root in PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Set `GEMINI_API_KEY` in a local `.env` file or in the process environment. The image generator reads optional `POLLINATIONS_TOKEN`. Never commit `.env` or real credentials.

## Run

```powershell
uvicorn app.main:app --reload
```

Open `http://127.0.0.1:8000/` in a browser.

## Routes

- `GET /`: home page and comic input form.
- `POST /generate`: form-based comic generation and preview.
- `POST /generate-comic/json`: JSON comic-generation API.
- `GET /test-image`: direct image-generation utility.
- `GET /download-pdf`: PDF download endpoint.
- `GET /export-success`: export confirmation page.

## Integration Note

Gemini generates text when configured. The current image generator uses Pollinations.ai, not a Hugging Face Stable Diffusion endpoint. Update this documentation if the implementation changes.