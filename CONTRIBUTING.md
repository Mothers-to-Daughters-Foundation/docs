# Contributing Guide

Thank you for contributing to our documentation! This guide will help you get started.

## How to Contribute

### For Non-Technical Contributors

The easiest way to contribute is through GitHub's web interface:

1. **Find the page you want to edit**
   - Navigate to the file on GitHub (e.g., `docs/guides/writing-docs.md`)
   - Or click "Edit this page" at the top of any documentation page

2. **Make your changes**
   - Click the pencil icon (✏️) to edit
   - Make your changes in the editor
   - You can preview how it will look

3. **Submit your changes**
   - Scroll down and click "Commit changes"
   - Select "Create a new branch" and give it a descriptive name
   - Click "Propose changes"
   - Create a pull request with a description of your changes

4. **Wait for review**
   - Someone will review your changes
   - They may suggest improvements
   - Once approved, your changes will be merged!

### For Technical Contributors

If you're comfortable with Git and local development:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   cd YOUR_REPO_NAME
   ```

2. **Set up your environment:**
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

4. **Make your changes:**
   - Edit files in the `docs/` folder
   - The preview updates automatically

5. **Commit and push:**
   ```bash
   git checkout -b your-feature-branch
   git add .
   git commit -m "Description of your changes"
   git push origin your-feature-branch
   ```

6. **Create a pull request** on GitHub

## Writing Guidelines

### Markdown Basics

- Use headers (`#`, `##`, `###`) to structure content
- Use lists for multiple items
- Use code blocks for code examples
- Add links to related pages

See [Writing Documentation](docs/guides/writing-docs.md) for detailed formatting guidelines.

### Adding New Pages

1. Create a new `.md` file in the appropriate folder
2. Add front matter with title and tags
3. **That's it!** Navigation is auto-generated from folder structure
4. Commit and push

See [Adding New Pages](docs/guides/adding-pages.md) for step-by-step instructions.
See [Folder Organization](docs/guides/folder-organization.md) to understand how folders map to navigation.

### Using Tags and Categories

Add tags and categories to help organize content:

```markdown
---
title: Your Page Title
tags:
  - relevant-tag
  - another-tag
categories:
  - Guides
---
```

**Tags** appear above the page title and are clickable - click any tag to see all related pages.  
**Categories** help organize content into broader groups.

See [Using Tags](docs/guides/using-tags.md) for best practices.  
See [Tags and Categories Reference](docs/guides/tags-reference.md) for complete documentation.

## Code of Conduct

- Be respectful and constructive
- Help others learn
- Focus on improving the documentation
- Ask questions if you're unsure

## Getting Help

- Check existing documentation first
- Review the [Getting Started](docs/getting-started/overview.md) guide
- Ask questions in pull requests
- Contact the maintainers if needed

## What to Contribute

We welcome contributions of all kinds:

- ✅ Fixing typos and grammar
- ✅ Clarifying unclear explanations
- ✅ Adding missing information
- ✅ Creating new guides and tutorials
- ✅ Improving examples
- ✅ Adding screenshots or diagrams
- ✅ Translating content (if applicable)

Thank you for helping make our documentation better! 🎉
