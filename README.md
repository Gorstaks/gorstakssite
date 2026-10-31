# gorstak-site

> **Gorstak download page.** Static HTML page with a profile sidebar and download links.
>
> Live at **https://gorstak.eu** (GitHub Pages, custom domain).

---

## Overview

gorstak-site is a single static page. The left column holds the profile and social links. The main column links to the download folders on MediaFire and Pixeldrain. It is hosted on GitHub Pages under the `gorstaks` account at the custom domain `gorstak.eu`.

---

## Project Structure

| File | Description |
|------|-------------|
| `index.html` | The page (self-contained HTML, CSS, and JavaScript) |
| `assets/` | Logo and other images |
| `CNAME` | Custom domain (`gorstak.eu`) |
| `build.js` | Copies the site to a sibling `releases/gorstak-site` folder |
| `package.json` | Local dev server scripts (`http-server`) |
| `.github/workflows/` | GitHub Pages deploy workflow |

---

## Deployment

### GitHub Pages

1. Push to the `main` branch of `gorstaks/gorstakssite`.
2. Settings -> Pages -> Source: "Deploy from a branch" (or the included Actions workflow).
3. The `Deploy GitHub Pages` workflow publishes the site on every push to `main`.

### Custom Domain (gorstak.eu)

1. `CNAME` contains `gorstak.eu`.
2. DNS at the registrar (OVH):
   - Apex `@` A records -> GitHub Pages IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `www` CNAME -> `gorstaks.github.io.`
3. Enable "Enforce HTTPS" in Settings -> Pages once the certificate provisions.

### Local Testing

```bash
# Using Python
python -m http.server 8000
# Using Node.js
npx serve .
# Access
http://localhost:8000
```

---

## Customization

Edit the CSS variables at the top of the `<style>` block in `index.html` to change the colors. The download buttons are the `.download-btn` links in the main column.

---

## License & Disclaimer

---

## Comprehensive legal disclaimer

This project is intended for authorized defensive, administrative, research, or educational use only.

- Use only on systems, networks, and environments where you have explicit permission.
- Misuse may violate law, contracts, policy, or acceptable-use terms.
- Running security, hardening, monitoring, or response tooling can impact stability and may disrupt legitimate software.
- Validate all changes in a test environment before production use.
- This project is provided "AS IS", without warranties of any kind, including merchantability, fitness for a particular purpose, and non-infringement.
- Authors and contributors are not liable for direct or indirect damages, data loss, downtime, business interruption, legal exposure, or compliance impact.
- You are solely responsible for lawful operation, configuration choices, and compliance obligations in your jurisdiction.

---

<p align="center">
  <sub>Built with care by <strong>Gorstak</strong></sub>
</p>
