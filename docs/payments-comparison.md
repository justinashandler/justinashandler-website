# Payments: Stripe vs Venmo/Zelle vs Shopify

You're currently accepting payments for Creative Recess via Venmo, PayPal, and Zelle. Here's why Stripe is worth the small fee, and why Shopify is overkill.

---

## What You're Doing Now (Venmo / PayPal / Zelle)

The current flow:
1. Someone reads about Creative Recess on your site
2. They click "Join now"
3. They leave your site and open Venmo/PayPal/Zelle
4. They manually send you $200
5. You manually check that payment came through
6. You manually friend them on Facebook and add them to the group

### Problems with this approach
- **Friction kills sales** — every extra step loses people. Leaving your site to open another app is a big drop-off point
- **No automatic confirmation** — you have to manually match payments to people
- **No receipts** — your students don't get a professional receipt for their records (some may expense this)
- **No enrollment cap** — you can't auto-close registration when 30 spots fill
- **No refund management** — disputes are handled informally
- **Tax headaches** — no centralized reporting, you're tracking payments across three platforms
- **PayPal isn't free either** — PayPal business transactions cost 2.89% + 49¢ (more than Stripe)
- **Zelle has zero buyer protection** — no dispute resolution, which makes some buyers hesitant
- **Looks informal** — "Venmo me" doesn't match the quality of your program

---

## Stripe: What Changes

With Stripe, the flow becomes:
1. Someone reads about Creative Recess on your site
2. They click "Enroll Now"
3. A checkout form appears right on your page (or a Stripe-hosted checkout page)
4. They pay with credit card, Apple Pay, or Google Pay — never leaves your site
5. They instantly get a confirmation email with a receipt
6. You get notified, the spot count updates, and registration auto-closes at 30

### What Stripe gives you
- **One-click checkout** — Apple Pay and Google Pay mean some people pay in literally one tap
- **Automatic confirmation emails** — Stripe sends receipts, you can customize them
- **Enrollment cap** — your site can auto-close registration when all spots are sold
- **Discount codes** — early-bird pricing, referral codes, etc.
- **Dashboard** — see all payments, refunds, and revenue in one place
- **Tax reporting** — Stripe generates your 1099 at year-end
- **Refunds** — one-click refund from the dashboard
- **Professional** — builds trust, looks like a real business (because it is)
- **No monthly fee** — you only pay when someone actually pays you

### What it costs

**Per transaction: 2.9% + 30¢**

For Creative Recess at $200/seat, 30 seats:

| | Per sale | Full cohort (30 seats) |
|---|---|---|
| Revenue | $200.00 | $6,000.00 |
| Stripe fee | $6.10 | $183.00 |
| You keep | $193.90 | $5,817.00 |

**$183 out of $6,000 = 3.05% effective rate.** That's the cost of a professional checkout experience, automatic receipts, tax reporting, and not having to manually track 30 Venmo payments.

If you run Creative Recess twice a year, that's $366/yr in Stripe fees — roughly the same as what you're saving by leaving Squarespace.

---

## Why Not Shopify?

Shopify is an e-commerce platform for online stores. It's great if you're selling dozens of physical products with inventory, shipping, and variants. You're not.

### What Shopify costs
| Plan | Monthly | Annual | Transaction fee |
|------|---------|--------|-----------------|
| Starter | $5/mo | $60/yr | 5% per transaction |
| Basic | $39/mo | $468/yr | 2.9% + 30¢ |
| Shopify | $105/mo | $1,260/yr | 2.7% + 30¢ |

- **Starter plan** ($5/mo) charges 5% per transaction — that's $10 per $200 sale ($300 on a full cohort) plus the $60/yr subscription = $360/yr
- **Basic plan** ($39/mo) has the same transaction rate as Stripe (2.9% + 30¢) but adds $468/yr in subscription fees on top

### The comparison

| | Stripe | Shopify Starter | Shopify Basic |
|---|---|---|---|
| Monthly fee | $0 | $5 | $39 |
| Annual fee | $0 | $60 | $468 |
| Per-sale fee on $200 | $6.10 | $10.00 | $6.10 |
| Full cohort (30 seats) fees | $183 | $360 | $651 |
| Annual cost (2 cohorts) | **$366** | **$720** | **$1,134** |

### Why Shopify doesn't fit
- **You're not a store** — you're selling one program at a time, not managing a product catalog
- **Monthly fees for no reason** — Shopify charges monthly whether you're selling or not
- **Overkill features** — inventory management, shipping calculators, product variants — none of which apply
- **Less control** — you'd be locked into Shopify's templates and ecosystem
- **You already have a site** — adding Stripe to your existing site is simpler than rebuilding in Shopify

