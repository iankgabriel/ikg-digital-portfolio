# IKG Digital Portfolio

The source for **[ikgdigital.com](https://www.ikgdigital.com)**, my portfolio site as an AI Automation Specialist. It showcases the workflow automations I've built in Make, n8n, Zapier, and GoHighLevel, each with a before-and-after summary and a short case study.

![IKG Digital portfolio preview](og-image-v2.png)

## What's on the site

- **Home:** an introduction, the platforms I work with, and my certificates, which open in a pop-up
- **About:** my background, including how 8 years in video editing and production shaped the way I build automations
- **Projects:** tabs for Make, n8n, Zapier, and GoHighLevel. Each project card opens a pop-up with screenshots, Before and After boxes, the result, and a case study.
- **Contact:** email, WhatsApp, and LinkedIn

The site has a light mode by default and a dark mode toggle, and it's built to work on both desktop and phone.

## How it's built

The whole site is a single `index.html` file with no framework and no build step. The four pages live inside that one file and switch with hash links (`#home`, `#about`, `#projects`, `#contact`), so moving between pages is instant and nothing reloads.

All images are embedded directly in the file, which keeps it fully self-contained. The trade-off is file size, so link previews go through a small separate page (see `share.html` below).

Headings use Atkinson Hyperlegible and body text uses Inter. The design was inspired by the Athos Framer template.

## Files

| File | Purpose |
|---|---|
| `index.html` | The entire site |
| `share.html` | A lightweight page with link-preview tags that sends visitors to the homepage. Used when sharing the site on LinkedIn, since the full homepage is too large for LinkedIn to preview. |
| `og-image.png`, `og-image-v2.png` | Link preview images |
| `robots.txt` | Allows search engines to crawl the site |

## Hosting and deployment

The site is hosted on **Cloudflare Pages**, connected to this repo. Every push to `main` deploys automatically, and any deployment can be rolled back from the Cloudflare dashboard.

Before pushing a change, I compare the new file against the current version line by line and screenshot every page on desktop and phone with Playwright, so nothing reaches the live site unchecked.

## Related

- **[automation-workflows](https://github.com/iankgabriel/automation-workflows):** the workflows behind the projects on this site, with write-ups, screenshots, and exported files

---

Built by Ian Kennedy Gabriel, IKG Digital. The site's text, images, and project content belong to me. The code is shared here for reference.
