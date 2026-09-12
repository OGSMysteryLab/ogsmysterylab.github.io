# OGS Mystery Lab — Sources site

Free website that lists the sources for every video, with a link to the video.
Hosted on GitHub Pages at **https://ogsmysterylab.github.io** (free, your own account).

## Put it online (one time, ~5 minutes)

1. Go to github.com and sign in (or make a free account). Create a new **public** repository named exactly `ogsmysterylab.github.io` (if your GitHub username is different, name it `<your-username>.github.io`).
2. Upload these three files into it: `index.html`, `episodes.json`, `README.md` (drag them into the repo page → "Add file" → "Upload files" → Commit). Or with Git:
   ```
   git clone https://github.com/<your-username>/<your-username>.github.io
   copy the three files in
   git add . && git commit -m "Sources site" && git push
   ```
3. Repo → Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)` → Save.
4. Wait 1–2 minutes. The site is live at `https://<your-username>.github.io`.
5. Put that address as the first link on your YouTube channel page (the first link is the one viewers see), in your Linktree, and in your TikTok/Instagram bio.

## Add a video (every upload)

Open `episodes.json` and add one block at the top of the list. Every block except the last one ends with a comma.

```json
{
  "id": "vikings-horns",                       ← short slug, used in the link: yoursite/#vikings-horns
  "ep": 2,                                     ← episode number
  "format": "MYTH",                            ← FACT, MYTH or WHATIF
  "title": "Did Vikings wear horned helmets?",
  "claim": "One line: what the video asks.",
  "verdict": "BUSTED",                         ← optional, MYTH only
  "date": "2026-09-13",
  "youtube": "https://youtube.com/shorts/XXXXXXXX",
  "sources": [
    { "type": "book", "title": "Title of the source", "publisher": "Who published it", "url": "https://...", "note": "optional" },
    { "type": "paper", "title": "...", "publisher": "...", "url": "https://..." }
  ]
}
```

`type` can be: paper, book, archive, news, official, website.
Leave `"sources": []` empty and the page shows "sources are in the video description" until you add them.

Commit/push the file and the site updates itself. No rebuild, no tools.

## Deep link per video

Each episode has its own link: `https://<your-username>.github.io/#gate-to-hell`.
Paste it in the description of regular videos. (Links in Shorts descriptions are not clickable on YouTube — write "Sources: first link on the channel page" there instead.)
