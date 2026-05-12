# HubSpot CRM Guide 2026 — Simplify Group

The 2026 HubSpot operating manual for Simplify Group teams, with Breeze AI updates.

## What's in this repo

```
.
├── index.html          # The complete guide (single file, self-contained)
├── images/             # Screenshot folder (placeholders are in the HTML)
└── README.md           # This file
```

## Live site

Once GitHub Pages is enabled, this will be at:
`https://<your-org>.github.io/<repo-name>/`

---

## Deploy to GitHub Pages (5-minute setup)

1. Create a new GitHub repository (suggested name: `hubspot-crm-guide`).
2. Upload `index.html` and the `images/` folder to the root.
3. Go to **Settings → Pages**.
4. Under **Source**, choose **Deploy from a branch**.
5. Select **main** branch and **/ (root)** folder. Click **Save**.
6. Wait 1-2 minutes. Your live URL will appear at the top of the Pages settings.

That's it. No build step, no dependencies, no Node, nothing.

---

## How to add the real screenshots

The guide currently shows 26 styled placeholder boxes where screenshots will go. Each placeholder displays:

- The caption (what the screenshot should show)
- The expected filename (e.g., `images/01-contact-module-overview.png`)

### To replace a placeholder with a real image

Open `index.html`, find the placeholder (search by filename, e.g. `01-contact-module-overview.png`), and replace this block:

```html
<figure class="screenshot">
  <div class="screenshot-placeholder">
    <div class="screenshot-icon">...</div>
    <div class="screenshot-caption">Contact module overview in HubSpot CRM</div>
    <span class="screenshot-filename">images/01-contact-module-overview.png</span>
  </div>
</figure>
```

with this:

```html
<figure class="screenshot">
  <img src="images/01-contact-module-overview.png" alt="Contact module overview in HubSpot CRM" style="width: 100%; border-radius: 10px; border: 1px solid #e6e8ec;">
  <figcaption style="text-align: center; font-size: 13px; color: #6e6e72; margin-top: 8px;">Contact module overview in HubSpot CRM</figcaption>
</figure>
```

### Recommended screenshot specs

- Format: PNG
- Width: 1200-1600px (full HD captures work great)
- Compression: use TinyPNG or Squoosh before uploading to keep page load fast
- Naming: keep the suggested filenames so the order stays clean

### Full list of screenshots needed

| # | Filename | Shows |
|---|----------|-------|
| 1 | 01-contact-module-overview.png | Contact module overview |
| 2 | 02-contact-status-section.png | Status section with all key properties |
| 3 | 03-company-module-overview.png | Company module full view |
| 4 | 04-deal-module-overview.png | Deal section with all properties |
| 5 | 05-deal-properties-detail.png | Deal dates and financial fields |
| 6 | 06-deal-add-company.png | Click Add in Companies panel |
| 7 | 07-deal-search-account.png | Search and select account |
| 8 | 08-task-creation-panel.png | Task creation panel |
| 9 | 09-log-meeting-panel.png | Log Meeting panel |
| 10 | 10-calendar-connect.png | Calendar connection screen |
| 11 | 11-calendar-provider-choice.png | Provider choice (Google/Outlook/Exchange) |
| 12 | 12-email-meeting-options.png | Email composer Meeting options |
| 13 | 13-scheduling-link-edit.png | Insert scheduling link |
| 14 | 14-select-times-calendar.png | Select times calendar view |
| 15 | 15-manage-meeting-link.png | Manage Meeting Link Automation tab |
| 16 | 16-log-call-panel.png | Log Call panel |
| 17 | 17-outlook-ribbon.png | HubSpot Sales add-in in Outlook ribbon |
| 18 | 18-hubspot-sales-panel.png | HubSpot Sales panel with message tools |
| 19 | 19-email-integration-settings.png | Email settings with connected inbox |
| 20 | 20-call-recording.png | Active call with Record button + consent pop-up |
| 21 | 21-breeze-studio-dashboard.png | Breeze Studio dashboard |
| 22 | 22-prospecting-agent-dashboard.png | Prospecting Agent overview |
| 23 | 23-selling-profile-setup.png | Selling Profile setup |
| 24 | 24-sales-workspace-pipeline.png | Sales Workspace pipeline view |
| 25 | 25-buyer-intent-tab.png | Buyer Intent tab |
| 26 | 26-breeze-assistant-chat.png | Breeze Assistant chat panel |

---

## Features built into the guide

- **Sticky left sidebar** with grouped navigation (CRM Properties / Daily Workflow / Breeze AI)
- **Right rail** "On this page" mini-TOC that updates as you scroll
- **Live search** — filters sidebar nav as you type (press `/` to focus, `Esc` to clear)
- **Active section highlighting** — sidebar and TOC both update based on scroll position
- **Dark mode** toggle (saves preference to localStorage)
- **Mobile responsive** — sidebar collapses into a slide-out drawer below 860px
- **Print-friendly** — clean layout when printed, sidebar/TOC hidden
- **Scroll progress bar** at the top of the page
- **Anchor links** on every heading (hover to see the # link)
- **Breadcrumbs** for navigation context (per 2026 SEO best practice)
- **Simplify Group brand** — Arrow Green #2D8C4E, Near Black #221F20, Proxima Nova typography (per 2026 Simplify Family Brand Guidelines v1.0)

## Tech notes

- Pure HTML + CSS + vanilla JS. No framework, no build, no dependencies.
- Single self-contained file. Drops into any static host (GitHub Pages, Netlify, S3, internal SharePoint).
- Fonts loaded from Google Fonts CDN: Source Sans 3 (Proxima Nova substitute, per Simplify Group brand spec).

## Maintenance

When HubSpot rolls out new features, update the relevant section in `index.html`. The sidebar nav, breadcrumbs, and TOC will auto-update based on section IDs.

---

*Copyright © 2026 Simplify Group. All Rights Reserved. Confidential and Proprietary.*
