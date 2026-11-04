# Modern Woman website

A responsive, buildless concert website for Modern Woman: The All-Female Billy Joel Tribute Experience.

## Run locally

From this directory:

```sh
python3 -m http.server 8080 --directory dist
```

Open http://localhost:8080. No package installation or build is required. The site is also deployable to any static host using `dist/`.

## Edit the content

- `dist/content.js`: all five musicians, booking email, social links, and concert dates. The date and link examples are comments only, never displayed as real shows.
- `dist/index.html`: promotional copy, navigation, YouTube embed, and photo placeholders.
- `dist/style.css`: responsive design, preliminary wordmark, original piano illustration, and print EPK styles.
- `dist/app.js`: mobile menu, concert rendering, contact links, and band overview download.

Set `bookingEmail` to the official address to enable a real booking email link. Add official social profiles to `socialLinks` to replace the social-link placeholder. No inquiry form is present because no delivery service or contact address was supplied.

Add confirmed shows with `date` (YYYY-MM-DD), `venue`, `city`, and an HTTPS `tickets` URL. The empty state disappears automatically when shows exist. Ticket and social URLs are restricted to HTTPS.

Replace the clearly labeled gallery placeholders with actual band photographs, with descriptive alt text. No stock or generated people are used. The hero is original CSS piano artwork. The preliminary typographic logo includes the full subtitle.

The supplied YouTube Short is embedded with a privacy-enhanced player and a permanent fallback link. YouTube may restrict playback depending on browser, consent settings, network, or video owner settings. More vertical videos can be added using the existing `.video-shell` pattern.

The band overview download is a working plain-text file. Print EPK uses the browser's print dialog and print-specific styles; visitors can save it as PDF. No complete production technical rider or official promotional photos were supplied.

Typography uses Google Fonts with system fallbacks. All other design assets are local.

## Checks

`node --check dist/app.js` and `node --check dist/content.js` check JavaScript syntax. HTML structure, local references, section anchors, and supplied musician details were checked separately. Browser layout and third-party video playback were not verified in the current environment.

## Hosting

`.openai/hosting.json` retains the newly registered private Sites project identity. The Sites packaging helper was unavailable in this environment, so this checkout has not been published to Sites.
