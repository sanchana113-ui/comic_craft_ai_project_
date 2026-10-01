# 6. Project Testing

## Automated Test Coverage

The existing [test suite](../test_pipeline.py) checks:

- Five-panel outline structure.
- Script fields for each panel.
- Image file creation and uniqueness.
- Layout assembly and image-path alignment.
- PDF creation and output-file existence.
- Homepage, image test route, JSON generation, export confirmation, PDF download, and form generation.

## Run the Tests

Install dependencies from the repository root, configure environment variables if needed, then run:

```powershell
python -m unittest test_pipeline.py
```

These are integration tests. They can make external requests and create image and PDF outputs. Gemini has procedural fallbacks; image generation can request Pollinations.ai before using the local fallback.

## Manual Test Checklist

1. Start the server with `uvicorn app.main:app --reload`.
2. Open `http://127.0.0.1:8000/` and submit a prompt.
3. Confirm the preview includes five panels, text, and images.
4. Download and open the PDF.
5. Submit a valid request to `/generate-comic/json` and inspect the response.
6. Verify the fallback behavior when an external generation service is unavailable.

Record test date, Python version, command, outcome, and external-service availability. This document does not claim a test pass; run the suite to obtain a current result.