# 🎬 Movie Night Picker

A dark, cinematic web app that uses Claude AI to recommend films for family movie night. Set your preferences — genre, era, BBFC rating, IMDb score, mood, runtime — and get five tailored picks instantly.

Built as a single HTML file with no dependencies, hosted on GitHub Pages.

## Features

- Filter by genre, decade, BBFC age certificate, IMDb score, runtime, and mood/vibe
- Results show IMDb rating, BBFC certificate, Common Sense Media age recommendation, and runtime
- Personalised "why this film?" note for each pick
- Dark, cinematic UI
- Your API key is stored locally in your browser — never sent anywhere except the Anthropic API

## Setup

### 1. Fork or clone this repo

```bash
git clone https://github.com/YOUR_USERNAME/movie-picker.git
```

### 2. Enable GitHub Pages

- Go to your repo → **Settings** → **Pages**
- Under *Source*, select **Deploy from a branch**
- Choose **main** branch, **/ (root)** folder
- Click **Save**

Your app will be live at `https://YOUR_USERNAME.github.io/movie-picker` within a minute or two.

### 3. Get an Anthropic API key

- Visit [console.anthropic.com](https://console.anthropic.com)
- Sign in or create a free account
- Go to **API Keys** and create a new key
- Copy the key (starts with `sk-ant-…`)

### 4. Use the app

- Open the GitHub Pages URL
- Paste your API key when prompted — it's saved in your browser and you won't be asked again
- Set your preferences and hit **Find tonight's film**

## Updating the app

Any changes pushed to the `main` branch will automatically redeploy to GitHub Pages within ~30 seconds.

```bash
git add index.html
git commit -m "Update movie picker"
git push
```

## Tech

- Plain HTML, CSS, and JavaScript — no build step, no dependencies
- Calls the [Anthropic Messages API](https://docs.anthropic.com/en/api/messages) directly from the browser
- API key stored in `localStorage`
