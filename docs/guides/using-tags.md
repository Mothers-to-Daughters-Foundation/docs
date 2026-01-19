---
title: Using Tags
tags:
  - guide
  - tags
  - metadata
  - organization
categories:
  - Guides
---

# Using Tags

Tags help organize and discover related content across the documentation.

## What are Tags?

Tags are keywords that categorize your content. They make it easier to:

- Find related pages
- Group content by topic
- Discover documentation you might not know exists

## Adding Tags to a Page

Add tags in the front matter of your Markdown file:

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

Content here...
```

## Tag Best Practices

1. **Be consistent** - Use the same tag names across related pages
2. **Don't over-tag** - 3-5 tags per page is usually enough
3. **Use specific tags** - "authentication" is better than "stuff"
4. **Check existing tags** - Reuse tags that already exist

## Common Tags

Here are some suggested tags you might use:

- `getting-started` - For beginner-friendly content
- `api` - API-related documentation
- `configuration` - Setup and configuration guides
- `troubleshooting` - Problem-solving guides
- `reference` - Reference documentation
- `guide` - Step-by-step guides
- `tutorial` - Learning materials

## Viewing Tagged Content

1. Visit the [Tags page](../tags.md) to see all tags
2. Click on a tag to see all pages with that tag
3. Use the search bar to find content by tag name

## Categories

Categories are broader groupings that help organize content. Add them alongside tags:

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

### Categories vs Tags

- **Categories**: Broad groupings (1-2 per page)
  - Examples: `Getting Started`, `Guides`, `Reference`, `News`
- **Tags**: Specific topics (3-5 per page)
  - Examples: `api`, `authentication`, `troubleshooting`

Categories help organize content by type, while tags help find specific topics.

## Viewing Tagged Content

### Tag Index Page

Visit the [Tags page](../tags.md) to:
- See all tags used across the documentation
- Click any tag to see all pages with that tag
- Discover related content

### On Individual Pages

- Tags appear above the page title
- Click any tag to see all related pages
- Tags are also searchable

## Need Help?

- See [Tags and Categories Reference](tags-reference.md) for complete documentation
- Check [Adding New Pages](adding-pages.md) for how to create pages with tags
- Visit the [Tags page](../tags.md) to see existing tags
- Review existing pages for tag usage examples
