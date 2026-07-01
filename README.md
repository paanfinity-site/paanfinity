# Paanfinity Website (Static, Free Hosting)

A standalone replica of the Paanfinity Shopify store, built as a plain HTML/CSS/JS
site. No Shopify, no monthly fee — host it for free on GitHub Pages.

## Files
- `index.html` — homepage
- `shop.html` — full product grid (all 6 Sweet Paan Bite variants)
- `our-story.html`, `shipping.html`, `returns.html`, `contact.html`
- `style.css` — all styling (one shared file)
- `script.js` — mobile nav toggle

## Before you publish — 2 things left to fix

1. ~~Re-host the product images~~ ✅ Done — all images now live in `assets/`
   and are referenced locally. Nothing pulls from Shopify anymore.

2. **Add your real payment links.**
   Every "Buy Now" button currently points to a placeholder:
   `https://www.paypal.com/paypalme/yourbusiness/14.99`
   Replace these with either:
   - A [PayPal.me](https://paypal.me) link for your business, or
   - A [Stripe Payment Link](https://dashboard.stripe.com/payment-links) per product (recommended — Stripe Payment Links can show your product image, collect shipping address, and calculate tax automatically).
   Search `paypalme/yourbusiness` across all files to find every spot.

3. **Connect the forms.**
   The newsletter signup (homepage) and contact form (`contact.html`) post to
   a placeholder Formspree endpoint (`YOUR_FORM_ID`). GitHub Pages can't run
   server code, so forms need an external service:
   - Sign up free at [formspree.io](https://formspree.io)
   - Create a form, copy your endpoint URL
   - Paste it into the `action="..."` attribute on both forms

## Note on the t-shirt product
Your current Shopify collection includes a "Champion CC8C Adult Long-Sleeve
T-Shirt" mixed in with the paan bites — it looks like a leftover sample
product rather than something you sell. It was left out of this site. Let me
know if it should be added back as a real product.

## Deploying to GitHub Pages (free)

1. Create a new GitHub repository (e.g. `paanfinity-site`).
2. Upload all the files in this folder to the repo (drag-and-drop on
   github.com works, or use `git push`).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set Source to **Deploy from a branch**,
   branch `main`, folder `/ (root)`. Save.
5. Wait ~1 minute, then your site will be live at:
   `https://YOUR-USERNAME.github.io/paanfinity-site/`
6. (Optional) To use your own domain (paanfinity.com), add a `CNAME` file
   with your domain name, and update your domain's DNS to point at GitHub
   Pages — GitHub's docs walk through this under "Custom domains".

That's it — no server, no monthly hosting cost.
