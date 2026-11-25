# Weekly Planner

A phone-first week planner (installable web app). Plan each day in time windows, keep load realistic, and protect weekly learning goals. No build step and no dependencies.

Files: `index.html` (the app), `manifest.webmanifest` (install info), `sw.js` (offline), `icons/`.

## Put it on your phone

The app must be served over **HTTPS** for "Install app" and offline to work. Any static host works. Easiest free option, GitHub Pages:

1. Create a new GitHub repository (it can be private only on paid plans; Pages on a free plan needs a public repo, which is fine because the app holds no data of yours).
2. Upload the contents of this folder (so `index.html` is at the repo root).
3. Repo Settings, Pages, deploy from branch `main`, folder `/ (root)`.
4. Open `https://<your-user>.github.io/<repo>/` on your phone.

Netlify Drop (drop.netlify.com) also works: drag this folder onto the page and you get an HTTPS link in seconds.

## Install

- **Android (Chrome):** menu, "Install app" (or "Add to Home screen").
- **iPhone (Safari):** Share button, "Add to Home Screen". It must be Safari.

## Your data

Everything is stored in the browser on that phone (localStorage), not on a server. Each device has its own plan.
Use Day tab, Windows, "Download backup" now and then, and "Restore backup" to move a plan to another device.
Clearing the browser's site data deletes the plan.

## Updating

Change `index.html`, redeploy, and bump `V` in `sw.js` (e.g. `planner-v2`) so installed copies refresh.

## Run locally

Serve the folder with any static server on `localhost` (service workers only run on localhost or HTTPS), e.g. `python -m http.server` in this folder.
