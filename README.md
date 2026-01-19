# Documentation Hub

A simple, easy-to-use documentation hub built with [MkDocs](https://www.mkdocs.org/) and the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme. Designed for small organizations to collaborate on documentation with minimal technical overhead.

## ✨ Features

- 📝 **Markdown-based** - Easy to write and edit
- 🌳 **Auto-generated navigation** - Tree-style sidebar that mirrors folder structure
- 🔍 **Full-text search** - Find anything quickly
- 🏷️ **Tags & Categories** - Organize content by topic
- 📱 **Responsive design** - Works on all devices
- 🌓 **Dark mode** - Easy on the eyes
- 📊 **Version history** - All changes tracked in Git
- ✏️ **Edit links** - Edit any page directly from GitHub
- 🚀 **Auto-deployment** - Automatically deploys to GitHub Pages

## 🚀 Quick Start

### Prerequisites

- Python 3.7 or higher
- Git

### Local Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   cd YOUR_REPO_NAME
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Preview locally:**
   ```bash
   mkdocs serve
   ```
   Open http://127.0.0.1:8000 in your browser

5. **Build the site:**
   ```bash
   mkdocs build
   ```
   Output will be in the `site/` directory

## 📁 Project Structure

```
.
├── docs/                    # Documentation source files
│   ├── index.md            # Home page
│   ├── getting-started/    # Getting started guides
│   ├── guides/             # How-to guides
│   ├── reference/          # Reference documentation
│   └── tags.md             # Tags index page
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Actions deployment
├── mkdocs.yml              # MkDocs configuration
├── requirements.txt        # Python dependencies
├── CONTRIBUTING.md         # Contribution guidelines
└── README.md               # This file
```

## ⚙️ Configuration

### Basic Configuration

Edit `mkdocs.yml` to customize:

- **Site name and URL** - Update `site_name` and `site_url`
- **Repository info** - Update `repo_name` and `repo_url` for "Edit this page" links
- **Theme colors** - Modify the `palette` section
- **Navigation** - Update the `nav:` section to match your content structure

### GitHub Pages Setup

1. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Source: Deploy from a branch
   - Branch: `gh-pages` (or `main` if using `/docs` folder)
   - Folder: `/ (root)`

2. **The GitHub Action will automatically:**
   - Build the site on every push to `main`
   - Deploy to GitHub Pages
   - Update the site automatically

### Customization

- **Theme colors:** Edit the `palette` section in `mkdocs.yml`
- **Logo:** Add a logo file and reference it in `theme.logo`
- **Social links:** Add links in the `extra.social` section
- **Plugins:** Add or remove plugins in the `plugins:` section

## 📝 Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

### Quick Contribution Guide

1. **Edit via GitHub (Easiest):**
   - Click "Edit this page" on any documentation page
   - Make your changes
   - Create a pull request

2. **Add a new page:**
   - Create a new `.md` file in the appropriate folder under `docs/`
   - Navigation updates automatically - no configuration needed!
   - Commit and push

3. **Use tags:**
   - Add tags in the front matter of your Markdown files
   - Tags help organize and discover content

See the [Contributing Guide](CONTRIBUTING.md) for more details.

## 🛠️ Development

### Available Commands

- `mkdocs serve` - Start the development server
- `mkdocs build` - Build the static site
- `mkdocs gh-deploy` - Deploy to GitHub Pages (manual)

### Adding Plugins

1. Install the plugin:
   ```bash
   pip install mkdocs-plugin-name
   ```

2. Add to `requirements.txt`

3. Add to `plugins:` section in `mkdocs.yml`

## 📚 Documentation

- [Getting Started](docs/getting-started/overview.md)
- [Writing Documentation](docs/guides/writing-docs.md)
- [Adding New Pages](docs/guides/adding-pages.md)
- [Folder Organization](docs/guides/folder-organization.md) - How navigation works
- [Navigation System](docs/guides/navigation-system.md) - Detailed navigation guide
- [Using Tags](docs/guides/using-tags.md) - Tag usage guide
- [Tags and Categories Reference](docs/guides/tags-reference.md) - Complete tags reference

## 🎯 Features Explained

### Auto-Generated Tree-Style Navigation

The navigation **automatically generates from your folder structure**. Folders become collapsible sections, and files become pages. No manual configuration needed - just organize your files, and the navigation updates automatically. See [Folder Organization](docs/guides/folder-organization.md) for details.

### Full-Text Search

Built-in search plugin indexes all content. No backend required - it's all client-side JavaScript.

### Tags & Categories

Add tags and categories to pages using front matter:
```markdown
---
title: Your Page Title
tags:
  - api
  - authentication
categories:
  - Guides
---
```

Tags appear above the page title and are clickable - click any tag to see all related pages. The [Tags page](docs/tags.md) automatically lists all tags and their associated pages.

### Version History

All changes are tracked in Git. View history on GitHub or use `git log` locally.

### Edit Links

The "Edit this page" link at the top of each page takes you directly to GitHub's editor.

## 🔧 Troubleshooting

### Build Errors

- Check that all files referenced in `nav:` exist
- Ensure Markdown syntax is correct
- Check Python version (3.7+)

### Search Not Working

- Ensure the `search` plugin is enabled in `mkdocs.yml`
- Clear browser cache
- Rebuild the site

### GitHub Pages Not Updating

- Check GitHub Actions workflow status
- Ensure Pages is enabled in repository settings
- Verify the workflow has proper permissions

## 📄 License

This project is open source. Add your license information here.

## 🙏 Acknowledgments

- [MkDocs](https://www.mkdocs.org/) - Documentation framework
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) - Beautiful theme
- [GitHub Pages](https://pages.github.com/) - Free hosting

## 📞 Support

- Check the [documentation](docs/)
- Review [existing issues](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME/issues)
- Create a new issue if needed

---

**Built with ❤️ for easy documentation collaboration**
