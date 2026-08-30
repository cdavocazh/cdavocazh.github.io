# cdavocazh.github.io

Portfolio site for Kris Zhang, built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/)
and deployed to GitHub Pages on every push to `main`.

Live: <https://cdavocazh.github.io/>

> **Optional custom domain (currently disabled):** to serve at `kris.awehawk.cloud`,
> (1) add a CNAME record `kris` → `cdavocazh.github.io` in Hostinger DNS,
> (2) restore `docs/CNAME` containing `kris.awehawk.cloud`,
> (3) set the custom domain in repo Settings → Pages and enable "Enforce HTTPS",
> (4) change `site_url` in `mkdocs.yml` back to the custom domain.
> The `cdavocazh.github.io` URL keeps working (301s to the custom domain), so
> resume links never break.

## Local development

```bash
# one-time
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

# preview with live reload at http://127.0.0.1:8000
mkdocs serve

# production build (matches CI; catches broken links)
mkdocs build --strict
```

## Structure

```
docs/
├── index.md                # Landing page — 3 project cards
├── about.md                # Background + contact
├── projects/
│   ├── market-tracker.md
│   ├── macro-trader.md
│   └── financial-agent.md
└── assets/
    ├── diagrams/           # Architecture images
    └── screenshots/        # Sample outputs
```

## Deploy

Push to `main` — the GitHub Action at `.github/workflows/deploy.yml` builds
and deploys automatically. First-time setup after pushing the repo:

1. GitHub → repo → Settings → Pages → **Source: GitHub Actions**
2. Push to `main`
3. Wait ~60s; site is live at `https://cdavocazh.github.io/` (or `https://kris.awehawk.cloud/` once DNS propagates)

## Adding a new project writeup

1. Create `docs/projects/<slug>.md` using one of the existing writeups as a template.
2. Add it to the `nav:` section in `mkdocs.yml`.
3. Add a card to `docs/index.md`.
4. Drop any diagrams into `docs/assets/diagrams/` and screenshots into `docs/assets/screenshots/`.

## Conventions

- **Mermaid for diagrams.** GitHub Pages renders them client-side via the
  `pymdownx.superfences` extension configured in `mkdocs.yml`.
- **No inline screenshots wider than 1200px.** Resize before committing.
- **Every writeup has five sections:** Problem · Architecture · Design choices
  & tradeoffs · Sample output · Stack.
