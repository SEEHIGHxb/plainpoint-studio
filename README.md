# Plain Point Studio

The studio site at [plainpoint.net](https://plainpoint.net/) — one page listing the apps,
with each app's data handling stated on its own label.

Static HTML and CSS. No build step, no framework, **no JavaScript at all**, and no
third-party requests: the typeface (Archivo, variable) is served from this domain. That is
deliberate — the page makes a privacy claim about the apps, so it holds itself to the same
standard.

## Layout

| Path | What it is |
|---|---|
| `index.html` | The whole site |
| `styles.css` | The whole design system |
| `fonts/` | Archivo variable subsets (latin, latin-ext), self-hosted |
| `privacy.html` | Per-app privacy policy |
| `shots/` | Specimen photographs of the live apps (WebP, self-hosted) |
| `og.png` | Social card, 1200×630 |
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

Each app is one `<article class="label">` in `index.html`. The coloured auxiliary strips are
not decoration — they carry the app's actual data handling, and their colour is semantic:

| Class | Meaning |
|---|---|
| `strip--good` | A privacy property that holds (on-device data, no account) |
| `strip--note` | Something the visitor should know before using it (needs a server, needs sign-in) |
| `strip--info` | Neutral fact (platform, languages, licence) |
| `strip--hold` | Status (not yet released) |

### Specimens

A label only gets a photograph in `shots/` if a reader can open the app themselves and its
interface has settled. Midori is unreleased and Table of Five is private; Life Balance Index
is live but still being designed, so a shot of it would date the moment it changes. All three
stay text-only. Every specimen is a real
capture of the running app at 1280×800, driven to a populated state with invented demo data
and never with anyone's real records, then written out at 1000×625 WebP. Do not replace one
with a mockup or a design comp; the sheet is an honest record or it is worthless.

### Strips

Never give an app a `strip--good` it has not earned. Runaway carries `strip--note` because it
genuinely stores runs on a server; that honesty is the point of the design.
