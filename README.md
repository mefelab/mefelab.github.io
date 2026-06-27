# MEFE Lab website

Static website for the **Microbial Ecology & Functional Engineering Lab (MEFE)** /
미생물생태 기능설계 연구실, led by Prof. Kiseok Lee — Department of Systems Biology,
Yonsei University (opening March 2027).

Plain HTML + CSS + a little JS. No build step. Edit the files and push.
Colors use the **Yonsei blue** palette.

## Pages (nav order)
1. `index.html` — Home
2. `research.html` — Research
3. `mission.html` — Mission
4. `team.html` — Team
5. `pi.html` — PI (Kiseok Lee bio)
6. `papers.html` — Papers (links to Google Scholar)
7. `gallery.html` — Gallery
8. `join.html` — Join Us (includes contact info)

`assets/styles.css` — shared styles · `assets/nav.js` — mobile menu

---

## ⚠️ One thing to add: the PI photo
The PI pages reference **`assets/kiseok.jpg`** but the image file isn't included yet
(I couldn't save it from chat). Save your headshot — I recommend the smiling one with
glasses and the navy pinstripe suit — as **`assets/kiseok.jpg`** in this folder. Until
then, the PI/Team pages show a "KL" placeholder tile automatically.

To add gallery photos later: drop files in `assets/gallery/` and replace the placeholder
blocks in `gallery.html` (instructions are in an HTML comment there).

---

## Deploying to mefelab.github.io

### Option A — let me commit it for you
Install the **Engineering** plugin (the card I showed in chat) and connect GitHub.
Then create the `mefelab` account + a repo named `mefelab.github.io`, and ask me to push.

### Option B — do it yourself (no command line)
1. Sign up at github.com with username **`mefelab`** (use `kiseokkeithlee@gmail.com`).
2. Create a public repo named exactly **`mefelab.github.io`**.
3. On the repo page: **Add file → Upload files**, drag in everything from this folder
   (all `.html` files + the `assets/` folder), **Commit changes**.
4. **Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save.**
5. Live at **https://mefelab.github.io** in a minute or two.

### With git instead
```bash
cd "path/to/this/folder"
git init && git add . && git commit -m "Initial MEFE Lab website"
git branch -M main
git remote add origin https://github.com/mefelab/mefelab.github.io.git
git push -u origin main
```

---

## Other things to personalize
- **Yonsei email** — set to `kiseokkeithlee@gmail.com` with a "coming soon" note; update on `join.html` when you have it.
- **News** — edit the list in `index.html` as the lab grows.
- **Map** — `join.html` links to a Google Maps search; swap for your exact building when known.
- **Colors** — all in the `:root` block of `assets/styles.css` (change once, applies everywhere).

The Google Scholar link (`UcMtC88AAAAJ`) is already wired into every page and the Papers tab.
