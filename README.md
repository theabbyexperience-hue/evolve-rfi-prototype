# Evolve Owner RFI: concept prototype

A redesign concept for Evolve's owner "request for information" (RFI) flow, made for a product design case study. This is a concept, not Evolve's live site: nothing entered in the forms is sent anywhere.

## What's here

| Path | What it is |
|---|---|
| `index.html` (site homepage) | Presentation version: the mobile prototype plus a design summary page (what causes the drop-off, how the design improves it, expected lift and validation, what to try if testing doesn't show improvement, AI workflow). Case notes and scenarios open from the "Case notes" button. Open the summary from Case notes, from any "You're all set" screen, or directly at `/#summary`. |
| `side-by-side/index.html` | The phone flow next to an always-open case notes panel (scenarios, rationale for each screen, and the lead profile sales would see). Best on a computer. |
| `mobile/index.html` | Mobile-only version without the design summary. |
| `walkthrough/index.html` | Same as the homepage (kept so older links still work). |
| `hero.jpg`, `logo.png` | Images (each folder has its own copy so it works on its own). |

No build step and no dependencies: plain HTML, CSS and JavaScript. Fonts (Montserrat, Nunito) load from Google Fonts.

## The flow in one line

The first question splits owners into two paths. Owners who already have a listing paste one link and get an estimate in seconds; everyone else gets a short guided flow. Both show value before asking for a phone number, screen out poor fits early, and route the best leads to sales.

## Try it

Open `index.html` in a browser, or use the **Try these scenarios** buttons in the case notes to jump to: one listing, a host with 3 homes, a property manager account, an unreadable link, a private room, the guided flow, or the buyer exit.

## Deploy

**Netlify (quickest):** go to app.netlify.com → Add new site → Deploy manually, and drag this whole folder onto the page. The presentation version is the homepage (summary at `/#summary`), the side-by-side version is at `/side-by-side/` and the mobile-only version at `/mobile/`.

**GitHub:**
```
git init
git add .
git commit -m "Evolve owner RFI concept prototype"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```
To publish from GitHub, either connect the repo in Netlify (Add new site → Import an existing project; no build command, publish directory `/`), or turn on GitHub Pages (repo Settings → Pages → Deploy from branch → `main` / root).

## Assumptions

Listing data is simulated (in production it would come from a listing-data provider or the listing's public preview). Estimates, the ~25% property-manager fee, the 10+ listings rule and the lead-scoring weights are placeholders to be calibrated with Evolve's data. Drop-off figures (35% at contact, 30% at address) come from the case study brief.
