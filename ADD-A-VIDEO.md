# Add a video to the blog

The site is static, so videos are hosted on YouTube and embedded on the site. To publish one:

1. Upload the video to YouTube and copy its 11-character video ID from the URL. For `https://www.youtube.com/watch?v=abcdefghijk`, the ID is `abcdefghijk`.
2. Open `videos/videos.json` and add an object to the array. Keep the comma between entries:

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

3. Save and push the change to `main`. The GitHub Pages workflow publishes the update automatically.

The newest video should be the first object in the list. Use the date format `YYYY-MM-DD`. The embed uses YouTube's privacy-enhanced `youtube-nocookie.com` host.
