# YTviewer
View yt videos

## Comments

Open **Comments** under the player to read a video's comments (sorted by Top or Newest, with replies).
Comments come from the YouTube Data API, which needs an API key. Set one up once for the whole site and nobody gets asked for one:

1. In the [Google Cloud console](https://console.cloud.google.com/), create a project (or pick an existing one).
2. Go to **APIs & Services → Library**, search for **YouTube Data API v3**, and enable it.
3. Go to **APIs & Services → Credentials → Create credentials → API key**.
4. Edit the key:
   - **Application restrictions → Websites**: add your site's domain followed by `/*`, e.g. `https://yourname.github.io/*`. Use just the domain, not the page's path: the page only tells Google which domain it's on.
   - **API restrictions → Restrict key**: pick **YouTube Data API v3**.
5. In `index.html`, put the key in `var SITE_API_KEY = "";` near the top of the script.

The key is visible in the page's source; that can't be avoided on a site without a server, and it's why step 4 matters.
The API is free: the key gets 10,000 units a day, each page of comments or replies costs 1 unit, and when they run out comments pause until the next day.

If `SITE_API_KEY` is left empty, the Comments panel asks each browser for its own key instead and saves it there.
