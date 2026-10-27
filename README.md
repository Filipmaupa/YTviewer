# YTviewer
View yt videos

## Comments

Open **Comments** under the player to read a video's comments (sorted by Top or Newest, with replies).
Comments come from the YouTube Data API, so the first time you open them you'll be asked for a free API key:

1. In the [Google Cloud console](https://console.cloud.google.com/), create a project (or pick an existing one).
2. Go to **APIs & Services → Library**, search for **YouTube Data API v3**, and enable it.
3. Go to **APIs & Services → Credentials → Create credentials → API key**.
4. Recommended: edit the key and restrict it to your site under **Website restrictions**, and to **YouTube Data API v3** under **API restrictions**.
5. Paste the key into the Comments panel. It's stored only in that browser's local storage.

The free quota is 10,000 units a day; each page of comments or replies costs 1 unit.
