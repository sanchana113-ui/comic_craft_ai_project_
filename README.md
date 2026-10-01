# ComicCraft Project Package

This folder organizes the project deliverables into the eight requested project phases. The working application code remains in the repository's existing `app/`, `templates/`, and `static/` directories; phase documents link to those files rather than duplicating them.

## Project Phases

1. [Brainstorming & Ideation](01-brainstorming-and-ideation.md)
2. [Requirement Analysis](02-requirement-analysis.md)
3. [Project Design Phase](03-project-design.md)
4. [Project Planning Phase](04-project-planning.md)
5. [Project Development Phase](05-project-development.md)
6. [Project Testing](06-project-testing.md)
7. [Project Documentation](07-project-documentation.md)
8. [Project Demonstration](08-project-demonstration.md)

## Application

ComicCraft is a web application that turns a user-provided story premise into an illustrated five-panel comic. It generates an outline and script, creates one image per panel, assembles a browser preview, and exports a PDF.

### Main Code Files

- [FastAPI app entry point](../app/main.py)
- [Web and JSON routes](../app/routes.py)
- [Five-panel outline generation](../app/gemini_flash.py)
- [Panel script generation](../app/gemini_pro.py)
- [Panel illustration generation](../app/image_generator.py)
- [Panel layout assembly](../app/layout_builder.py)
- [PDF export](../app/exporters.py)
- [Integration test suite](../test_pipeline.py)
- [Python dependencies](../requirements.txt)

### Important Configuration

Set `GEMINI_API_KEY` locally for Gemini text generation. `POLLINATIONS_TOKEN` is optional for illustration generation. Never commit `.env`, API keys, or tokens. Generated PDFs and panel images are runtime artifacts and are excluded by `.gitignore`.