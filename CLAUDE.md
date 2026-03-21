# CLAUDE.md

## Project Overview

Apps gallery for Amjad Hussain hosted at apps.amjadhu.com. Static site deployed to GitHub Pages.

## Architecture

- **No build tools or frameworks** - pure HTML/CSS/JS
- Single page site: `index.html` is the only page
- Styles in `css/style.css`
- Animated canvas background rendered with vanilla JS (inline in index.html)
- GitHub Actions deploys the repo root directly to GitHub Pages on push to `main`

## Key Files

- `index.html` - Gallery page with app cards linking to live deployments
- `css/style.css` - Styling, responsive grid, card components, animations
- `CNAME` - Custom domain configuration (apps.amjadhu.com)
- `.github/workflows/deploy.yml` - GitHub Pages deploy workflow

## Apps Showcased

| App | URL | Hosting |
|-----|-----|---------|
| The Commission | https://amjadhu.github.io/the-commission/ | GitHub Pages |
| AI Terminal | https://ai-terminal-one.vercel.app | Vercel |
| College Explorer | https://amjadhu.github.io/college-explorer/ | GitHub Pages |
| Vantage | https://github.com/amjadhu/vantage | Vercel (repo link for now) |
| Syslens | https://github.com/amjadhu/syslens | CLI tool (repo link) |

## Adding a New App

Add a new `.card` anchor element inside the `.grid` div in `index.html`:

```html
<a href="LIVE_URL" target="_blank" rel="noopener noreferrer" class="card">
  <div class="card-icon">EMOJI</div>
  <h2>App Name</h2>
  <p>Short description.</p>
  <span class="card-tag">Tag</span>
</a>
```

## Design Decisions

- Dark theme (#0a0a0f background) matching amjadhu.com
- Same animated orbs background and dot grid overlay as main site
- Inter font (weights 300, 400, 500)
- Responsive card grid (auto-fill, min 260px)
- Glass-morphism cards with backdrop blur
- Indigo accent color on hover (matching main site's LinkedIn button hover)

## Working With This Site

- No install or build step needed - just edit files and push
- Test locally by opening `index.html` in a browser
- All deployment is automatic via GitHub Actions on push to main
- Keep the site lightweight - avoid adding frameworks or build tools
