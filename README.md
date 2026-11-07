# Pullayya Gari Cement Kottu · Google review page

A single-page "Share your experience" page for **పుల్లయ్య గారి సిమెంట్ కొట్టు** (Pullayya Gari Cement Kottu), a cement, paint and hardware shop in Gunupudi, Bhimavaram. A customer scans a QR code, taps a few options, edits a short draft and posts it on Google.

Live page (after GitHub Pages is on): https://chakravarthiperumalla.github.io/pullayagaricement-googlereview/

## How it works

1. The customer taps a **star rating**.
2. They tap **what they bought** (cement, paint, waterproofing, adhesives / sealants, hardware).
3. They tap **what was good** (4–5 stars) or **what could be better** (1–3 stars).
4. A draft review appears in **English or తెలుగు**. They can edit it freely, or tap **↻ New draft** for different wording.
5. **Copy & open Google reviews** copies the text and opens the shop's review box on Google. They paste it, confirm their stars and post.

The draft only contains what the customer ticked, and every rating leads to the same Google button. Please keep it that way: Google's policies do not allow filtering unhappy customers away from reviews, offering rewards for reviews, or posting reviews that do not reflect a real purchase.

The page also has an about card, contact icons (call, WhatsApp, Google listing, directions) and a "Visit the store" card. It is marked `noindex`, so search engines will not list it.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole page: HTML, CSS and JavaScript in one file. The logo is embedded, so it works on its own. |

No build step and no dependencies. Only the Google Fonts (Plus Jakarta Sans, Noto Sans Telugu) load from the internet.

## Deploy on GitHub Pages

1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch `main` and folder `/ (root)`, then save.
4. After a minute the page is live at the URL above. Point the shop's QR code at that URL.

## Shop details used in the page

| Item | Value |
| --- | --- |
| Address | 18-10-3, Gandhi Nagar, Gunupudi, Bhimavaram, Andhra Pradesh 534201 |
| Phone / WhatsApp | +91 81799 51999 |
| Hours (per Google listing) | 7:30 AM – 7:30 PM, may differ on festival days |
| Coordinates | 16.5412239, 81.5264281 |
| Google Maps CID | `12673521240897900903` |
| Google Place ID | `ChIJYXtqRQDTNzoRZ1EW4Wtk4a8` |

The review button uses `https://search.google.com/local/writereview?placeid=<Place ID>`, which opens the write-a-review box for this shop.

## Editing

Open `index.html` and search for:

- `placeid=` to change the Google Place ID (two links).
- `918179951999` to change the phone or WhatsApp number (several links).
- `const BOUGHT`, `const POS` and `const NEG` in the script to change the tappable options.
- `var T = {` for the sentence banks that build the English and Telugu drafts. Each list has a few wordings, and "New draft" cycles through them.
- `--orange` and `--char` at the top of the CSS for the brand colours (taken from the shop logo).

## Before sharing widely

- Confirm that 81799 51999 is on WhatsApp. The current Google listing shows no phone number, so this number comes from the shop's earlier listing.
- The logo was captured from the shop's Google Maps photos at 390 × 315 px. Replace the embedded image with the owner's original file for a sharper result.
- Read the Telugu wording with a Telugu speaker before printing the QR.
