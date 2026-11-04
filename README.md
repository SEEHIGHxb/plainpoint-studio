# Plain Point Studio

The studio site and hiring portfolio at [plainpoint.net](https://plainpoint.net/): who
Plain Point Studio is, two case studies (NgernNgok and Asterism), services, smaller work and
a contact route, with each app's data handling stated on its own label. It is the link to
put on LinkedIn, Fiverr and the Google Play developer profile.

Static HTML and CSS. No build step, no framework, **no JavaScript at all**, and no
third-party requests: the typeface (Archivo, variable) is served from this domain. That is
deliberate — the page makes a privacy claim about the apps, so it holds itself to the same
standard.

## Layout

| Path | What it is |
|---|---|
| `index.html` | The portfolio: hero, two case studies, services, more work, contact |
| `styles.css` | The whole design system |
| `fonts/` | Archivo variable, Latin subset, self-hosted |
| `privacy.html` | Per-app privacy policy |
| `shots/` | Real captures of NgernNgok and Asterism (WebP, self-hosted) |
| `og.png` | Social card, 1200×630, rendered from `styles.css` (master label) |
| `brand/` | Studio mark, LinkedIn/Fiverr avatar and LinkedIn cover |
| `favicon.svg`, `apple-touch-icon.png` | Tab icon (drawn to read at 16px) and the 180px iOS home-screen icon |
| `404.html` | Not-found page, same design |
| `.htmlvalidate.json` | Validator config; `.htmlvalidate.md` says why two rules are off |
| `CNAME` | Binds the GitHub Pages deploy to `plainpoint.net` |
| `PRODUCT.md` | Durable product record (audiences, constraints, brand commitments) |
| `DESIGN.md` | The visual system, recorded from the built page |

## Running it locally

Any static server works, since there is nothing to compile:

```bash
npx --yes serve -l 4321 .
```

## Deploying

Pushing to the default branch publishes it, once GitHub Pages is enabled for the repo with
the source set to that branch's root. `CNAME` handles the custom domain; the apex record for
`plainpoint.net` is managed in Cloudflare.

## Editing the labels

Each app is one `<article class="label">` in `index.html`: a `case` for the two flagship
apps, a compact label under More work for the rest. Before changing a label, read the app's
own repository: when an app gains a server, an account or an SDK, its strips and
`privacy.html` must change in the same commit. The coloured auxiliary strips are
not decoration — they carry the app's actual data handling, and their colour is semantic:

| Class | Meaning |
|---|---|
| `strip--good` | A privacy property that holds (on-device data, no account) |
| `strip--note` | Something the visitor should know before using it (needs a server, needs sign-in) |
| `strip--info` | Neutral fact (platform, languages, licence) |
| `strip--hold` | Status (not yet released) |

### Product images

Every image of an app is a real capture of the running app with invented demo data, never
a mockup. NgernNgok's come from its own `store-listing/en` screens; Asterism's are captured
from its code with Playwright after a demo onboarding. DESIGN.md › Product imagery has the
exact method, including the wellbeing banner that must be dismissed before capture.

### Brand assets

`brand/` holds the studio mark (`mark.svg`, `mark-512.png`), an 800px avatar for LinkedIn and
Fiverr profile pictures, and a 1584×396 LinkedIn cover. The favicon, `apple-touch-icon.png`
and `og.png` use the same mark.

### Strips

Never give an app a `strip--good` it has not earned. Runaway carries `strip--note` because it
genuinely stores runs on a server; that honesty is the point of the design.