---

## Checkout Friction: The Hidden Cost of "Free" Payments

The Stripe fee on a full Creative Recess cohort is $183. That feels like real money. But the friction of sending people off-site to Venmo/Zelle almost certainly costs more than that in lost sales you never see.

### The data on checkout abandonment

- **70% of online purchases are abandoned before payment** — this is the industry average across all e-commerce ([Baymard Institute](https://baymard.com/lists/cart-abandonment-rate))
- **22% of shoppers abandon specifically because the checkout process is too long or complicated** ([Contentsquare](https://contentsquare.com/guides/cart-abandonment/stats/))
- **86% abandonment rate on mobile** — your audience is likely mostly on phones ([Drip](https://www.drip.com/blog/cart-abandonment-statistics))
- **Redirecting to an external payment service hurts conversion** — checkout research consistently flags off-site redirects as a major friction point ([Baymard Institute](https://baymard.com/lists/cart-abandonment-rate))

Your current flow is the worst case for friction: someone has to leave your site, open a different app, remember the amount, type it in, and send it to the right person. Every one of those steps is a place where someone thinks "I'll do this later" and never comes back.

### What on-site checkout does to conversion

- **Stripe found a 2x conversion rate increase** when Apple Pay was shown early in checkout vs. at the end ([Stripe Blog](https://stripe.com/blog/testing-the-conversion-impact-of-50-plus-global-payment-methods))
- **Business Insider reduced their payment flow from 10 steps to 2** using digital wallets and saw a **15% lift in conversions** ([INMA](https://www.inma.org/blogs/ideas/post.cfm/business-insider-improves-conversions-with-mobile-one-click-paywall))
- **SpotHero saw a 20% increase in conversions** when Google Pay was the default payment option ([Xola](https://www.xola.com/articles/how-apple-pay-and-google-pay-can-lift-mobile-conversion-rates/))
- **Apple Pay integration shows up to 58% higher conversion rates** vs. traditional credit card forms ([SalesCycle via SportsFusion](https://www.sportsfusion.co.uk/how-google-pay-and-apple-pay-drive-higher-conversion-rates-key-insights-and-data/))
- **Adding relevant payment methods beyond cards increased revenue by 12%** on average ([Stripe Blog](https://stripe.com/blog/testing-the-conversion-impact-of-50-plus-global-payment-methods))

### What this means for Creative Recess

Let's say 50 people visit the Creative Recess page and are interested enough to consider enrolling. With your current Venmo/Zelle flow:

| Scenario | Conversion rate | Enrollments | Revenue |
|----------|----------------|-------------|---------|
| Current (leave site, open Venmo) | 60% | 30 | $6,000 |
| With Stripe Checkout + Apple Pay | 75-80% | 38-40 | $7,600-$8,000 |

That's conservative — the research suggests the lift from removing off-site redirects and adding one-tap payment could be even higher. But even a modest improvement:

- **5 additional sales × $200 = $1,000 in extra revenue**
- **Stripe fees on the full 35 sales = $213.50**
- **Net gain: ~$786**

The $183 in Stripe fees isn't a cost — it's an investment that likely pays for itself multiple times over. You just never see the people who wanted to enroll but bounced because they had to open Venmo.

### The invisible loss

The cruelest part of checkout friction is that you never know it's happening. You don't get a notification that says "Sarah from Portland was about to enroll but gave up when she had to open Zelle." Those people just silently disappear. The only way to know is to remove the friction and see what happens to your numbers.

---

## Bottom Line

| Option | Best for | Annual cost (2 cohorts/yr) |
|--------|----------|---------------------------|
| **Venmo/Zelle** | Casual, small-scale, friends & family | ~$0 (but PayPal charges ~$350) |
| **Stripe** | Professional checkout, automatic everything | ~$366 |
| **Shopify Starter** | Small stores selling physical products | ~$720 |
| **Shopify Basic** | Serious e-commerce with inventory | ~$1,134 |

**Stripe is the right choice.** No monthly fee, professional checkout, automatic receipts and enrollment management, and the per-transaction cost is lower than every Shopify plan. You're trading $6.10 per sale for hours of manual payment tracking and a significantly better experience for your students.

The real question isn't "is 2.9% worth it?" — it's "how many sales am I losing because someone had to leave my site, open Venmo, and type in an amount manually?" Even one lost $200 sale per cohort more than covers the Stripe fees for the entire cohort.
