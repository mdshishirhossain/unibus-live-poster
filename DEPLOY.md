# How to Publish These Posters on GitHub Pages

You'll get **a free, public URL** that works from any device, anywhere.

> Result: `https://<your-username>.github.io/<repo-name>/`
> e.g. `https://mdshishirhossain.github.io/unibus-live-poster/`

---

## Step 1 — Create a new GitHub repository

1. Go to <https://github.com/new>
2. Repository name: `unibus-live-poster` (or anything you like — keep it short)
3. Visibility: **Public** (required for free GitHub Pages on Free tier)
4. ☐ Do **not** initialise with a README — we already have one
5. Click **Create repository**

GitHub will show you a quick-setup screen. Keep that tab open.

## Step 2 — Push the poster folder

Open a terminal **in the `posters/` folder** (where `README.md`, `index.html`, the two poster HTMLs, and `npi-logo.png` live):

```bash
cd D:/path/to/posters             # your local folder
git init
git add .
git commit -m "Initial poster + README"
git branch -M main
git remote add origin https://github.com/<your-username>/unibus-live-poster.git
git push -u origin main
```

Replace `<your-username>` with your GitHub username.

## Step 3 — Enable GitHub Pages

1. On the repository page on GitHub, click **Settings** (top-right tab)
2. In the left sidebar, click **Pages**
3. Under **Source**, choose **Deploy from a branch**
4. Branch: **`main`** · Folder: **`/ (root)`**
5. Click **Save**

GitHub will spend about 30–60 seconds publishing the site. Refresh the Pages screen — you'll see:

> Your site is live at `https://<your-username>.github.io/unibus-live-poster/`

Click that URL — you'll see the landing page (`index.html`), and from there you can click into either poster.

---

## Direct links you'll have after publishing

| What | URL |
|---|---|
| Landing page | `https://<user>.github.io/unibus-live-poster/` |
| Full Project poster | `https://<user>.github.io/unibus-live-poster/poster-1-full-project.html` |
| Mobile App poster | `https://<user>.github.io/unibus-live-poster/poster-2-app-overview.html` |
| Project documentation | `https://<user>.github.io/unibus-live-poster/README.md` *(view on the repo's main page instead — GitHub renders it nicely)* |

Share any of these with your supervisor, classmates, or the print shop.

---

## Optional polish

### Custom domain

If you own a domain (e.g. `unibus.live`), add a `CNAME` file in the repo with that domain inside, then point your DNS at GitHub's IPs. Free HTTPS via Let's Encrypt is automatic.

### Repo description &amp; topics

On the repo's main page, click the ⚙ icon next to **About** (top-right of the file list) and add:

- Description: *"Real-time university bus tracking platform · NPIUB Final Year Project 2026 · React Native + Expo + Node.js + Socket.IO"*
- Website: paste your Pages URL
- Topics: `react-native`, `expo`, `nodejs`, `socket-io`, `bus-tracking`, `university-project`, `bangladesh`, `npiub`

This makes the repo discoverable on GitHub search.

### Pin the repo on your profile

Go to your GitHub profile → **Customize your pins** → select this repo. It then appears prominently on your profile — great for sharing during job applications or your supervisor's review.

---

## Updating the posters later

Just edit the HTML files locally, commit, push:

```bash
git add .
git commit -m "Update poster content"
git push
```

GitHub Pages redeploys automatically in ~30 seconds.

---

## What if I want to print from the live URL?

Same workflow:

1. Open the live poster URL in Chrome
2. `Ctrl+P` → Save as PDF
3. Paper size: Custom **20 × 30 in** · Margins: **None** · Background graphics: **ENABLED**
4. Save → take to the print shop

The same printable PDF can be generated from the live URL or your local file — they're identical.
