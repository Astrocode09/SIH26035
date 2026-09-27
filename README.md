# VeriScale — SIH26035

A pitch site and working prototype for Smart India Hackathon 2026 problem statement
**SIH26035**: *Development of a Software Program/Application for Generation of Test
Reports for Non-Automatic Weighing Instruments (NAWI) as per OIML Recommendation R-76*,
raised by the Ministry of Consumer Affairs, Food & Public Distribution.

## What's in this repo

- `index.html` — the entire site: single self-contained HTML file (no build step,
  no dependencies to install). Open it directly in a browser, or serve it with
  GitHub Pages.

## Running it locally

No install needed — just open `index.html` in a browser. If you want a local
server instead of the `file://` URL (some browsers restrict things like
`Intl.NumberFormat` locale data over `file://`):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying with GitHub Pages

1. Push this repo to GitHub.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`.
4. Save. Your site will publish at `https://<your-username>.github.io/<repo-name>/`.

## What's real vs. illustrative

The **"Try it" / compliance-engine section** on the page is a genuinely working
calculator:
- It implements the actual OIML R-76-1 maximum-permissible-error table
  (±0.5e / ±1.0e / ±1.5e bands by accuracy class and number of verification
  scale intervals).
- Repeatability and eccentricity verdicts are computed from the numbers you
  type in, not hardcoded.

Two things are simplified for the demo, and the page says so in-line:
- It checks one test load rather than the full multi-load R-76-1 Annex A/B
  sequence.
- The "verification code" is a simple client-side fingerprint (FNV-1a) shown
  as a stand-in for a real hash + QR verification system — not cryptographically
  secure, just illustrative of the concept.

The time-savings comparison in the "impact" section is labeled as a working
estimate for the pitch, not a measurement from a deployed system.

## Editing before you present

Search for `[Your team name]` in `index.html` (footer) and replace it with
your actual team name before submitting or presenting.
