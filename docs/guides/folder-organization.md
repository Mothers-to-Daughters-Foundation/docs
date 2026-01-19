---
title: Folder Organization Guide
tags:
  - guide
  - navigation
  - organization
  - folders
categories:
  - Guides
---

# Folder Organization Guide

This guide explains how to organize your documentation files so they appear correctly in the auto-generated navigation.

## How Auto-Generated Navigation Works

The navigation sidebar **automatically mirrors your folder structure**:

- **Folders** → Collapsible sections in the sidebar
- **Markdown files** → Pages in the navigation
- **Subfolders** → Nested sections

No manual configuration needed! Just organize your files, and the navigation updates automatically.

## Folder Structure Examples

### Simple Structure

```
docs/
├── index.md                    → Home page
├── getting-started/
│   ├── overview.md            → Page under "Getting Started"
│   └── quick-start.md         → Page under "Getting Started"
└── guides/
    ├── writing-docs.md        → Page under "Guides"
    └── adding-pages.md        → Page under "Guides"
```

**Result in Navigation:**
```
📄 Home
📁 Getting Started
  📄 Overview
  📄 Quick Start
📁 Guides
  📄 Writing Documentation
  📄 Adding New Pages
```

### Nested Structure

```
docs/
├── guides/
│   ├── beginner/
│   │   ├── first-steps.md     → Nested under Guides > Beginner
│   │   └── basics.md
│   └── advanced/
│       └── optimization.md    → Nested under Guides > Advanced
```

**Result in Navigation:**
```
📁 Guides
  📁 Beginner
    📄 First Steps
    📄 Basics
  📁 Advanced
    📄 Optimization
```

## Controlling Navigation

### Automatic (Default)

By default, all `.md` files in a folder are automatically included in alphabetical order. Just create files, and they appear!

### Using .pages Files

To control the order or hide specific files, create a `.pages` file in any directory:

```yaml
# docs/guides/.pages
title: Guides  # Custom title for the section

nav:
  - writing-docs.md      # Explicit order
  - adding-pages.md
  - using-tags.md
  # Files not listed are hidden
```

### .pages File Options

**Basic .pages file:**
```yaml
title: Section Title
```

**With explicit ordering:**
```yaml
title: Section Title
nav:
  - first-page.md
  - second-page.md
  - subfolder/        # Include entire subfolder
```

**Hide files:**
```yaml
# Only listed files appear
nav:
  - visible-page.md
  # other-page.md won't appear
```

## Best Practices

### 1. Organize by Topic

Group related content in folders:
- `getting-started/` - For beginners
- `guides/` - How-to guides
- `reference/` - API docs, specs
- `troubleshooting/` - Problem-solving

### 2. Use Descriptive Folder Names

Folder names become section titles in navigation:
- ✅ `user-guide/` → "User Guide"
- ✅ `api-reference/` → "API Reference"
- ❌ `stuff/` → "Stuff" (not descriptive)

### 3. Keep It Flat When Possible

Avoid deep nesting (more than 2-3 levels):
- ✅ `docs/guides/advanced/`
- ❌ `docs/guides/advanced/optimization/performance/`

### 4. Use Consistent Naming

- Folders: lowercase with hyphens (`user-guide/`)
- Files: lowercase with hyphens (`my-page.md`)

### 5. Index Pages

Create `index.md` in folders to serve as landing pages:
```
docs/
└── guides/
    ├── index.md          → Landing page for Guides section
    ├── writing-docs.md
    └── adding-pages.md
```

## Adding a New Section

To add a new top-level section:

1. **Create the folder:**
   ```bash
   mkdir docs/your-new-section
   ```

2. **Add a .pages file (optional):**
   ```yaml
   # docs/your-new-section/.pages
   title: Your New Section
   ```

3. **Add files:**
   ```bash
   touch docs/your-new-section/first-page.md
   ```

4. **Update root .pages (if needed):**
   ```yaml
   # docs/.pages
   nav:
     - index.md
     - getting-started/
     - guides/
     - your-new-section/  # Add here
     - reference/
   ```

The section appears automatically in the navigation!

## Common Patterns

### Pattern 1: Simple Documentation Site

```
docs/
├── index.md
├── getting-started/
├── guides/
└── reference/
```

### Pattern 2: Product Documentation

```
docs/
├── index.md
├── installation/
├── user-guide/
│   ├── basics/
│   └── advanced/
├── api/
└── troubleshooting/
```

### Pattern 3: Knowledge Base

```
docs/
├── index.md
├── articles/
│   ├── category-a/
│   └── category-b/
├── tutorials/
└── faq/
```

## Troubleshooting

### Page Not Appearing?

1. Check the file is a `.md` file
2. Verify it's in the `docs/` directory
3. Check if a `.pages` file is hiding it
4. Ensure the folder is listed in parent `.pages` file

### Wrong Order?

Create or edit the `.pages` file in that directory to specify order explicitly.

### Section Title Wrong?

Edit the `.pages` file and set a `title:` field, or rename the folder.

## Need Help?

- See [Adding New Pages](adding-pages.md) for step-by-step instructions
- Check existing folders for examples
- Review the [Contributing Guide](../../CONTRIBUTING.md)
