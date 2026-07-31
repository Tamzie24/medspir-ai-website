# MedSpir AI — Website

Static, framework-free site (HTML/CSS/JS) for MedSpir AI. No build step required.

## Pages
- `index.html` — Home
- `about.html` — About / founder / advisors
- `product.html` — Product (ADR module + MDR-TB module)
- `contact.html` — Contact

## Local preview
Just open `index.html` in a browser, or serve it locally:
```bash
python3 -m http.server 8000
```
Then visit http://localhost:8000

## Deploy with GitHub Pages

1. **Create the repo** (on github.com):
   - Click **New repository**
   - Name it `medspir-ai-website` (or your preferred repo name)
   - Keep it **Public** (required for free GitHub Pages) and don't initialize with a README (this folder already has one)

2. **Push this folder to it**, from inside this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial MedSpir AI website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/medspir-ai-website.git
   git push -u origin main
   ```

3. **Turn on Pages**:
   - In the repo, go to **Settings → Pages**
   - Under "Build and deployment," set **Source** to `Deploy from a branch`
   - Branch: `main`, folder: `/ (root)` → **Save**
   - GitHub will give you a live URL like:
     `https://<your-username>.github.io/medspir-ai-website/`

4. **(Optional) Custom domain**: if you buy `medspir.ai` or similar, add it under
   Settings → Pages → Custom domain, and create the DNS records GitHub shows you
   (a `CNAME` record pointing to `<your-username>.github.io`).

## Notes
- Contact form on `contact.html` currently submits via `mailto:` (no backend). Swap in a form
  service (Formspree, Getform, etc.) if you want direct submissions instead of opening the
  visitor's email client.
- Favicon source is `favicon.svg`; PNG fallbacks (`favicon-32.png`, `favicon-180.png`) are
  pre-generated from it.
