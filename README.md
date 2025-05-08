# Zack's Linux Hacker Notes

A personal documentation site for Linux learning, commands, projects, and resources.

## About

This repository contains my notes and resources for learning various Linux distributions and tools. The site is built with MkDocs and deployed using GitHub Pages.

## Structure

- `docs/`: Contains all the Markdown files that make up the site content
- `mkdocs.yml`: Configuration file for MkDocs
- `.github/workflows/`: GitHub Actions workflows for automatic deployment

## Local Development

To run this site locally:

1. Set up a Python virtual environment and install dependencies:
   ```bash
   # Create a virtual environment
   python -m venv venv
   
   # Activate the virtual environment
   source venv/bin/activate  # On Linux/macOS
   # or
   # .\venv\Scripts\activate  # On Windows
   
   # Install MkDocs and the Material theme
   pip install mkdocs mkdocs-material
   ```

2. Start the development server:
   ```bash
   # With virtual environment activated
   mkdocs serve
   
   # Or use the convenience script
   ./run_mkdocs.sh
   ```

3. Open your browser to http://localhost:8000

## License

This project is open source and available under the [MIT License](LICENSE).