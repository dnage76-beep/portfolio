# Portfolio

Personal site for Derek Nagel, mechanical engineering student at George Mason University.

Live at [dereknagel.com](https://dereknagel.com).

## Stack

A single hand-written `index.html` with no framework and no build step, deployed on Vercel. The page is static on purpose: it loads in one request, there is nothing to rebuild when a project changes, and the whole thing stays readable in one file.

## Structure

```
index.html              the entire site
fonts/                  self-hosted webfonts (no external font requests)
images/                 project imagery
og-image.svg            social preview card
Derek_Nagel_Resume.pdf  linked from the site
vercel.json             routing and headers
```

## Running it

No dependencies. Open `index.html` in a browser, or serve the directory:

```bash
python3 -m http.server 8000
```

Deploys automatically from `main` via Vercel.
