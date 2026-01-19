# Tags and Categories Reference

Complete reference guide for using tags and categories in documentation.

## Quick Reference

### Basic Frontmatter

```markdown
---
title: Your Page Title
tags:
  - tag1
  - tag2
  - tag3
categories:
  - Category Name
---
```

## Tags

### What are Tags?

Tags are keywords that help organize and discover content. They appear:
- Above the page title on each page
- In the tag index page
- As clickable links to find related content

### Adding Tags

Add tags in the front matter of any Markdown file:

```markdown
---
title: API Authentication Guide
tags:
  - api
  - authentication
  - security
  - getting-started
---

# API Authentication Guide

Your content here...
```

### Tag Best Practices

1. **Be Consistent**
   - Use the same tag names across related pages
   - Check existing tags before creating new ones
   - Use lowercase or kebab-case: `api`, `getting-started`, `user-guide`

2. **Be Specific**
   - ✅ `authentication` (specific)
   - ❌ `stuff` (too vague)
   - ✅ `api-endpoints` (clear)
   - ❌ `things` (unclear)

3. **Don't Over-Tag**
   - 3-5 tags per page is usually enough
   - Focus on the most relevant topics
   - Too many tags reduce their usefulness

4. **Use Standard Tags**
   - `getting-started` - For beginner content
   - `api` - API-related documentation
   - `guide` - How-to guides
   - `reference` - Reference documentation
   - `troubleshooting` - Problem-solving guides
   - `configuration` - Setup and config
   - `tutorial` - Step-by-step learning

### Viewing Tagged Content

1. **Tag Index Page**
   - Visit the [Tags page](../tags.md)
   - See all tags and their associated pages
   - Click any tag to see all pages with that tag

2. **On Individual Pages**
   - Tags appear above the page title
   - Click a tag to see all related pages

3. **Search**
   - Use the search bar to find content by tag name
   - Tags are indexed and searchable

## Categories

### What are Categories?

Categories are broader groupings that help organize content into sections. They're useful for:
- Blog posts
- Content types
- Audience segments

### Adding Categories

```markdown
---
title: New Feature Announcement
tags:
  - feature
  - release
categories:
  - News
  - Updates
---
```

### Category Best Practices

1. **Use Consistently**
   - Define a set of allowed categories
   - Use the same category names across related content
   - Keep the list manageable (5-10 categories)

2. **Common Categories**
   - `Getting Started` - Introduction content
   - `Guides` - How-to guides
   - `Reference` - API docs, specs
   - `News` - Announcements
   - `Updates` - Change logs

3. **Categories vs Tags**
   - **Categories**: Broad groupings (few per page, 1-2 usually)
   - **Tags**: Specific topics (multiple per page, 3-5 usually)

## Examples

### Example 1: Getting Started Guide

```markdown
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

Content...
```

### Example 2: API Reference

```markdown
---
title: User API Endpoints
tags:
  - api
  - endpoints
  - users
  - reference
categories:
  - Reference
---

# User API Endpoints

Content...
```

### Example 3: Troubleshooting Guide

```markdown
---
title: Common Issues and Solutions
tags:
  - troubleshooting
  - problems
  - solutions
  - help
categories:
  - Guides
---

# Common Issues and Solutions

Content...
```

## Tag Index Pages

The tag index page (`tags.md`) automatically:
- Lists all tags used across the documentation
- Shows how many pages use each tag
- Provides links to view all pages with a specific tag

The tag index is auto-generated from all frontmatter tags in your documentation.

## Finding Related Content

### By Tag

1. Click any tag on a page or the tags index
2. See all pages that share that tag
3. Discover related content you might not have found otherwise

### By Category

Categories help you browse content by type:
- All "Getting Started" content
- All "Reference" documentation
- All "Guides"

## Troubleshooting

### Tags Not Appearing?

1. Check frontmatter syntax (must be valid YAML)
2. Ensure tags are in a list format: `- tag1`
3. Verify the tags plugin is enabled in `mkdocs.yml`
4. Rebuild the site: `mkdocs build`

### Tag Index Not Updating?

1. Ensure `tags.md` contains `<!-- material/tags -->`
2. Check that `tags_file: tags.md` is in `mkdocs.yml`
3. Rebuild the site

### Tags Not Clickable?

- Tags should be clickable by default
- Check that the tags plugin is properly configured
- Verify Material theme is being used

## Need Help?

- See [Using Tags](using-tags.md) for a beginner-friendly guide
- Check [Adding New Pages](adding-pages.md) for how to add tags to new pages
- Review existing pages for tag usage examples
