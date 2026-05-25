---
name: ad-supported-music-artist-site
description: Build an ad-supported personal website for independent music artists with streaming links, merch teasers, fan donations, and booking contact. Use when a musician, rapper, singer, or producer wants a website to grow their fanbase, earn ad revenue, accept tips/donations, and promote their music or upcoming releases.
---

# Ad-Supported Music Artist Site

Build a complete, publishable artist website that generates revenue through ad placements and fan donations while promoting music, merch, and bookings. Designed for independent artists who want a professional web presence without label backing.

## When to Use

- Independent artist wants a website to promote their music
- Artist wants to earn passive income from ads on their site
- Artist wants to accept fan tips/donations (Cash App, Bitcoin, PayPal, Venmo)
- Artist wants a hub linking all streaming platforms
- Artist needs a booking/contact page for shows and features

## Workflow

Building an ad-supported music artist site involves these steps:

1. Gather artist requirements (name, genre, payment, streaming links)
2. Initialize webdev project (static frontend)
3. Design brainstorm and selection
4. Generate custom visuals (artist promo shots, album art backgrounds)
5. Build full site with music, bio, merch, ad zones, and donation integration
6. Add booking/contact form
7. Deliver with monetization setup instructions

## Step 1: Gather Requirements

Collect these essentials before building:

| Required | Field | Example |
|----------|-------|---------|
| Yes | Artist/stage name | "Lil Redemption", "KXNG Verse" |
| Yes | Genre/vibe | Hip-hop, R&B, Gospel Rap, Indie |
| Yes | At least one payment method | Cash App tag, Bitcoin, PayPal, Venmo |
| No | Streaming links | Spotify, Apple Music, SoundCloud, YouTube |
| No | Social media handles | Instagram, TikTok, Twitter/X |
| No | Upcoming release info | Album name, single drop date |
| No | Merch plans | Clothing line, accessories |
| No | Booking email | For shows, features, collabs |

If user provides vague requirements, make creative decisions matching their genre and inform them.

## Step 2: Site Architecture

Use `webdev_init_project` with `web-static` scaffold. Structure as a single-page scrolling experience:

1. **Hero** — Full-bleed artist image or album art, artist name, tagline, play button
2. **Music** — Embedded players or streaming platform links (Spotify, Apple Music, SoundCloud, YouTube)
3. **About/Bio** — Artist story, journey, influences, message
4. **Merch** (optional) — Coming soon teaser or live store link
5. **Videos** (optional) — YouTube embeds or music video links
6. **Booking/Contact Form** — For shows, features, press inquiries
7. **Support the Artist** — Donation/tip methods with clear CTAs
8. **Footer** — Social links, copyright, streaming icons

## Step 3: Ad Placement Strategy

Place ad zones at natural content breaks without disrupting the artist's brand:

| Placement | Size | Location |
|-----------|------|----------|
| Leaderboard | 728×90 | Between hero and music section |
| Rectangle | 336×280 | Beside bio or below music player |
| Leaderboard | 728×90 | Above support/donate section |

Create a reusable `AdBanner` component with size variants. Style ads to blend with the site's dark aesthetic. Include clear comments for the artist to replace with their actual AdSense code.

## Step 4: Music Integration

Embed or link to streaming platforms:

**Spotify:**
- Use Spotify embed iframe: `https://open.spotify.com/embed/track/TRACK_ID`
- Compact player style works best in dark layouts

**Apple Music:**
- Link button to Apple Music artist page

**SoundCloud:**
- Use SoundCloud embed widget for unreleased/exclusive tracks

**YouTube:**
- Embed latest music video or lyric video
- Link to full channel

**Link Aggregator Section:**
- Grid of platform icons (Spotify, Apple, SoundCloud, YouTube, Tidal, etc.)
- Each links to the artist's profile on that platform

## Step 5: Donation/Tip Integration

For each payment method, create a visually distinct card matching the artist's brand:

**Cash App:**
- Display cashtag prominently
- Link directly to `https://cash.app/$TAG`
- CTA: "Buy Me a Beat" or "Support the Grind"

**Bitcoin:**
- Display full wallet address (monospace, break-all)
- One-click "Copy Address" button with feedback state

**PayPal / Venmo (if provided):**
- Direct link buttons

**Framing:**
- Position donations as "Support the Music" or "Fuel the Next Project"
- Never frame as begging — frame as fan investment in independent art

## Step 6: Booking/Contact Form

Include a booking and contact form with:
- Name field (required)
- Email field (required)
- Inquiry type dropdown: Booking (Shows), Feature Request, Press/Interview, Fan Message, Business/Other
- Message textarea (required)
- Budget range (optional, for bookings)
- Submit button with success state

For static sites without a backend, use:
- `mailto:` link construction with pre-filled subject
- Free form service (Formspree, Web3Forms)
- Upgrade to `web-db-user` for server-side handling

## Step 7: Monetization Setup Instructions

After delivering the site, provide clear next steps:

1. **Google AdSense** — Apply at adsense.google.com, wait for approval, replace placeholder components with script tags
2. **Publish** — Click Publish button in Management UI to go live
3. **Drive traffic** — Share link in Instagram bio, TikTok bio, YouTube descriptions, tweet pinned post
4. **Link in Bio** — Use this site AS the link-in-bio instead of Linktree
5. **Track earnings** — Monitor AdSense dashboard for revenue

## Design Guidelines

- **Dark, moody aesthetics** by default for hip-hop/rap/R&B artists
- **Neon or bold accent colors** matching the artist's brand (gold, red, electric blue, purple)
- **Typography**: Heavy condensed display font (Bebas Neue, Oswald, Anton) + clean sans-serif body (Inter, Manrope)
- Generate 3-5 custom images: artist promo shot, album art background, concert energy, studio vibe
- Use grain/noise textures for grit and authenticity
- Parallax or subtle scroll animations for cinematic feel
- Audio waveform or equalizer visual motifs
- Mobile-first — fans will visit from Instagram/TikTok links on their phones

**Genre-specific adjustments:**
- Hip-hop/Rap: Dark, bold, street energy, gold/red accents
- R&B/Soul: Warm tones, smooth gradients, elegant type
- Gospel/Christian Rap: Dark with divine light, gold, scripture integration
- Indie/Alternative: Muted earth tones, organic textures, handwritten elements
- Electronic/EDM: Neon, glitch effects, dark backgrounds, geometric shapes

## Key Reminders

- Never promise specific earnings — ad revenue depends on traffic volume
- The site should feel like a professional artist page, not an ad farm
- Ads should be present but not dominate the experience
- All donation methods must feel like fan support, not charity
- Comply with AdSense policies (original content, no misleading claims)
- Respect copyright — only embed the artist's own music
- Include streaming links prominently — the site should drive streams too
