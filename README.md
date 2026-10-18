# Certificate Generator

A free, browser-based certificate maker with a design engine that produces
**3,840 distinct design variants per category** across 10 categories
(38,400 total designs).

## Features
- Asks how many logos the organiser has (0-4), then shows that many upload slots
- Logo arrangements: side by side, or main logo on top with the rest smaller below
- 10 categories: Cyber Security, Technology, Science, Academic, Sports,
  Arts & Culture, Corporate, Workshop, Hackathon, Training
- Design engine: 8 colour palettes x 6 frames x 4 layouts x 5 fonts x 4 textures,
  with a live design count, a variant gallery and a "Surprise Me" randomiser
  that never repeats the current design
- Signature photo upload, placed above the signatory line
- Position / rank: Participation, 1st, 2nd or 3rd Position presets, or a fully
  custom label (e.g. "Winner", "Best Performer"), shown as a ribbon under the
  recipient's name
- Background logo / watermark upload, centred behind the certificate content,
  with opacity and size sliders
- Optional custom message, printed as an elegant italic line on the certificate
- Up to 3 signatories, each with their own signature photo, name and title,
  laid out evenly in a row (a single signatory keeps the classic layout)
- Recipient, event, date, editable certificate text, signatory name and title
- Live preview; download as PNG or PDF (A4 landscape)
- Fully client-side: uploads never leave the user's device; no server, no database

## Bulk Certificates
For large events, the Bulk Certificates section generates one certificate per
recipient using the same category, design, logos, watermark and signatures:
- Import recipients from an Excel/CSV file (SheetJS; Name and Email columns
  auto-detected, plus optional Position and Message columns that apply to that
  recipient only), from a photo of a printed/handwritten list (Tesseract.js OCR),
  or by pasting a list (one per line, optional "Name, email" or
  "Name, email, position")
- Editable review table (name, email, position and message per row,
  add/remove rows, recipient count) — a row's own Position or Message overrides
  the shared one for that person only
- Generates every certificate and downloads them as a single ZIP (JSZip),
  one PNG per recipient, with live progress
- Optional email sending via the organiser's own free EmailJS account
  (Public Key / Service ID / Template ID stored only in the browser's
  localStorage; the template needs an attachment variable named
  `certificate_image` and uses `to_email` for the recipient). Without EmailJS,
  per-person mailto "Compose" buttons are offered instead

## Run locally
Open `index.html` in a browser, or serve the folder with any static server.

## Live
Deployed on Vercel (see repository About / deployment for the production URL).
