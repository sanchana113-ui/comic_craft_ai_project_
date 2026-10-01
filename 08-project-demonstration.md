# 8. Project Demonstration

## Demonstration Goal

Show a complete workflow from a user's story idea to a five-panel illustrated comic and downloadable PDF.

## Walkthrough

1. Start the FastAPI app and open `http://127.0.0.1:8000/`.
2. Enter the story premise, character, setting, tone, and art style.
3. Generate the comic and show the five panels, including narration, captions, dialogue, and images.
4. Download and open the exported PDF to show its cover and panel pages.
5. Optionally demonstrate the JSON endpoint and describe the fallback behavior.

## Demo Materials

- [Input form](../templates/index.html)
- [Comic preview](../templates/comic_preview.html)
- [Export confirmation](../templates/export_success.html)
- [Current workspace demo recording](../Recording%202026-09-24%20233301.mp4)

Generated PDFs in `static/exports/` and panel images in `static/panels/` are runtime artifacts. The repository currently excludes generated output and the recording from Git. If the submission requires these files, review their size and include only selected examples intentionally. Never expose `.env` or API credentials.

## Ready-to-Present Checklist

- Confirm the application starts and the home page loads.
- Confirm the prompt produces five panels.
- Confirm the PDF download opens correctly.
- Be ready to explain fallback behavior if an external service is unavailable.
- Keep API credentials and unrelated local files out of the demonstration.