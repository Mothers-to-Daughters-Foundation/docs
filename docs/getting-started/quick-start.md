---
title: Quick Start Guide
tags:
  - getting-started
  - quick-start
  - tutorial
categories:
  - Getting Started
---

# Quick Start Guide

Get started contributing to the documentation in just a few steps!

## Option 1: Edit via GitHub Web Interface (Easiest)

1. Navigate to the file you want to edit on GitHub
2. Click the **pencil icon** (Edit this file)
3. Make your changes in the editor
4. Scroll down and click **"Commit changes"**
5. Select **"Create a new branch"** and give it a name
6. Click **"Propose changes"**
7. Create a pull request

## Option 2: Edit Locally (For Advanced Users)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   cd YOUR_REPO_NAME
   ```

2. **Set up Python environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Preview locally:**
   ```bash
   mkdocs serve
   ```
   Open http://127.0.0.1:8000 in your browser

4. **Make changes:**
   - Edit files in the `docs/` folder
   - The preview updates automatically

5. **Commit and push:**
   ```bash
   git add .
   git commit -m "Update documentation"
   git push origin your-branch-name
   ```

## Adding a New Page

1. Create a new `.md` file in the appropriate folder under `docs/`
2. Add front matter at the top (optional but recommended):
   ```markdown
   ---
   title: Your Page Title
   tags:
     - tag1
     - tag2
   ---
   ```
3. **Navigation is automatic!** The page appears in navigation automatically based on folder structure
4. Commit and push your changes

## Need Help?

- Check the [Writing Documentation](../guides/writing-docs.md) guide
- See [Adding New Pages](../guides/adding-pages.md) for detailed instructions
- Review existing pages for examples
