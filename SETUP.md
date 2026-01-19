# Setup Guide

This guide will help you get your documentation hub up and running.

## Stack Overview

### Why MkDocs + Material?

We chose **MkDocs with Material for MkDocs** because it:

✅ **Meets all requirements:**
- Free and open-source
- Markdown-based (easy for non-technical users)
- Full-text search (client-side, no backend)
- Tree-style navigation
- Tags and categories support
- Clean, responsive design
- GitHub Pages compatible

✅ **Easy for contributors:**
- Simple Markdown syntax
- GitHub web interface editing
- Automatic version history via Git
- Clear edit history and diffs

✅ **Low maintenance:**
- Static site (no server needed)
- Automatic deployment via GitHub Actions
- Minimal configuration

## Initial Setup Steps

### 1. Update Configuration

Edit `mkdocs.yml` and replace these placeholders:

```yaml
site_url: https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/
repo_name: YOUR_USERNAME/YOUR_REPO_NAME
repo_url: https://github.com/YOUR_USERNAME/YOUR_REPO_NAME
```

### 2. Test Locally

```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Preview site
mkdocs serve
```

Visit http://127.0.0.1:8000

### 3. Configure GitHub Pages

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Initial documentation setup"
   git push origin main
   ```

2. **Enable GitHub Pages:**
   - Go to repository **Settings** → **Pages**
   - **Source:** Deploy from a branch
   - **Branch:** `gh-pages` (or `main` with `/docs` folder)
   - **Folder:** `/ (root)`

3. **Enable GitHub Actions:**
   - Go to repository **Settings** → **Actions** → **General**
   - Ensure "Workflow permissions" allows "Read and write permissions"
   - Check "Allow GitHub Actions to create and approve pull requests"

### 4. Verify Deployment

- The GitHub Action will run automatically on push
- Check the **Actions** tab to see deployment status
- Your site will be available at: `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

## File Structure Explained

```
.
├── docs/                          # All documentation content
│   ├── index.md                   # Homepage
│   ├── getting-started/           # Introduction guides
│   │   ├── overview.md
│   │   └── quick-start.md
│   ├── guides/                    # How-to guides
│   │   ├── writing-docs.md
│   │   ├── adding-pages.md
│   │   └── using-tags.md
│   ├── reference/                 # Reference docs
│   │   ├── api.md
│   │   └── configuration.md
│   └── tags.md                    # Tags index (auto-generated)
│
├── .github/
│   └── workflows/
│       └── deploy.yml             # Auto-deployment workflow
│
├── mkdocs.yml                     # Main configuration
├── requirements.txt              # Python dependencies
├── CONTRIBUTING.md               # Contribution guide
├── README.md                     # Project overview
└── LICENSE                       # License file
```

## Key Features Implementation

### 1. Tree-Style Navigation

The `nav:` section in `mkdocs.yml` creates the navigation structure. Folders in `docs/` correspond to sections:

```yaml
nav:
  - Getting Started:
    - Overview: getting-started/overview.md
    - Quick Start: getting-started/quick-start.md
```

### 2. Full-Text Search

Enabled by default via the `search` plugin. No configuration needed - it automatically indexes all content.

### 3. Tags & Categories

Add tags to any page using front matter:

```markdown
---
title: My Page
tags:
  - api
  - authentication
---
```

The tags plugin automatically creates the tags index page.

### 4. Version History

All changes are tracked in Git:
- View history on GitHub: Click "History" on any file
- See diffs in pull requests
- Use `git log` locally

### 5. Edit Links

The "Edit this page" link appears automatically at the top of each page, linking to GitHub's editor.

## WYSIWYG Editor Workflow

### Option 1: GitHub Web Interface (Recommended)

This is the closest to a WYSIWYG experience for non-technical users:

1. Click "Edit this page" on any documentation page
2. GitHub's editor shows:
   - Markdown source on the left
   - Live preview on the right
3. Make changes and commit
4. Create a pull request

### Option 2: Local Markdown Editor

For users comfortable with local tools:

- **VS Code** with Markdown extensions
- **Typora** - WYSIWYG Markdown editor
- **Mark Text** - Real-time preview editor
- **Obsidian** - Knowledge base editor

### Option 3: Git-Based CMS (Advanced)

For a more WYSIWYG experience, you could integrate:

- **Decap CMS** (formerly Netlify CMS) - Requires a config file
- **Forestry** - Git-based CMS (has free tier)
- **Stackbit** - Visual editor (has free tier)

However, these may require additional setup and some have limitations on free tiers.

## Customization

### Change Theme Colors

Edit `mkdocs.yml`:

```yaml
theme:
  palette:
    - scheme: default
      primary: indigo  # Change to: blue, green, red, etc.
      accent: blue
```

### Add Logo

1. Add logo file to `docs/images/logo.png`
2. Update `mkdocs.yml`:

```yaml
theme:
  logo: images/logo.png
```

### Customize Navigation

Edit the `nav:` section in `mkdocs.yml` to match your content structure.

## Troubleshooting

### Site Not Building

- Check GitHub Actions logs
- Verify `mkdocs.yml` syntax is correct
- Ensure all files in `nav:` exist

### Search Not Working

- Clear browser cache
- Rebuild the site: `mkdocs build`
- Verify `search` plugin is in `plugins:` list

### Pages Not Updating

- Check GitHub Actions workflow status
- Verify GitHub Pages is enabled
- Ensure workflow has write permissions

## Next Steps

1. ✅ Replace placeholder content with your actual documentation
2. ✅ Customize colors and branding in `mkdocs.yml`
3. ✅ Add your organization's logo
4. ✅ Update repository URLs in configuration
5. ✅ Share the site with your team
6. ✅ Start contributing!

## Resources

- [MkDocs Documentation](https://www.mkdocs.org/)
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

---

Need help? Check the [Contributing Guide](CONTRIBUTING.md) or create an issue on GitHub.
