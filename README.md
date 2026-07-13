# MINA FZC LLC — Static Website

A static Next.js website for MINA FZC LLC (dental, surgical & medical instruments).

**Pages:** Home · About Us · Contact · Privacy Policy · Terms & Conditions
**Fonts:** Montserrat (headings) · Poppins (body) — loaded via `next/font/google`
**Brand colors:** Primary Blue `#0B2D6B` · Royal Blue `#1E63F3` · White · Silver `#C0C0C0`

## Getting started

```bash
npm install
npm run dev        # development server at http://localhost:3000
npm run build      # static export into the /out folder
```

The site is configured with `output: 'export'`, so `npm run build` produces a
fully static site in `/out` that you can upload to any static host
(Vercel, Netlify, cPanel/shared hosting, S3, GitHub Pages, etc.).

## Customizing your details (one file)

All company info — **address, phone, WhatsApp, email, markets, tagline** — lives in:

```
lib/site.js
```

Edit the values there once and every page (header, footer, contact, legal pages)
updates automatically. Product names, codes, descriptions and features are in the
same file under `products`.

## Images

Product and brand images are in `public/images/`:

- `logo.jpg` — brand logo (navbar + footer)
- `hero-banner.jpg` — home/about hero image
- `composite-gold.jpg`, `composite-blue.jpg`, `pmt-set.jpg`,
  `chrome-removal.jpg`, `rubber-dam-clamp.jpg`, `impression-tray.jpg`,
  `tweezer.jpg` — product cards

Replace any file with a new image of the same name to swap it.

## Notes

- The contact form is static-host friendly: submitting it opens the visitor's
  email client with the message pre-filled (no backend required). If you later
  want real form submissions, wire it to a service like Formspree or Web3Forms.
- Colors and typography tokens are defined at the top of `app/globals.css`.
