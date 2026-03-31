# AFFiNE Template Downloader

A single-file HTML tool that makes it easy to download [AFFiNE](https://affine.pro) templates for import into self-hosted instances.

## The Problem

Importing templates into a self-hosted AFFiNE instance requires manually:
1. Finding the template on affine.pro
2. Copying the "Use this template" link
3. Extracting the `snapshotUrl` parameter from the URL
4. URL-decoding it
5. Downloading the ZIP from the CDN
6. Importing the snapshot in your AFFiNE app

This tool reduces that to **copy link, paste, done**.

## Usage

### 1. Download the HTML file

Download [`index.html`](index.html) and open it in your browser (or [use it online via GitHub Pages](#github-pages)).

### 2. Copy the template link from AFFiNE

On any [AFFiNE template page](https://affine.pro/templates), **right-click the "Use this template" button** and select **Copy Link Address**.

The link will look something like:
```
https://app.affine.pro/template/import?workspaceId=...&docId=...&name=Pokemon+Team+Planner&snapshotUrl=https%3A%2F%2Fcdn.affine.pro%2Ftemplate-snapshots%2F...zip
```

### 3. Paste and download

Paste the link into the tool. The ZIP file downloads **automatically on paste** — no button click needed.

### 4. Import into AFFiNE

In your self-hosted AFFiNE app:
1. Go to **Import** in the left sidebar
2. Select **Snapshot**
3. Choose the downloaded `.zip` file

## Features

- **Auto-download on paste** — paste the URL and the ZIP downloads immediately
- **Auto-clipboard read** — if you have a template URL copied, it auto-fills when you focus the input
- **Download history** — tracks your recent downloads (stored in localStorage)
- **Single HTML file** — no dependencies, no build step, no server required
- **Works offline** — once opened, no internet needed except for the actual download

## GitHub Pages

You can also use this tool directly in your browser without downloading:

**https://wilky00.github.io/affine-template-downloader/**

## License

MIT
