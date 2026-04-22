# sbvandeven.com

Source for **sbvandeven.com** — the Authentic Connection Institute (ACI). Personal hub for Stephan van de Ven. Hosted on GitHub Pages, served from a custom domain.

## Stack

- Plain HTML + CSS (no build step, no generator)
- GitHub Pages for hosting
- Custom domain via DNS (A-records → GitHub Pages IPs)
- Typography: [Fraunces](https://fonts.google.com/specimen/Fraunces) (headings) + [Inter](https://fonts.google.com/specimen/Inter) (body), loaded from Google Fonts
- Hand-drawn SVG illustrations via Obsidian Excalidraw plugin

## Architecture

```
/                ACI landing (vision, belief, goal, roles)
/coaching/       Coaching role
/facilitation/   Facilitation role
/writing/        Writing practice
/speaking/       Speaking role
/assets/         Excalidraw SVGs
/css/style.css   Shared stylesheet
/CNAME           Custom domain for GitHub Pages
```

**Phase 2 (later):** digital garden at `notes.sbvandeven.com` (Quartz), sourced from a separate `sbvandeven-garden/` folder.

## Local preview

Open `index.html` in a browser. Relative links work when files are served; if opening directly from the filesystem, navigating between pages may require a local server. Quickest option:

```bash
cd ~/Documents/sbvandeven-website
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publishing

1. Create a GitHub repo (public), e.g. `<username>.github.io` or `sbvandeven.com`.
2. Push this folder to `main`.
3. In the repo's **Settings → Pages**, set Source = `main` branch / `/` root.
4. Confirm GitHub detects the `CNAME` file and shows `sbvandeven.com` under Custom domain.
5. At the DNS registrar (Totaal Holding), set A-records for `sbvandeven.com` to:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
6. Add CNAME for `www.sbvandeven.com` → `<username>.github.io`.
7. Wait for DNS to propagate (up to 24h), then confirm HTTPS via Let's Encrypt auto-provisioning in GitHub Pages settings.

## Content placeholders

Pages include `{{TOKEN}}` placeholders for copy that still needs Stephan's voice pass. See `Efforts/sbvandeven.com Website/CONTENT_DRAFT.md` in the Eldunari vault for draft language per section.

Placeholders currently in the files:

- `{{ACI_TAGLINE}}`, `{{ACI_SUB_TAGLINE}}`
- `{{COACHING_*}}` — lead, audience, approach, story
- `{{FACILITATION_*}}` — lead, offerings, track record prose, approach
- `{{WRITING_*}}` — lead, in-progress pieces, upcoming blurbs
- `{{SPEAKING_*}}` — lead, topics, formats, past appearances
- `{{CALENDLY_*_URL}}` — booking links (one shared or four role-specific)

## Planning docs

- `/Users/Stephan/.claude/plans/i-think-that-a-pure-manatee.md` — approved Plan v2.0
- `Efforts/sbvandeven.com Website/WORKLOG.md` — ongoing task log
- `Efforts/sbvandeven.com Website/CONTENT_DRAFT.md` — copy drafts
- `Efforts/sbvandeven.com Website/DECISION_PACKAGE.md` — voice research (Apr 9, partially reusable)

## License

Content copyright Stephan van de Ven. Site source is personal and not open-sourced.
