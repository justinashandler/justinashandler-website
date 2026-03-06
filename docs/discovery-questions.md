# Justina Shandler: Squarespace → Cloudflare Migration — Discovery Questions

## Context
Helping Justina migrate [justinashandler.com](https://www.justinashandler.com) from Squarespace to a self-hosted static site on Cloudflare Pages, backed by a private GitHub repo, with Claude Code skills for ongoing design/functionality.

## Current Site Audit (what's there today)
- **4 pages**: Home, Creative Recess, About, Contact
- **Business**: Singer-songwriter, composer (Cocomelon/Blippi/Little Angel), music mentor
- **Creative Recess**: 5-week songwriting program, $200 "Play Pass", payments via Venmo/PayPal/Zelle (no Stripe), capped at 30 participants, uses Facebook group for delivery
- **Contact**: Simple name/email/message form with reCAPTCHA
- **Socials**: Instagram, TikTok, Spotify, Bandcamp
- **Instagram feed** embedded on homepage
- **Design**: Minimalist, image-forward, Squarespace v7.1
- **Not using**: E-commerce, blog, scheduling, member areas, email marketing through Squarespace
- **Analytics**: Facebook Pixel

---

## Discovery Questions for Justina

### 1. Why Are You Leaving Squarespace?
- What's frustrating you about Squarespace? (Cost, limitations, speed, something else?)
- What does your Squarespace plan cost today? (Likely $16-33/mo — the new site would be free hosting)
- Is there anything you love about Squarespace you'd want to keep?

### 2. Design & Vibe
- Are you happy with the current look, or do you want a visual refresh?
- Any websites you admire for design inspiration?
- Do you have your brand assets (logo, fonts, color palette) as files, or are they only in Squarespace?
- The Instagram feed embed on your homepage — do you want to keep that?

### 3. Creative Recess & Payments
- Is Creative Recess a recurring program (runs multiple times a year), or was it a one-time thing?
- Are you planning other paid programs/offerings?
- You currently accept Venmo/PayPal/Zelle — would you prefer a proper checkout experience on the site? (Stripe would let people pay by credit card directly on the page, with Apple Pay/Google Pay)
- Do you need to cap enrollment and auto-close registration?
- Do you want an email sent automatically when someone pays?
- Do you need discount codes or early-bird pricing?

### 4. Content & Pages
- Are these 4 pages (Home, Creative Recess, About, Contact) the full site, or are there hidden/draft pages?
- Do you want to add any new pages? (Music/discography, press/EPK, testimonials, a blog?)
- Do you want a dedicated page for your projects (LADY SLOTH, Velvet Halo, JELAINA)?
- Any content you want to drop or restructure?

### 5. Music & Media
- Do you want to embed Spotify players or Bandcamp players on the site?
- Any video content (YouTube, music videos) you'd want featured?
- Do you have high-res press photos that need hosting?

### 6. Email & Newsletter
- Do you collect email addresses from fans/students? If so, through what tool?
- Would you want a mailing list signup on the site?
- If yes — do you have a preference for email platform? (Mailchimp, ConvertKit, Buttondown, etc.)

### 7. Contact & Communication
- Is the simple contact form sufficient, or do you want something more? (Booking requests, inquiry categories, auto-replies?)
- Do you need a scheduling/calendar tool for mentoring sessions?

### 8. Domain & Email
- Where is justinashandler.com registered? (Squarespace, or elsewhere?)
- What email do you use for business? (Gmail, Squarespace Email, etc.)
- Are you open to transferring the domain to Cloudflare? (Saves money, at-cost pricing)

### 9. Analytics & SEO
- How important is Google search traffic to you?
- Do you want to keep Facebook Pixel tracking?
- Do you use Google Analytics or Search Console?

### 10. Ongoing Maintenance
- How comfortable are you editing text/content? (This determines whether we add a visual CMS layer or you ask a developer for changes)
- How often do you update the site? (Weekly? A few times a year?)
- Would you want to be able to update things like program dates, pricing, and page text yourself?

### 11. Wishlist
- What does your site NOT do today that you wish it did?
- If you could wave a magic wand and your site did one new thing, what would it be?

---

## Likely Stack (post-discovery)

| Layer | Tool | Cost |
|-------|------|------|
| Hosting | Cloudflare Pages | Free |
| Code | Private GitHub repo | Free |
| Framework | Astro (static, fast, simple) | Free |
| Payments | Stripe Checkout | 2.9% + 30¢ per txn |
| Forms | Cloudflare Workers or Formspree | Free tier |
| CMS (if needed) | Decap CMS (git-based, free) | Free |
| Analytics | Cloudflare Web Analytics | Free |
| Domain | Cloudflare Registrar | At-cost (~$10/yr) |
| Email | Keep existing provider | Varies |

**Squarespace cost eliminated**: ~$192-396/yr → ~$10/yr (domain only)

## Claude Code Skills to Build
- **Frontend design skill**: Component library, responsive layouts, design system
- **Stripe integration skill**: Checkout flows, payment confirmation, webhook handling
- **Content management skill**: Easy content updates via git-based CMS or markdown
- **Deployment skill**: GitHub → Cloudflare Pages CI/CD pipeline
