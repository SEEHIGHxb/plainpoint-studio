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
| `404.html` | Not-found page, same design |
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

Never give an app a `strip--good` it has not earned. Runaway carries `strip--note` because it
genuinely stores runs on a server; that honesty is the point of the design.
