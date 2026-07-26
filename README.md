# Adrianne Birthday RSVP — GitHub Pages version

## Repository root

Place these files in the GitHub repository root:

- `index.html`
- `hero.png`
- `README.md` (optional)

The Apps Script backend remains in Google Apps Script as `Code.gs`.

## Deploy the Apps Script backend

1. Replace the old Apps Script code with `Code.gs`.
2. Deploy as a Web app.
3. Execute as: **Me**.
4. Who has access: **Anyone**.
5. Copy the URL ending in `/exec`.

## Connect the GitHub page to Apps Script

In `index.html`, find:

```html
action="PASTE_YOUR_APPS_SCRIPT_EXEC_URL_HERE"
```

Replace it with your Apps Script `/exec` URL.

## Enable GitHub Pages

1. Repository **Settings**
2. **Pages**
3. Source: **Deploy from a branch**
4. Branch: `main`
5. Folder: `/ (root)`
6. Save

## Update event details

Search in `index.html` for:

- `Restaurant TB`
- the dinner Google Maps URL
- the OTO Google Maps URL
- `21st August 2026`
- `20:00`
- `TBD`
- `15th August 2026`

## Telephone input

The page uses `intl-tel-input` v29.1.2 and stores:

- country calling code
- ISO2 country code
- full E.164 phone number
