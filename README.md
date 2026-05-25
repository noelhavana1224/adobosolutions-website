# Adobo Solutions Website

Multi-page static website for adobosolutions.com — hosted on GitHub Pages.

## Pages
- `index.html` — Homepage
- `services.html` — All VA services
- `adoboost.html` — AdoBoost product page
- `pricing.html` — VA + AdoBoost pricing
- `about.html` — About Adobo Solutions
- `contact.html` — Hire a VA / Contact form

## Deploy to GitHub Pages

1. Create a new GitHub repo named `adobosolutions-website` (or any name)
2. Push all files to the `main` branch
3. Go to **Settings → Pages → Source** → select `main` branch, `/ (root)`
4. Under **Settings → Pages → Custom domain**, enter `adobosolutions.com`
5. At your domain registrar (GoDaddy / Namecheap / Cloudflare), add these DNS records:

```
Type   Name   Value
A      @      185.199.108.153
A      @      185.199.109.153
A      @      185.199.110.153
A      @      185.199.111.153
CNAME  www    your-github-username.github.io
```

6. Wait 10–30 minutes for DNS to propagate — then your site is live at adobosolutions.com

## To connect the contact form
Replace the `handleSubmit` function in `contact.html` with a POST to:
- **Formspree**: `https://formspree.io/f/YOUR_ID` (free, no backend needed)
- **Netlify Forms**: add `netlify` attribute to the `<form>` tag if deploying to Netlify

## File structure
```
adobosolutions-website/
├── index.html
├── services.html
├── adoboost.html
├── pricing.html
├── about.html
├── contact.html
├── CNAME
├── css/
│   └── main.css
└── assets/
    └── logo.jpg
```
