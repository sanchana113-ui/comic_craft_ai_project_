# 5. Project Development Phase

## Implemented Workflow

1. `POST /generate` accepts the browser form, or `POST /generate-comic/json` accepts a JSON request.
2. The route derives a comic title and requests a five-panel outline.
3. The route generates a script and one illustration for each panel.
4. The layout builder aligns outline, script, and image paths.
5. The form route renders the comic preview; the JSON route returns the layout and PDF path.
6. The PDF exporter saves a multi-page comic under `static/exports/`.

## Source Code

- [Application entry point](../app/main.py)
- [Web routes and orchestration](../app/routes.py)
- [Gemini Flash outline and fallback](../app/gemini_flash.py)
- [Gemini Pro script and fallback](../app/gemini_pro.py)
- [Pollinations image generation and local fallback](../app/image_generator.py)
- [Panel layout builder](../app/layout_builder.py)
- [Comic PDF exporter](../app/exporters.py)

## User Interface

- [Comic prompt form](../templates/index.html)
- [Comic preview page](../templates/comic_preview.html)
- [Export success page](../templates/export_success.html)

The code files remain in these original locations; this phase document organizes and explains them without creating divergent duplicate copies.