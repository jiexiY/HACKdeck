# HACKdeck

### Find the right event. See the timeline. Make room to build.

[Explore HACKdeck](https://hackdeck-app.vercel.app/) · [简体中文](README.zh-CN.md) · [Español](README.es.md)

HACKdeck is a multilingual discovery platform for hackathons, build weeks, and developer programs. It turns scattered event announcements into a connected chronological deck, helping builders compare opportunities before committing their time.

## The experience

- **A draggable timeline:** browse chronologically aligned event cards and understand overlapping dates.
- **Practical filters:** narrow opportunities by organizer, location, remote participation, dates, deadlines, prizes, eligibility, format, and status.
- **Source-linked details:** inspect event information and follow official or organizer links.
- **Live catalog updates:** discover newly verified opportunities and event changes as they are published to the site.
- **Three interface languages:** English, Mandarin Chinese, and Spanish.
- **Local saves:** keep a shortlist in the browser without creating an account.
- **Portable backups:** export saved information as JSON and import it in another browser or device.
- **Responsive layout:** use the discovery flow across desktop and smaller screens.

## Why a deck?

An event directory answers what exists. Planning requires more: when applications close, which events overlap, whether participation is remote, and whether the opportunity fits a builder's interests and eligibility.

HACKdeck brings those details together in a visual timeline. The interface is designed to make comparison and shortlisting easier without adding a registration barrier.

## Using HACKdeck

1. Open the [live site](https://hackdeck-app.vercel.app/).
2. Choose a language and adjust the filters.
3. Explore the timeline and open an event's details.
4. Check the organizer's current information before applying.
5. Save useful events and export a backup when moving between browsers.

## Live updates and data quality

The catalog is curated from official company, university, and organizer sources. A monitored organization is a discovery lead, not an event by itself.

HACKdeck publishes live catalog updates as new opportunities and event changes are verified and released to the site. Updates may be delayed by regional differences in source availability or access, as well as verification and publishing time. Refresh the site to load the latest published catalog.

Dates, eligibility, prizes, availability, and application rules can change. Check the original source before making plans. The data validator flags records that need maintenance, including ended events that still need archiving.

## Engineering overview

HACKdeck uses React 19, Vite, Tailwind CSS, Radix UI components, Lucide icons, and OGL visual effects.

- `src/App.jsx` coordinates the timeline, filtering, details, and saved-event experience.
- `src/data/events.js` contains event records and source metadata.
- `src/data/i18n.js` provides interface translations.
- `scripts/validate-events.mjs` checks catalog consistency.
- `src/components/` contains reusable interface and visual components.

## Run locally

Use Node.js 20 or later and pnpm.

```bash
pnpm install --frozen-lockfile
pnpm dev
```

Open the local address printed by Vite.

```bash
pnpm validate:data
pnpm build
pnpm preview
```

Data-validation findings and compilation results are separate checks. Resolve catalog findings against the organizer's source before publishing an event-data update.

## Saved events and privacy

Saved events stay in the visitor's browser through local storage; the application does not require an account or upload that shortlist. Clearing browser storage can remove saved information. Use JSON export and import for a portable backup; this is not automatic cross-device synchronization.

## Contributing

For a new event or correction, provide an official or organizer source, preserve unknown details, check duplicate IDs and URLs, and archive ended events. Interface contributions should preserve keyboard access, readable labels, responsive behavior, and all three supported languages.

## Copyright

Copyright © 2026 Jiexi Yang. All rights reserved.
This project is publicly available for viewing and portfolio evaluation only.
