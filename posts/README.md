# Gyatbox Blog System

This folder contains all blog posts and the blog system configuration.

## Files

- **`posts.json`** - Index of all blog posts (metadata only)
- **`blog-post-styles.css`** - Shared styles for all blog post pages
- **`_template.html`** - Reusable template for creating new blog posts
- **Individual post files** - Each blog post is a standalone HTML file

## How to Add a New Blog Post

### Step 1: Create the HTML file

1. Copy `_template.html` and rename it using your post's slug (e.g., `my-new-post.html`)
2. Open the new file and edit the following sections marked with `<!-- EDIT: -->`:
   - Page title in `<title>` tag
   - Meta description
   - Post date in the meta section
   - Post title in the `<h1>` tag
   - Post content in the `.post-content` section

### Step 2: Add metadata to posts.json

Add a new entry to the `posts.json` array:

```json
{
  "title": "Your Post Title",
  "slug": "your-post-slug",
  "date": "2025-02-15",
  "description": "A short description of your post (1-2 sentences)."
}
```

**Important:**

- The `slug` must match your HTML filename (without `.html`)
- Use the format `YYYY-MM-DD` for dates
- Posts are automatically sorted by date (newest first)

### Step 3: Push to GitHub

Once you commit and push your changes to GitHub Pages, the blog will automatically display your new post.

## Content Formatting

The blog post template supports:

- **Headings**: `<h2>` and `<h3>` for sections
- **Paragraphs**: Standard `<p>` tags
- **Lists**: Bulleted (`<ul>`) and numbered (`<ol>`)
- **Links**: `<a href="...">link text</a>`
- **Inline code**: `<code>code here</code>`
- **Code blocks**: `<pre><code>code block</code></pre>`

## Example Workflow

1. Copy `_template.html` → `getting-started.html`
2. Edit the content in `getting-started.html`
3. Add this to `posts.json`:
   ```json
   {
     "title": "Getting Started Guide",
     "slug": "getting-started",
     "date": "2025-02-10",
     "description": "Everything you need to know to get started with Gyatbox."
   }
   ```
4. Commit and push to GitHub

That's it! Your new post will appear on the blog page automatically.
