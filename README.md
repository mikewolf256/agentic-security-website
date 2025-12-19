# Agentic Security Partners - Marketing Website

Landing page for Agentic Security Partners, deployed on Netlify.

## Quick Start

This is a static HTML website. No build process required.

### Local Development

Simply open `index.html` in your browser, or use a local server:

```bash
# Python 3
python3 -m http.server 8000

# Node.js
npx serve .

# Then open http://localhost:8000
```

## Deployment

### Netlify (Recommended)

1. Push this repo to GitHub
2. Go to [netlify.com](https://netlify.com) and sign up/login
3. Click "Add new site" > "Import an existing project"
4. Connect to GitHub and select this repository
5. Netlify will auto-detect settings (publish directory: root)
6. Click "Deploy site"
7. Your site will be live at `https://random-name-123.netlify.app`

### Custom Domain

1. In Netlify: Site settings > Domain management
2. Add your custom domain (e.g., `agenticsec.team`)
3. Follow DNS instructions (add CNAME record)
4. Netlify provides free SSL automatically

## File Structure

```
.
├── index.html          # Main landing page
├── logo.png            # Logo file (add your logo here)
├── netlify.toml        # Netlify configuration
├── README.md           # This file
└── .gitignore          # Git ignore rules
```

## Notes

- The site uses client-side routing (SPA-style navigation)
- All CSS and JavaScript is inline in `index.html`
- Logo is referenced as `logo.png` - add your logo file to the root
- No external dependencies required

## Updating Content

Edit `index.html` directly. Changes will auto-deploy if connected to Netlify via GitHub.

## TODOs (GTM / Proof)

- Add HubSpot email-only embed to `demo.html` (replace `HUBSPOT_FORM_PLACEHOLDER`) and set HubSpot redirect to `/demo-thanks.html`.
- Add booking calendar URL to the disabled “Book a call” button in `demo-thanks.html`.

