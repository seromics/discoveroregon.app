# Discover Oregon Website Summary

**Last Updated**: January 13, 2026

---

## Quick Access

| Resource | URL |
|----------|-----|
| **Live Site** | https://discoveroregon.app |
| **GitHub Repo** | https://github.com/seromics/discoveroregon.app |
| **Cloudflare Dashboard** | https://dash.cloudflare.com (domain: discoveroregon.app) |

---

## Hosting Setup

### GitHub Pages
- **Repo**: `seromics/discoveroregon.app`
- **Branch**: `main` (deploys automatically on push)
- **Custom Domain**: Configured via `CNAME` file pointing to `discoveroregon.app`

### Cloudflare
- **DNS**: Managed through Cloudflare
- **SSL**: Full (strict) - handled by Cloudflare
- **Email Routing**: Configured (see below)

### Deployment
```bash
# From /Users/tylerhulett/Desktop/discoveroregon.app
git add -A && git commit -m "Your message" && git push
```
Changes go live within ~1 minute after push.

---

## Email Setup (Cloudflare Email Routing)

| Address | Forwards To |
|---------|-------------|
| tyler@discoveroregon.app | Your Gmail |
| support@discoveroregon.app | Your Gmail |

**Note**: Receive-only. For sending, use Gmail with "Send as" or just reply from Gmail.

---

## Site Structure

```
discoveroregon.app/
├── index.html              # Homepage (media + apps)
├── CNAME                   # GitHub Pages custom domain
├── .nojekyll               # IMPORTANT: Bypasses Jekyll build (see Troubleshooting)
├── SUMMARY.md              # This file
├── MEDIA_PORTFOLIO.md      # Asset reference doc
│
├── about/
│   └── index.html          # About Tyler page
│
├── media/
│   └── index.html          # Video & Media page
│
├── frog-it/
│   └── index.html          # Frog It! app landing page
│   └── privacy/
│       └── index.html      # Frog It! privacy policy
│
└── images/
    ├── logo-wide.png       # Header logo
    ├── logo-stacked.png    # Alternative logo
    ├── favicon.png         # Browser favicon
    ├── signature.png       # White signature (hero)
    ├── signature-blue.png  # Navy signature (about page)
    ├── hero-aurora.jpg     # Homepage hero image
    ├── frog-dice-large.png # Frog It! app icon
    └── media-preview.png   # Screenshot of short videos
```

---

## Pages Overview

### Homepage (`/`)
- Hero image: Mt. Hood (hood-landing.jpg)
- Quote block with signature
- **Media section** (first): Links to /media/ with preview screenshot
- **Apps section**: Frog It! card with "Coming Soon" badge

### Media (`/media/`)
- **Short Videos**: 8 YouTube embeds (3 per row)
- **Discover Oregon Films**: 4 YouTube embeds (2x2 grid)
- **Video Licensing**: Links to Pond5, Keycut, Getty, Shutterstock, Adobe Stock
- **Audio Licensing**: Links to Pond5, A Sound Effect

### About (`/about/`)
- Bio: Tyler Hulett, PhD, CSO at CDI Labs, built CAAtlas
- Links to LinkedIn, X (@seromics)
- Navy blue signature

### Frog It! (`/frog-it/`)
- App landing page for the dice game
- Links to privacy policy

---

## YouTube Videos on Site

### Discover Oregon Films (4 videos)
- G3wJcq5uF8w
- xsxhS7NmoFI
- 2tksAb7Sjgg
- ULwAUXKYFF4

### Short Videos (8 videos)
- j6DFvKT6qyc
- U1MEPe0dG6c
- VLEA-InQbDc
- CX8DSLWv0C8
- D1417qK60ig
- o8GsQPcjWSU
- ZqykHFYr4fo
- sDoePS95Gss

### Not Currently on Site
- igKK-T0_2rk (Portraits of Oregon - commented out in MEDIA_PORTFOLIO.md)

---

## Stock Licensing Links

### Video
| Platform | URL |
|----------|-----|
| Pond5 | https://www.pond5.com/artist/discoveroregon?tab=footage |
| Keycut | https://www.keycutstock.com/artist/403 |
| Getty Images | https://www.gettyimages.com/search/2/film?artistexact=Tyler%20Hulett |
| Shutterstock | https://www.shutterstock.com/g/discoveroregon/video |
| Adobe Stock | https://stock.adobe.com/contributor/207325769/Tyler%20Hulett |

### Audio
| Platform | URL |
|----------|-----|
| Pond5 | https://www.pond5.com/artist/discoveroregon?tab=sfx |
| A Sound Effect | https://www.asoundeffect.com/shop/sound-designer/discover-oregon |

