# Add an article or video to the blog

The mixed blog at `/blog/` lists articles and videos together, newest first. It runs as static files, so no database or server is needed.

## Publish an article

1. Copy `blog/posts/plantilla.html` into a new folder such as `blog/posts/cyber-risk-basics/index.html`.
2. Replace the template title, description, canonical URL, date, introduction, category, and body with your article content. Add headings, paragraphs, links, images, or code samples in the `.content` section.
3. Add this entry to `blog/articles.json`, with the newest post at the top:

   ```json
   [
     {
       "title": "Cyber risk basics for small businesses",
       "date": "2026-10-16",
       "summary": "A short introduction to the practical ideas in this article.",
       "url": "/blog/posts/cyber-risk-basics/",
       "tags": ["Cybersecurity", "SMEs"]
     }
   ]
   ```

## Publish a video

Upload it to YouTube and copy its 11-character video ID from the URL. Add an entry to `videos/videos.json`:

```json
[
  {
    "youtubeId": "abcdefghijk",
    "title": "A clear title for the video",
    "date": "2026-10-16",
    "description": "A short summary of what viewers will learn."
  }
]
```

Use the `YYYY-MM-DD` date format. After committing and pushing the changes to `main`, GitHub Actions deploys the static site to Pages.
