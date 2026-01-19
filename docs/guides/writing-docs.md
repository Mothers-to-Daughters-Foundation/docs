---
title: Writing Documentation
tags:
  - guide
  - documentation
  - markdown
  - writing
categories:
  - Guides
---

# Writing Documentation

This guide explains how to write and format documentation for this site.

## Markdown Basics

All documentation is written in Markdown. Here are the essentials:

### Headers

```markdown
# Level 1 Header
## Level 2 Header
### Level 3 Header
```

### Text Formatting

```markdown
**bold text**
*italic text*
`code inline`
```

### Lists

```markdown
- Unordered list item
- Another item

1. Ordered list item
2. Another item
```

### Links

```markdown
[Link text](path/to/page.md)
[External link](https://example.com)
```

### Code Blocks

````markdown
```python
def hello():
    print("Hello, World!")
```
````

### Images

```markdown
![Alt text](images/example.png)
```

## Front Matter

Add metadata at the top of your file using YAML front matter:

```markdown
---
title: Your Page Title
tags:
  - documentation
  - guide
categories:
  - Guides
---

# Your Page Title

Your content here...
```

### Available Front Matter Fields

- `title` - Page title (if different from the first header)
- `tags` - List of tags for categorization (appears above page title, clickable)
- `categories` - List of categories for broader content organization

## Best Practices

1. **Use clear headings** - Structure your content with descriptive headers
2. **Keep it simple** - Write for your audience's level
3. **Add examples** - Code examples and screenshots help a lot
4. **Link related content** - Connect related pages with links
5. **Use tags** - Tag your content for better discoverability

## Admonitions

You can use special callout boxes:

```markdown
!!! note "Note Title"
    This is a note.

!!! tip
    This is a tip.

!!! warning
    This is a warning.

!!! danger
    This is a danger notice.
```

## Tables

```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Data 1   | Data 2   | Data 3   |
| Data 4   | Data 5   | Data 6   |
```

## Need More Help?

- Check the [Material for MkDocs documentation](https://squidfunk.github.io/mkdocs-material/reference/)
- Look at existing pages for examples
- Ask in your organization's communication channel