### Photo (not on site, but available)
| Platform | URL |
|----------|-----|
| Pond5 | https://www.pond5.com/artist/discoveroregon?tab=photo |
| Getty Images | https://www.gettyimages.com/search/2/image-film?family=creative&sort=mostpopular&phrase=%22tyler%20hulett%22 |
| Adobe Stock | https://stock.adobe.com/contributor/207325769/Tyler%20Hulett |
| Shutterstock | https://www.shutterstock.com/g/discoveroregon |

---

## Social Links

| Platform | Handle/URL |
|----------|------------|
| X (Twitter) | @seromics |
| LinkedIn | https://www.linkedin.com/in/tyler-hulett-2a716618/ |
| YouTube | https://www.youtube.com/@tylerhulett2909 |

---

## Design Notes

### Colors
- **Background**: `#fff4ee` (cream)
- **Primary Blue**: `#1a3d5c` (navy)
- **Accent Green**: `#4a7c23`
- **Text**: `#2d3a4a`

### Breakpoints
- **Desktop**: > 768px
- **Mobile**: ≤ 768px
- Only two breakpoints for simplicity

### Typography
- System font stack: `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif`

---

## Where to Go Next

### Immediate Options
- [ ] Add more YouTube videos as you create them
- [ ] Create Pond5 thumbnail images for licensing sections (titles + preview images)
- [ ] Update Frog It! page when app launches (remove "Coming Soon", add store links)

### Future Enhancements
- [ ] Add a proper YouTube playlist section when playlists are organized
- [ ] Consider adding a blog/journal for new video releases
- [ ] Photo licensing section if desired (links ready in MEDIA_PORTFOLIO.md)
- [ ] Analytics (Google Analytics or Cloudflare Web Analytics)

### Frog It! App Launch Checklist
- [ ] Update app status badge from "Coming Soon" to "Available"
- [ ] Add App Store / Google Play buttons
- [ ] Update privacy policy if needed
- [ ] Add screenshots to the landing page

---

## Local Development

The site is plain HTML/CSS - no build step required.

```bash
# Clone the repo
git clone https://github.com/seromics/discoveroregon.app.git

# Open in browser
open index.html

# Or use a local server
python3 -m http.server 8000
# Then visit http://localhost:8000
```

### GitHub Access
- **Account**: seromics
- **Auth**: SSH keys configured on Tyler's Mac Mini
- On a new machine, you'll need to either:
  - Set up SSH keys for the seromics GitHub account, OR
  - Use HTTPS with a personal access token

---

## Troubleshooting

### GitHub Pages Build Failing

**IMPORTANT**: If GitHub Pages shows "errored" or "Page build failed", check the following:

#### 1. Verify `.nojekyll` file exists
```bash
ls -la .nojekyll
```
This file MUST exist in the repo root. It tells GitHub Pages to skip Jekyll processing and serve files directly. Without it, Jekyll may fail on markdown files or other content.

#### 2. Check build status
```bash
# Check Pages status
gh api repos/seromics/discoveroregon.app/pages --jq '.status'

# Check recent builds
gh api repos/seromics/discoveroregon.app/pages/builds --jq '.[0]'

# Check GitHub Actions runs
gh run list --repo seromics/discoveroregon.app --limit 5
```

#### 3. If builds are stuck or errored
Sometimes the deploy job gets stuck in "queued" state. To fix:
```bash
# Trigger a new build with an empty commit
git commit --allow-empty -m "Trigger rebuild" && git push
```

#### 4. Verify site is actually live
Even if API shows "building", the site may already be deployed:
```bash
curl -sI https://discoveroregon.app | head -5
```
Look for `HTTP/2 200` - Cloudflare CDN may serve cached content while GitHub reports building.

### CSS Layout Issues

**DO NOT use `html, body { height: 100%; }`** with flexbox layouts. This was removed from all pages because it caused:
- Hero images to collapse/disappear
- Footers to float above content
- Flex containers to not calculate heights correctly

The correct pattern for sticky footers is:
```css
body {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}
main { flex: 1; }
```

### Changes Not Appearing

1. **Wait 1-2 minutes** after push for GitHub Pages to deploy
2. **Clear Cloudflare cache** if needed (Dashboard > Caching > Purge Everything)
3. **Hard refresh browser** (Cmd+Shift+R on Mac)
4. **Check GitHub Actions** to confirm deploy completed successfully

---

## Company Info

**Discover Oregon Video Productions, LLC**
- Contact: tyler@discoveroregon.app
- Location: Hood River, Oregon

---

*This summary was created to help continue development on another machine.*
