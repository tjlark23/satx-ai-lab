# 2026-04-26 — Cutover satxailab.com → texasailab.com

**Branch:** feat/migrate-to-texas
**Status:** shipped to main, Vercel auto-deployed, 301s verified on production

## Summary

Flipped satxailab.com to a 301 mirror of texasailab.com, mirroring the wilco-ai-lab and atx-ai-lab cutover pattern. Vercel `redirects` with `statusCode: 301` (not `permanent`). Legacy `/ai-training-*` slugs map to the new flattened `/san-antonio/<neighborhood>/` structure on texasailab.com; everything else falls through to `/san-antonio/`.

## Files touched

- `vercel.json` — added (was missing). Full redirect map.
- `sitemap.xml` — deleted. Canonical sitemap now lives on texasailab.com.
- `robots.txt` — kept allow-all, dropped the now-broken `Sitemap:` line that pointed to the deleted file.
- `session-log/2026-04-26-redirect-to-texasailab.md` — this entry.

## Redirect map

| From | To |
| --- | --- |
| `/blog/:slug/` | `https://texasailab.com/articles/:slug/` |
| `/blog/`, `/blog` | `https://texasailab.com/articles/` |
| `/ai-training-san-antonio/` | `https://texasailab.com/san-antonio/` |
| `/ai-training-alamo-heights/` | `https://texasailab.com/san-antonio/alamo-heights/` |
| `/ai-training-new-braunfels/` | `https://texasailab.com/san-antonio/new-braunfels/` |
| `/ai-training-schertz/` | `https://texasailab.com/san-antonio/schertz/` |
| `/ai-training-stone-oak/` | `https://texasailab.com/san-antonio/stone-oak/` |
| `/author/tj-larkin/`, `/author/` | `https://texasailab.com/author/tj-larkin/` |
| `/about/` | `https://texasailab.com/about/` |
| `/contact/`, `/newsletter/` | `https://texasailab.com/contact/` |
| `/services/` | `https://texasailab.com/#services` |
| `/events/` | `https://texasailab.com/san-antonio/#events` |
| `/`, `/:path*` | `https://texasailab.com/san-antonio/` |

All redirects are 301 (not `permanent`) for revertability.

## Verification

```
curl -sI https://www.satxailab.com/ | grep -iE 'HTTP|location'
curl -sI https://www.satxailab.com/blog/ai-101-what-every-business-owner-needs-to-know/ | grep -iE 'HTTP|location'
curl -sI https://www.satxailab.com/ai-training-stone-oak/ | grep -iE 'HTTP|location'
```

Expect 301 with Location pointing to texasailab.com on each.

## Trade-offs / surprises

- `/services/` redirects to a hash anchor on the homepage, matching wilco/atx pattern.
- Static HTML files (`index.html`, neighborhood pages) remain in the repo but are no longer served, since `redirects` fire before file resolution. Left in place to keep the diff surgical.
