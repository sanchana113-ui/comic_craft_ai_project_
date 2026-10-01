# 3. Project Design Phase

## Architecture

```text
User / JSON client
        |
        v
   FastAPI routes
        |
        +--> Gemini outline (procedural fallback)
        +--> Gemini script (procedural fallback)
        +--> Pollinations.ai panel art (local image fallback)
        |
        v
  Panel layout builder
      /          \
HTML preview   PDF exporter
```

## Component Responsibilities

- `main.py`: creates the FastAPI app and serves static output.
- `routes.py`: validates requests and coordinates the comic-generation flow.
- `gemini_flash.py`: creates the five-panel outline.
- `gemini_pro.py`: creates panel captions, narration, and dialogue.
- `image_generator.py`: creates panel illustrations and stores PNG files.
- `layout_builder.py`: combines panel text and image paths.
- `exporters.py`: formats the cover and panel pages in a PDF.
- `templates/`: provides the input form, comic preview, and export confirmation.

## Panel Data

Each panel contains a number, title, scene description, image path, caption, narration, dialogue, combined text, and image prompt. Panel order is used to align generated story content with generated images.

## Storage

- `static/panels/`: generated or fallback panel images.
- `static/exports/`: generated PDF files.

## Design Source Files

- [Route orchestration](../app/routes.py)
- [Panel data assembly](../app/layout_builder.py)
- [PDF page design](../app/exporters.py)
- [HTML templates](../templates/)