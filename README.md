# layland.xyz

Static one-page site for Layland Consulting, LLC. No build step, no
dependencies, no JavaScript.

```
index.html
css/style.css
assets/            # logo + favicon
CNAME              # custom domain for GitHub Pages
.nojekyll          # serve files as-is, skip Jekyll
```

## Local preview

```
python3 -m http.server 8000
```

## Deploy

Hosted on GitHub Pages from `main` / root. Pushing to `main` publishes.

```
git push origin main
```

## DNS

`layland.xyz` apex — four A records:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

Optional AAAA records for IPv6:

```
2606:50c0:8000::153
2606:50c0:8001::153
2606:50c0:8002::153
2606:50c0:8003::153
```

`www` — CNAME to `rockpunk.github.io` (no repository name).

After DNS resolves, enable *Enforce HTTPS* in the repo's Pages settings.

Note: `rockpunk/rockpunk.github.io` is a separate Jekyll blog with no custom
domain. This repo owns `layland.xyz` independently of it.

## Contact

No form and no JavaScript — the Get in touch section is a plain
`mailto:consulting@layland.xyz` link.
