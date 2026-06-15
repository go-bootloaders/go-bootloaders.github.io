<p align="center"><img src="static/img/logo.svg" alt="go-bootloaders" width="120"></p>

# go-bootloaders.github.io

Sources for **go-bootloaders.github.io** — the go-bootloaders landing page.
Built with [Hugo](https://gohugo.io), same single inline-CSS template shape as the
sibling family landings (go-compressions, go-onigmo, …).

go-bootloaders is **early-stage**: no library has shipped yet, so the page is an
honest roadmap of the boot stacks we mean to reimplement in pure Go — not a wall
of repo cards for code that does not exist.

## Layout

```text
.
├── hugo.toml              Site config + roadmap params
├── content/_index.md      Homepage marker (empty)
├── layouts/index.html     Homepage body (inline CSS, light/dark vars)
└── static/
    ├── img/logo.svg       88px hero logo
    └── favicon.svg        Favicon
```

## Build locally

```sh
hugo server -D            # live reload at http://localhost:1313/
hugo --gc --minify        # production build → ./public/
```

## Deploy

`.github/workflows/hugo.yml` builds + deploys on every push to `main`.
GitHub Pages **Source = "GitHub Actions"** (not "Deploy from a branch").
