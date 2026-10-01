# jamieguttermantherapy.com

Static site for Jamie Gutterman, LCSW. Plain HTML and one stylesheet (`css/style.css`); no build step.

## Editing

- Each page is a standalone `.html` file. The header and footer are repeated in every page, so a nav or footer change needs making in all six (`index`, `about`, `services`, `fees`, `contact`, `404`).
- The availability items ("Accepting new clients", "Telehealth across North Carolina") are in the hero of `index.html`.
- Search for `TODO` to find copy that still needs Jamie's confirmation.
- `home/` holds redirect stubs for the old WordPress URLs. Leave them in place.

## Preview locally

```bash
python3 -m http.server 8765
```

Then open http://localhost:8765.

## Hosting on GitHub Pages

1. Push this folder to a GitHub repository.
2. Repository Settings > Pages > Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. When ready to go live, set the custom domain to `jamieguttermantherapy.com` in the Pages settings (this adds a `CNAME` file). It is left unset for now so the `github.io` preview URL works.
4. At the domain registrar, point DNS at GitHub Pages:
   - `A` records for the apex domain: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www`: `<github-username>.github.io`
5. Once DNS has propagated, tick "Enforce HTTPS" in the Pages settings.
6. Check the live site, then cancel the WordPress hosting.
