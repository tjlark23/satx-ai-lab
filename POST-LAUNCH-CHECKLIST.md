# SATX AI Lab — Post-Launch Checklist

The site is live. These are the free external signals that take 2-15 minutes each but compound into real GEO authority over weeks. Do them now while the site is fresh.

## TIER 1 — DO TODAY (15 minutes total)

### 1. Google Search Console — Submit the sitemap
- Go to: https://search.google.com/search-console
- Click "Add property" → enter: https://www.satxailab.com
- Verify ownership (easiest: DNS TXT record via Cloudflare, or HTML file upload)
- Once verified, go to Sitemaps → paste: https://www.satxailab.com/sitemap.xml → Submit
- **Why it matters:** Tells Google the site exists and which URLs to crawl. Without this, it could take weeks to get indexed.

### 2. Bing Webmaster Tools — Submit the sitemap
- Go to: https://www.bing.com/webmasters
- Sign in with Google (yes, Bing accepts Google login now), import from Search Console if you want (saves setup time)
- Add: https://www.satxailab.com → Submit sitemap
- **Why it matters:** Bing powers ChatGPT search results. Submitting here directly helps ChatGPT citation coverage.

### 3. IndexNow submission
- IndexNow pushes your URLs directly to Bing and Yandex instantly.
- Vercel has a built-in IndexNow integration — enable it in the project settings, or Claude Code can add the IndexNow key file to `/public/`.
- **Why it matters:** Immediate indexing in Bing = faster ChatGPT inclusion.

### 4. Google Business Profile — Create and verify
- Go to: https://business.google.com
- Create a profile for "SATX AI Lab" with address in Liberty Hill, TX (TJ's business address) or San Antonio if TJ has an SA address/mail drop
- Service area: San Antonio, Alamo Heights, Stone Oak, Schertz, New Braunfels
- Website: https://www.satxailab.com
- Primary category: Business Management Consultant (or AI consultant if listed)
- **Why it matters:** Biggest single GEO signal for local businesses. Google uses this profile as a primary entity source.

### 5. Cloudflare analytics or Vercel analytics enabled
- Verify analytics are on so we can measure traffic from day one.
- **Why it matters:** Can't optimize what you can't measure.

## TIER 2 — DO THIS WEEK (1 hour total)

### 6. Apple Business Connect — Create listing
- Go to: https://businessconnect.apple.com
- Sign in with Apple ID → Add business → SATX AI Lab
- Address, service area, website
- **Why it matters:** Powers Apple Maps, Siri, and increasingly Apple Intelligence AI results.

### 7. Directory listings (batch these)
Submit SATX AI Lab to:
- Yelp Business: https://biz.yelp.com
- Clutch: https://clutch.co (IT consulting / AI section — they review listings manually, takes a week)
- LinkedIn Company Page: Create "SATX AI Lab" as a LinkedIn Company Page, add TJ as admin, link website
- Facebook Business Page: Create "SATX AI Lab" — link website, add service area
- **Why it matters:** Every directory listing is a citation source for AI engines. LinkedIn Company Page in particular correlates strongly with AI citation density.

### 8. Chamber of Commerce listings
- San Antonio Chamber: https://www.sachamber.org (paid, $400-500/yr — decide based on budget)
- Free alternatives: local BNI chapters, Greater San Antonio Better Business Bureau, NextDoor Business
- **Why it matters:** Local authority signal. Chambers are cited by AI engines when someone asks "local business in San Antonio."

### 9. AI-specific directories (new category, underused)
- There.ai, FutureTools.io directory, AIxplorer, TopAI Tools — submit SATX AI Lab to AI consultancy categories on each
- **Why it matters:** These directories are explicitly scraped by GPTBot, ClaudeBot, and PerplexityBot. Cheap citation sources.

## TIER 3 — WITHIN 30 DAYS (for real GEO compounding)

### 10. Cross-link from WilCo and ATX (already done in this deploy)
- Done as part of this launch. Both sister sites now cross-link to SATX in /about, in every sameAs array, and in llms.txt.
- Verify after crawlers have picked them up.

### 11. Local press mention
- Email 1-2 San Antonio business journalists (San Antonio Business Journal, Rivard Report, SA Current business section) with a short pitch about "the AI consultancy that teaches local SA businesses instead of selling enterprise AI."
- **Why it matters:** One earned media mention with a backlink is worth 10 directory listings.

### 12. Reddit / Quora seeding (organic, not spam)
- Find 2-3 existing questions on r/SanAntonio, r/smallbusiness, or Quora that are relevant to AI for local businesses
- Answer genuinely with real advice, mention SATX AI Lab only when directly relevant
- **Why it matters:** Reddit mentions correlate with AI citations per Ahrefs data.

### 13. YouTube channel (when TJ is ready)
- Parked for now per TJ. This is the biggest ceiling lift when activated.
- **Why it matters:** YouTube presence correlates 0.737 with AI citations — the strongest single brand signal.

### 14. Schedule re-audit in 30 days
- Run the GEO audit again on satxailab.com after 30 days to see score trajectory
- Claude.ai can handle this — just ask.

---

## Reminder from Claude

Claude should proactively remind TJ about these post-launch items at:
- Immediately after every local lead-gen site launch
- 7 days after launch (check Tier 2 progress)
- 30 days after launch (Tier 3 progress + re-audit)

If TJ hasn't done Tier 1 items within 48 hours, Claude should bring them up again.
