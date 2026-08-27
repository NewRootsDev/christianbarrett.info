# christianbarrett.info

Single page personal site. Plain HTML, no build step, no dependencies except two Google fonts.

Files:

- `index.html` The whole site
- `og-image.png` Share image for links pasted into social and chat apps
- `sitemap.xml` and `robots.txt` For search engines
- `CNAME` Custom domain for GitHub Pages (skip uploading this, GitHub creates it when you set the custom domain)

## Deploy

1. New public repo, name it `christianbarrett.info` (public is required for free Pages).
2. Upload `index.html` and `CNAME` to the root of `main`.
3. Settings, Pages, Source: Deploy from a branch, `main`, `/ (root)`.
4. Settings, Pages, Custom domain: `christianbarrett.info`, Save.
5. After DNS resolves, check Enforce HTTPS.

## DNS at your registrar

Apex `@`, four A records:

    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153

Apex `@`, four AAAA records:

    2606:50c0:8000::153
    2606:50c0:8001::153
    2606:50c0:8002::153
    2606:50c0:8003::153

`www`, one CNAME record pointing to `<your-github-username>.github.io.`

Delete any parked or forwarding A records the registrar added by default. Certificate issuance usually takes a few minutes and can take up to 24 hours.

## Editing

Everything is in `index.html`. Copy lives in `<main class="drawing">`, the right rail lives in `<aside class="titleblock">`, colors and type are the CSS variables at the top of the `<style>` block.

Contact email is `christian@newrootsdevelopment.co`, set in the Contact section and in the JSON-LD block in the head.
