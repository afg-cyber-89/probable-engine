# Adrianne’s Birthday Night — GitHub Pages version

## Files

- `index.html` — upload to the root of your GitHub repository.
- `hero.png` — keep this exact filename in the same directory as `index.html`.
- `Code.gs` — Google Apps Script backend that writes RSVP responses to Google Sheets.

## 1. Configure the webpage

Open `index.html` and edit the `EVENT_DATA` block near the bottom. Replace the dinner location and both Google Maps URLs as needed.

Then replace:

```js
const APPS_SCRIPT_WEB_APP_URL =
  'PASTE_YOUR_APPS_SCRIPT_WEB_APP_URL_HERE';
```

with the deployed Apps Script `/exec` URL.

## 2. Configure Google Apps Script

1. Create or open the Google Sheet that should receive responses.
2. Copy its spreadsheet ID from the URL.
3. Create a new Apps Script project and paste in `Code.gs`.
4. Replace `PASTE_YOUR_GOOGLE_SHEET_ID_HERE` with the spreadsheet ID.
5. Deploy as **Web app**:
   - Execute as: **Me**
   - Who has access: **Anyone**
6. Copy the deployed `/exec` URL into `index.html`.

Whenever `Code.gs` is changed, create a new deployment version and update the URL if Google gives you a new one.

## 3. Publish with GitHub Pages

1. Upload `index.html` and `hero.png` to the repository root.
2. Go to **Settings → Pages**.
3. Choose **Deploy from a branch**.
4. Select the branch and `/ (root)` folder.
5. Save and open the generated GitHub Pages URL.

## Phone field

The page uses `intl-tel-input` v27.0.10 from jsDelivr. It includes the complete country list, flags, calling codes, country search, formatting and validation. The saved `phone` value is in international E.164 format.
