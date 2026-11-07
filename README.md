# ADREN Technologies website

A plain static site: just `index.html` plus the `assets` folder. The enquiry form uses Web3Forms, so there is no server code.

## 1. Connect the form (2 minutes)
1. Go to https://web3forms.com, enter **info@adrentechnologies.com** and get your free access key by email.
2. Open `index.html`, your key is already set in the script near the bottom (`ACCESS_KEY`). Change it only if you generate a new one.
3. Save. The key is meant to be public, so it is safe in the page.

## 2. Deploy on Vercel
Push this folder to GitHub (or drag it into Vercel / run `npx vercel`). No build step and no environment variables are needed.

## 3. Connect adrentechnologies.com (GoDaddy DNS)
In Vercel > Project > Settings > Domains add `adrentechnologies.com` and `www.adrentechnologies.com`, then in GoDaddy DNS:
- `A` record, name `@`, value `76.76.21.21`
- `CNAME` record, name `www`, value `cname.vercel-dns.com`

Do not delete your MX records (they carry info@ email).

## 4. Test
Submit the form on the live site and check that the mail reaches info@adrentechnologies.com. The visitor's address is in the email, so replying answers them.

## Notes
- Spam: the form has a hidden field and a 3-second minimum. Web3Forms also filters spam, and its dashboard lets you turn on hCaptcha or Cloudflare Turnstile if needed.
- Automatic thank-you emails to visitors need a paid Web3Forms plan. The success message on the page already tells visitors you will reply within one business day.
- Placeholders to review before going live: the footer shows CIN and GSTIN; add Terms and Privacy pages after legal review.
