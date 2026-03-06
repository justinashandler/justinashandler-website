# Justina's Migration Checklist

Tasks for Justina to complete. Each phase has a verification step — don't move to the next phase until the current one checks out.

---

## Phase 1: Accounts & Security Setup

### Prerequisites
- [ ] Install an authenticator app on your phone if you don't have one already
  - Recommended: [1Password](https://1password.com) (paid, best overall), [Google Authenticator](https://apps.apple.com/app/google-authenticator/id388497605) (free), or [Authy](https://apps.apple.com/app/twilio-authy/id494168017) (free)
  - You'll use this for 2FA on all the accounts below
- [ ] Have a password manager ready (1Password, iCloud Keychain, etc.) — you'll be creating several accounts

### Account 1: GitHub (code hosting)
Your site's code will live here in a private repository you own.
- [x] Go to [github.com/signup](https://github.com/signup)
- [x] Sign up with your email
- [x] Choose the Free plan (that's all you need)
- [ ] Set up 2FA immediately:
  - Settings → Password and Authentication → Two-factor authentication → Enable
  - Choose "Authenticator app"
  - Scan the QR code with your authenticator app
  - Save your recovery codes somewhere safe (password manager or printed)
- [x] Create a new private repository for your site (`justinashandler-website`)

### Account 2: Cloudflare (hosting + domain)
Your site will be hosted here, and your domain will be managed here.
- [x] Go to [dash.cloudflare.com/sign-up](https://dash.cloudflare.com/sign-up)
- [x] Sign up with your email
- [x] The Free plan is all you need
- [ ] Set up 2FA immediately:
  - My Profile (top-right avatar) → Authentication → Two-Factor Authentication
  - Choose "Authenticator app" (they call it "Mobile app authentication")
  - Scan the QR code with your authenticator app
  - Save your recovery codes
- [x] Add your site to Cloudflare:
  - Dashboard → Add a Site → enter `justinashandler.com` → select the Free plan
  - Cloudflare will scan your DNS records — accept the defaults for now

### Account 3: Stripe (payments — if accepting card payments on the site)
This is how people will pay for Creative Recess and future offerings.
- [ ] Go to [dashboard.stripe.com/register](https://dashboard.stripe.com/register)
- [ ] Sign up with your email
- [ ] Complete business verification (Stripe will ask for name, address, bank account for payouts, SSN for tax reporting)
- [ ] Set up 2FA immediately:
  - Settings → Profile → Two-step authentication → Add
  - Choose "Authenticator app"
  - Scan the QR code with your authenticator app
  - Save your recovery codes
- [ ] Get your test API keys for later (Dashboard → Developers → API Keys → toggle "Test mode" first)
  - **Publishable key** (starts with `pk_test_`) — safe to use anywhere
  - **Secret key** (starts with `sk_test_`) — keep this private, you'll add it to your site's config later

> **Security tip**: Always work in "Test mode" first. Test keys can't process real charges. You'll switch to live keys only when the site is ready to launch.

---

## Phase 2: Download & Verify Your Site Locally

The goal here is to get an exact copy of your current Squarespace site running on your computer. Nothing changes publicly — your live site stays up the whole time.

### Step 1: Download your site
- [x] Downloaded a mirror of https://www.justinashandler.com into `site-archive` folder, including all pages and images
- [x] Set up local server to view it in browser

### Step 2: Verify it locally
- [x] Open the local URL (`http://localhost:8000`)
- [x] Check each page looks right:
  - [x] Home page — hero image, tagline, Instagram feed area
  - [x] Creative Recess — program description, pricing, join button
  - [x] About — bio, photo, accomplishments
  - [x] Contact — form displays correctly
- [x] Check that images load
- [x] Check that navigation works between pages

> **Note**: Some things won't work locally (Instagram embed, contact form submission, external links to Spotify/Bandcamp). That's expected — we're just verifying the content and layout transferred correctly.

### Step 3: Gather additional assets
- [ ] Collect any brand assets that aren't on the site: original logo files, specific fonts, color codes
- [ ] Gather any high-res press photos or images you want on the new site that aren't already on the current one

---

## Phase 3: Push to Cloudflare Pages & Verify on the Web

Now we put the same mirrored site on Cloudflare to confirm it works when hosted for real, before touching the domain.

### Step 1: Deploy to Cloudflare Pages
- [x] Pushed site-archive to GitHub (`justinashandler/justinashandler-website`)
- [x] Set up Cloudflare Pages deployment
- [x] Staging URL: `justinashandler-website.pages.dev`

### Step 2: Verify on the staging URL
- [x] Open the staging URL in your browser
- [x] Check each page again:
  - [x] Home page
  - [x] Creative Recess
  - [x] About
  - [x] Contact
- [x] Check that images load
- [x] Check that HTTPS works (padlock icon in browser)
- [ ] Test on your phone too

> **Your live Squarespace site is still running at justinashandler.com this whole time.** Nothing has changed publicly yet.

---

## Phase 4: Domain Migration to Cloudflare

Now that the site works on Cloudflare, it's safe to move the domain over.

### Step 1: Find out where your domain is registered
- [x] Domain is registered at **DreamHost** (not Squarespace — Squarespace was just the site builder)

### Step 2: Unlock your domain
- [x] Logged into DreamHost panel
- [x] Turned off domain transfer lock (domain shows as Unlocked)
- [ ] ~~Get EPP transfer code~~ — skipped: domain registered Oct 2025, ICANN 60-day lock prevents transfer. Used nameserver change instead.

### Step 3: Point nameservers to Cloudflare (instead of transferring)
- [x] Changed nameservers in DreamHost from DreamHost's to Cloudflare's:
  - `jill.ns.cloudflare.com`
  - `vern.ns.cloudflare.com`
- [x] Updated DNS records in Cloudflare (removed Squarespace A records, updated www CNAME to point to Pages)
- ⏳ Waiting for DNS propagation (1–2 hours, up to 24h)

### Step 4: Add custom domain to Cloudflare Pages
- [ ] Once DNS propagates, go to Pages → justinashandler-website → Custom Domains → Add `justinashandler.com`
- [ ] Then add `www.justinashandler.com` the same way

### Step 5: Verify everything works
- [ ] Visit https://www.justinashandler.com — it should now be served from Cloudflare
- [ ] Check each page loads correctly
- [ ] Check that HTTPS works
- [ ] Check that email still works by sending yourself a test email

> **Important**: Do NOT cancel Squarespace until this step is fully verified.

---

## Phase 5: Email Setup (if needed)

- [x] Using Gmail — email is independent of Squarespace/domain, no action needed ✓

---

## Phase 6: Site Improvements

Site has been fully rebuilt as a clean, self-hosted static site — zero Squarespace dependencies.
Live on staging: https://justinashandler-website.pages.dev

### Answer Discovery Questions
- [x] Reviewed and answered the questions in `discovery-questions.md`

### Done ✓
- [x] Rebuilt site as clean static HTML/CSS (no Squarespace dependencies)
- [x] Self-host all images (all images in `images/` folder, deployed to Cloudflare)
- [x] Embedded Spotify player (Justina Shandler artist embed on home page)
- [x] Better mobile experience (responsive CSS with media queries)

### Still To Do (needs your input)
- [ ] Replace Instagram embed with [Behold.so](https://behold.so) widget
  - Sign up at behold.so, connect Instagram @justinashandler
  - Paste embed code into `index.html` where the placeholder comment is
- [ ] Replace contact form with Formspree
  - Sign up at formspree.io, create a new form (connect to justinashandler@gmail.com)
  - Replace `YOUR_FORM_ID` in `contact.html` with your form ID (looks like `xpwzgkna`)
- [ ] Add real social links to footer (Instagram, TikTok, Spotify, Bandcamp URLs)

### Ideas for Later
- [ ] Stripe payments instead of Venmo/PayPal/Zelle for Creative Recess
- [ ] Mailing list / newsletter signup
- [ ] A press/EPK page
- [ ] New pages for your music projects (LADY SLOTH, Velvet Halo, JELAINA)

---

## Phase 7: Cleanup

- [ ] Cancel your Squarespace subscription (only after everything is confirmed working)
- [ ] Update any external links pointing to old Squarespace URLs (if any changed)
- [ ] Update Facebook Pixel or analytics tracking if needed
- [ ] Set up Cloudflare Web Analytics (free)

---

## Quick Reference: What Costs What

| Item | Old (Squarespace) | New |
|------|-------------------|-----|
| Hosting | $16-33/mo | Free (Cloudflare Pages) |
| Domain | ~$20/yr | ~$10/yr (Cloudflare, at-cost) |
| Payments | Venmo/Zelle (free but manual) | Stripe: 2.9% + 30¢ per transaction |
| Email | Depends on current setup | Keep current provider |
| SSL Certificate | Included | Free (Cloudflare) |
| **Annual total** | **$192-396+/yr** | **~$10/yr + Stripe fees on sales** |
