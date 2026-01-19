---
title: Navigation System
tags:
  - guide
  - navigation
  - system
categories:
  - Guides
---

# Navigation System

This guide explains how the auto-generated navigation system works.

## Overview

The navigation sidebar **automatically generates from your folder structure**. This means:

- ✅ **No manual configuration** - Just create files in folders
- ✅ **Collapsible folders** - Folders become expandable sections
- ✅ **Current page highlighting** - Active page is automatically highlighted
- ✅ **Instant updates** - New pages appear automatically

## How It Works

### Folder Structure → Navigation

Your folder structure directly maps to the navigation:

```
docs/
├── guides/
│   ├── writing-docs.md
│   └── adding-pages.md
```

Becomes:

```
📁 Guides
  📄 Writing Documentation
  📄 Adding New Pages
```

### Features

#### 1. Collapsible Folders

All folder sections are collapsible. Click the folder icon to expand/collapse.

#### 2. Current Page Highlighting

The current page is automatically highlighted in the navigation. The Material theme tracks your location as you navigate.

#### 3. Auto-Expansion

When you visit a page, its parent sections automatically expand to show the current page.

#### 4. Instant Navigation

Navigation uses instant loading - pages load without full page refreshes for a smooth experience.

## Controlling Navigation

### Automatic Mode (Default)

By default, all `.md` files in a folder are included automatically in alphabetical order.

### Using .pages Files

Create a `.pages` file in any directory to control:

- **Section title** - Custom name for the folder
- **Page order** - Specify exact order of pages
- **Hide files** - Only show specific files

Example `.pages` file:

```yaml
# docs/guides/.pages
title: Guides  # Custom section title

nav:
  - writing-docs.md      # Explicit order
  - adding-pages.md
  - using-tags.md
```

## Best Practices

### 1. Organize by Topic

Group related content in folders:
- `getting-started/` - Beginner content
- `guides/` - How-to guides
- `reference/` - API docs, specs

### 2. Use Descriptive Names

Folder and file names appear in navigation:
- ✅ `user-guide/` → "User Guide"
- ❌ `stuff/` → "Stuff"

### 3. Keep Structure Flat

Avoid deep nesting (2-3 levels max):
- ✅ `docs/guides/advanced/`
- ❌ `docs/guides/advanced/optimization/performance/`

### 4. Consistent Naming

- Folders: `lowercase-with-hyphens/`
- Files: `lowercase-with-hyphens.md`

## Adding a New Section

1. Create the folder: `docs/my-new-section/`
2. Add a `.pages` file (optional) for custom title
3. Add files to the folder
4. Update `docs/.pages` to include the new section (if you want to control order)

The section appears automatically!

## Troubleshooting

### Page Not Appearing?

- Check it's a `.md` file
- Verify it's in the `docs/` directory
- Check if a `.pages` file is hiding it
- Ensure the folder is listed in parent `.pages` file

### Wrong Order?

Create or edit the `.pages` file in that directory to specify order.

### Section Not Collapsible?

This should work automatically. If not, check that `navigation.sections` is enabled in `mkdocs.yml` (it is by default).

### Current Page Not Highlighted?

This should work automatically. If not, check that `navigation.tracking` is enabled in `mkdocs.yml` (it is by default).

## Technical Details

The navigation system uses:

- **mkdocs-awesome-pages-plugin** - Auto-generates navigation from filesystem
- **Material for MkDocs** - Provides collapsible sections and highlighting
- **.pages files** - Optional configuration for fine control

## Need Help?

- See [Folder Organization](folder-organization.md) for detailed folder structure guidance
- Check [Adding New Pages](adding-pages.md) for step-by-step instructions
- Review existing folders for examples
