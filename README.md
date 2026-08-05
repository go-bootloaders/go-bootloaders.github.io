<p align="center"><img src="static/img/logo.svg" alt="go-bootloaders" width="120"></p>

# go-bootloaders.github.io

Sources for **go-bootloaders.github.io** — the go-bootloaders landing page.
Built with [Hugo](https://gohugo.io), same single inline-CSS template shape as the
sibling family landings (go-compressions, go-onigmo, …).

go-bootloaders has shipped two real, tested targets — `grub` and `systemd-boot`,
both in production use (consumed by `go-diskimages/diskimage`) — with four more
still on the roadmap. The page is an honest accounting of which is which:
"shipped" cards link to real code, "planned" cards are direction, not
capability.

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
