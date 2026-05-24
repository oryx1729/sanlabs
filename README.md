# Sanlabs Website

Static website for [sanlabs.ai](https://sanlabs.ai/), published through GitHub Pages from [oryx1729/sanlabs](https://github.com/oryx1729/sanlabs).

## Structure

- `index.html` - landing page
- `impressum/` - German legal imprint
- `datenschutz/` - German privacy policy
- `assets/` - shared CSS, JavaScript, favicon, and locally hosted fonts
- `CNAME` - GitHub Pages custom domain declaration for `sanlabs.ai`
- `.nojekyll` - disables Jekyll processing on GitHub Pages

## Local Preview

From the repo root:

```sh
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## GitHub Pages

The repository is configured to publish from branch `main` and folder `/ (root)`.

If the Pages settings are changed later, restore them in **Settings -> Pages**:

1. Under **Build and deployment**, choose **Deploy from a branch**.
2. Select branch `main` and folder `/ (root)`, then save.
3. Under **Custom domain**, use `sanlabs.ai` and enable **Enforce HTTPS** once DNS has propagated and GitHub allows it.

## Namecheap DNS

For the apex domain `sanlabs.ai`, add these GitHub Pages records in Namecheap's **Advanced DNS** screen:

| Type | Host | Value |
| --- | --- | --- |
| A Record | `@` | `185.199.108.153` |
| A Record | `@` | `185.199.109.153` |
| A Record | `@` | `185.199.110.153` |
| A Record | `@` | `185.199.111.153` |
| CNAME Record | `www` | `oryx1729.github.io` |

Optional IPv6 records:

| Type | Host | Value |
| --- | --- | --- |
| AAAA Record | `@` | `2606:50c0:8000::153` |
| AAAA Record | `@` | `2606:50c0:8001::153` |
| AAAA Record | `@` | `2606:50c0:8002::153` |
| AAAA Record | `@` | `2606:50c0:8003::153` |

DNS changes can take up to 24 hours to propagate.
