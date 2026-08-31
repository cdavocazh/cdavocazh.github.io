# cdavocazh.github.io

Built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/)

Live: <https://cdavocazh.github.io/>


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
