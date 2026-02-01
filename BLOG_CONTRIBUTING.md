# Contributing Blog Posts to Tinkerbell.org

This guide explains how to add a blog post to the Tinkerbell website.

## Quick Start

1. Create a new Markdown file in `content/blog/` with a descriptive filename:

   ```text
   content/blog/YYYY-MM-your-post-title.md
   ```

2. Add the required front matter (see below)

3. Write your content in Markdown

4. Submit a pull request

## Front Matter

Every blog post requires front matter at the top of the file. Here's a complete example:

```yaml
---
title: "Your Post Title"
date: 2026-01-31
description: "A brief summary of your post (displayed in post listings)"
author: "Your Name"
authorGithub: "your-github-username"
tags: ["tag1", "tag2"]
image: "/images/blog/your-image.png"
---
```

### Required Fields

| Field          | Description                                                              |
|----------------|--------------------------------------------------------------------------|
| `title`        | The title of your blog post                                              |
| `date`         | Publication date in `YYYY-MM-DD` format                                  |
| `description`  | A 1-2 sentence summary shown in post listings                            |
| `author`       | Your name as you want it displayed                                       |
| `authorGithub` | Your GitHub username (used to link to your profile and show your avatar) |
| `tags`         | List of relevant tags (e.g., `["release", "tutorial", "community"]`)     |

### Optional Fields

| Field   | Description                                            |
|---------|--------------------------------------------------------|
| `image` | Path to a hero/thumbnail image (relative to `static/`) |

## Adding Images

### Hero/Thumbnail Image

To add a featured image to your post:

1. Add your image to `static/images/blog/`
2. Reference it in your front matter:

   ```yaml
   image: "/images/blog/my-post-image.png"
   ```

Recommended image dimensions:

- Hero image: 1200×630px (16:9 aspect ratio)
- File formats: PNG, JPG, or WebP

### Inline Images

For images within your post content, place them in `static/images/blog/` and reference them in Markdown:

```markdown
![Alt text](/images/blog/screenshot.png)
```

## Tags

Use existing tags when possible to help readers find related content. Common tags include:

- `release` - Version announcements
- `announcement` - General announcements
- `tutorial` - How-to guides
- `community` - Community stories and updates
- `deep-dive` - Technical deep-dives

You can view all existing tags at `/tags/` on the website.

## Writing Guidelines

### Content

- **Be clear and concise** - Technical readers appreciate directness
- **Include code examples** - Use fenced code blocks with language hints
- **Add context** - Explain why something matters, not just what it is
- **Link to resources** - Reference documentation, GitHub issues, or related posts

### Formatting

- Use `##` for main sections, `###` for subsections
- Use bullet lists for quick points
- Use numbered lists for sequential steps
- Use code blocks for commands, configuration, and code snippets

### Code Blocks

Use fenced code blocks with language identifiers:

````markdown
```yaml
apiVersion: tinkerbell.org/v1alpha1
kind: Hardware
metadata:
  name: example
```
````

## Example Post

Here's a minimal complete example:

```markdown
---
title: "Getting Started with Tinkerbell Workflows"
date: 2026-02-15
description: "Learn how to create your first Tinkerbell workflow for bare metal provisioning."
author: "Jane Developer"
authorGithub: "janedev"
tags: ["tutorial", "workflows"]
---

In this post, we'll walk through creating your first Tinkerbell workflow.

## Prerequisites

Before you begin, make sure you have:

- A running Tinkerbell stack
- At least one registered Hardware resource

## Creating a Workflow

First, create a Template...

[rest of your content]
```

## Submitting Your Post

1. Fork the [tinkerbell.org repository](https://github.com/tinkerbell/tinkerbell.org)
2. Create a new branch for your post
3. Add your blog post file and any images
4. Test locally with `hugo server -D`
5. Submit a pull request

### Local Testing

To preview your post locally:

```bash
# Clone the repo (or your fork)
git clone https://github.com/tinkerbell/tinkerbell.org.git
cd tinkerbell.org

# Start the development server
hugo server -D

# View at http://localhost:1313/blog/
```

## Questions?

If you have questions about contributing blog posts:

- Open an issue on the [tinkerbell.org repository](https://github.com/tinkerbell/tinkerbell.org/issues)
- Ask in the [#tinkerbell Slack channel](https://cloud-native.slack.com/archives/C01SRB41GMT)
