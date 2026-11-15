# Vaccine Planner – website

Static website for the Android app **Vakcināciju kalendārs un plāns / Vaccine Planner** (`lv.sensora.vaccine`):
landing page and privacy policy. Plain HTML + CSS, no build step, no external requests (the Montserrat font is
self-hosted, OFL licence in `assets/fonts`).

| File | Content |
|---|---|
| `index.html` | Landing page (Latvian) |
| `en.html` | Landing page (English) |
| `privacy.html` | Privacy policy, Latvian + English on one page (`#lv`, `#en`) – this URL goes into Google Play Console |
| `assets/` | `style.css`, app icon, font |

## Publish on GitHub Pages

1. On GitHub (account `MasterAGB`) create a **new public** repository named **`vaccine-planner`**.
   Do **not** use the private app repository: it contains the signing keystore.
2. Upload all files of this folder to the repository root (including the hidden `.nojekyll` file).
3. Repository → Settings → Pages → Source: *Deploy from a branch*, branch `main`, folder `/ (root)` → Save.
4. After a minute the site is at `https://masteragb.github.io/vaccine-planner/`.
5. Play Console → Policy → App content → Privacy policy: `https://masteragb.github.io/vaccine-planner/privacy.html`

The app (1.11+) opens the same URL from Informācija → Privātuma politika. It reads the URL from the translations
sheet (key `PrivacyPolicyUrl`, default in `OpenPrivacyPolicyButton.DefaultUrl`). If you use another repository
name, change that key in `VaccineAppLocalization.xlsx` – no app update needed.

## Google Play link

Done 2026-11-13: the app has been live on Google Play since 2026-11-11 (version 1.11), and both landing pages
(`index.html`, `en.html`) link to `https://play.google.com/store/apps/details?id=lv.sensora.vaccine`.

## When the app changes

Update `privacy.html` if the app starts collecting or sending any data (accounts, analytics, crash reporting, ads,
notifications, cloud sync), and change the "Effective" date. Keep it consistent with the Play Console *Data safety* form.
