---
title: Adding New Pages
tags:
  - guide
  - contributing
  - pages
categories:
  - Guides
---

# Adding New Pages

Learn how to add new pages to the documentation site.

## Step-by-Step Guide

### 1. Create the Markdown File

Create a new `.md` file in the appropriate folder under `docs/`:

```
docs/
  ├── guides/
  │   └── your-new-page.md  ← Create here
  ├── reference/
  │   └── another-page.md
  └── ...
```

### 2. Add Content

Start with front matter (optional but recommended):

```markdown
---
title: Your Page Title
tags:
  - relevant-tag
  - another-tag
---

# Your Page Title

Your content goes here...
```

### 3. Navigation is Automatic! ✨

**No configuration needed!** The navigation automatically includes your new page based on the folder structure. Just create the file in the right folder, and it will appear in the sidebar.

The page will appear in the navigation under the appropriate section (e.g., if you create `docs/guides/my-page.md`, it automatically appears under "Guides").

### 4. Optional: Control Page Order

If you want to control the order of pages in a folder, edit the `.pages` file in that directory:

```yaml
# docs/guides/.pages
nav:
  - writing-docs.md
  - adding-pages.md
  - your-new-page.md  # Add here to control order
```

If you don't create a `.pages` file, pages are automatically included in alphabetical order.

### 5. Commit and Push

1. **Via GitHub Web Interface:**
   - Create the file, add content, commit to a new branch
   - Create a pull request

2. **Via Git:**
   ```bash
   git add docs/guides/your-new-page.md
   git commit -m "Add new page: Your Page Title"
   git push origin your-branch-name
   ```

## File Organization

The navigation **automatically mirrors your folder structure**. Organize files by topic:

- `getting-started/` - Introduction and setup guides
- `guides/` - How-to guides and tutorials
- `reference/` - API docs, configuration, etc.
- `blog/` - News and updates (if using blog plugin)

**Folders become collapsible sections** in the navigation sidebar. Files in folders appear as pages under those sections.

## Naming Conventions

- Use lowercase with hyphens: `my-new-page.md`
- Keep names descriptive but concise
- The folder structure **is** the navigation structure - they match automatically

## Adding Tags

Tags help users find related content:

```markdown
---
tags:
  - api
  - authentication
  - security
---
```

Then add the page to `tags.md` or let the tags plugin handle it automatically.

## Preview Your Changes

Before submitting:

1. **Local preview:**
   ```bash
   mkdocs serve
   ```
   Visit http://127.0.0.1:8000

2. **GitHub preview:**
   - Create a pull request
   - GitHub Actions will build a preview (if configured)

## Need Help?

- See [Writing Documentation](writing-docs.md) for formatting tips
- Check existing pages for examples
- Review the [Contributing Guide](../../CONTRIBUTING.md)
