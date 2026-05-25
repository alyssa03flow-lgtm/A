---
name: ad-supported-personal-site
description: Build an ad-supported personal website with donation integration (Cash App, Bitcoin, PayPal, etc.) for individuals seeking to monetize a cause, mission, or personal brand. Use when a user wants to create a website that earns money through ads and/or accepts donations, especially for personal causes, faith-based missions, community projects, or bootstrapping a small business.
---

# Ad-Supported Personal Site

Build a complete, publishable personal website that generates revenue through ad placements and direct donations. Designed for individuals with a personal mission, cause, or brand who need income support.

## When to Use

- User wants a website that earns money from ads (Google AdSense, etc.)
- User wants to accept donations via Cash App, Bitcoin, PayPal, or similar
- User has a personal cause, mission, or story to share
- User wants to fund a project, help family, or bootstrap a business

## Workflow

Building an ad-supported personal site involves these steps:

1. Gather user requirements (cause/topic, payment details, audience)
2. Initialize webdev project (static frontend)
3. Design brainstorm and selection
4. Generate custom hero/section images
5. Build full site with content sections, ad zones, and donation integration
6. Add contact/outreach form
7. Deliver with monetization setup instructions

## Step 1: Gather Requirements

Collect these essentials before building:

| Required | Field | Example |
|----------|-------|---------|
| Yes | Topic/cause/mission | Sobriety mentorship, faith, youth outreach |
| Yes | At least one payment method | Cash App tag, Bitcoin address, PayPal link |
| No | Site name / brand name | "Walk By Faith" |
| No | Target audience | At-risk youth, community members |
| No | Future plans | Clothing brand, nonprofit, etc. |

If user provides vague requirements, make creative decisions and inform them.

## Step 2: Site Architecture

Use `webdev_init_project` with `web-static` scaffold. Structure the site as a single-page scrolling experience with these sections:

1. **Hero** — Full-bleed cinematic background, bold headline, CTA buttons
2. **Mission/About** — Who they are, why this matters
3. **Core Content** (1-3 sections) — Topic-specific (e.g., youth, faith, sobriety)
4. **Future Plans** (optional) — Upcoming brand/project teaser
5. **Contact/Outreach Form** — Let visitors reach out directly
6. **Support/Donate** — Payment methods with clear CTAs
7. **Footer** — Branding, quote, attribution

## Step 3: Ad Placement Strategy

Place ad zones at natural content breaks. Use placeholder components that clearly indicate dimensions and where to paste AdSense code:

| Placement | Size | Location |
|-----------|------|----------|
| Leaderboard | 728×90 | Between hero and first content section |
| Rectangle | 336×280 | Sidebar of content sections |
| Leaderboard | 728×90 | Above donation section |

Create a reusable `AdBanner` component with size variants. Include clear comments for the user to replace with their actual ad code.

## Step 4: Donation Integration

For each payment method, create a visually distinct card:

**Cash App:**
- Display cashtag prominently
- Link directly to `https://cash.app/$TAG`
- Use a clear CTA button ("Send via Cash App")

**Bitcoin:**
- Display full wallet address (monospace, break-all)
- Add one-click "Copy Address" button with copied feedback state
- Optionally show QR code

**PayPal (if provided):**
- Link to PayPal.me or donation page

## Step 5: Contact Form

Include a contact/outreach form with:
- Name field (required)
- Email field (optional — "so I can respond")
- Request type dropdown (contextual to the site's mission)
- Message textarea (required)
- Submit button with success state

For static sites without a backend, use one of:
- `mailto:` link construction (opens user's email client)
- Free form service (Formspree, Web3Forms, Getform)
- Upgrade to `web-db-user` for server-side handling

## Step 6: Monetization Setup Instructions

After delivering the site, provide clear next steps:

1. **Google AdSense** — Apply at adsense.google.com, wait for approval, replace placeholder components with actual script tags
2. **Publish** — Click Publish button in Management UI to go live
3. **Drive traffic** — Share link on social media, community groups, messaging apps
4. **Track earnings** — Monitor AdSense dashboard for revenue

## Design Guidelines

- Default to dark, bold aesthetics for mission-driven/faith-based sites
- Use high-contrast typography (condensed display font + readable serif body)
- Generate 3-5 custom images via `generate_image` for hero and key sections
- Include grain/texture overlays for depth
- Use scroll-triggered reveal animations
- Ensure all text is readable against backgrounds
- Mobile-responsive is mandatory — most traffic comes from social media on phones

## Key Reminders

- Never promise specific earnings — ad revenue depends on traffic volume
- Be transparent with the user about realistic expectations
- Ensure the site provides genuine value/content (not just ads)
- All donation methods must be clearly voluntary for visitors
- The site must comply with AdSense policies (original content, no misleading claims)
