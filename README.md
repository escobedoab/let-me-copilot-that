# Let Me Copilot That For You

A playful, constructive Microsoft Copilot-themed reimagining of the classic "let me search that for you" interaction.

This is intentionally **not** a clone of the original site's assets, branding, copy, or code. It borrows the interaction pattern: generate a link, animate the act of asking, and point the viewer toward a helpful destination.

## What the original pattern does

Research summary from the current public site and search snippets:

- The homepage is a JavaScript-driven static page with a search input and two search buttons.
- Entering text generates a shareable URL using a query parameter like `?q=...`.
- Opening that URL animates a fake cursor, types the query into the search field, clicks the search button, shows a punchline, and redirects to a search destination.
- The current site also includes link copy, preview, URL shortening, share buttons, localization helpers, analytics, and merch/sponsor areas.

## What this version adds

- A kinder, workplace-safe tone.
- Copilot-style prompt coaching: context, outcome, and constraints.
- Multiple destinations: Copilot, Bing, Microsoft Learn, and Microsoft 365 search.
- No analytics, no third-party scripts, no backend, and no stored user data.
- GitHub Pages-ready static deployment.
- Accessibility basics, responsive layout, and reduced-motion support.

## Run locally

Open `index.html` directly in a browser, or serve the folder with any static server:

```powershell
cd .\let-me-copilot-that
npx serve .
```

## Deploy with GitHub Pages

1. Create a new public GitHub repository.
2. Upload the contents of this folder.
3. In the repo, go to **Settings > Pages**.
4. Set the source to **Deploy from a branch**, choose `main`, and select `/root`.

## URL format

```text
/?q=How%20do%20I%20use%20Copilot&to=copilot&tone=kind
```

Parameters:

- `q`: the question or task to animate.
- `to`: `copilot`, `bing`, `learn`, or `work`.
- `tone`: `kind`, `spicy`, or `coach`.

## Public positioning

Recommended tagline:

> A cheerful prompt-coaching nudge for people who ask before they ask Copilot.

Recommended disclaimer:

> Unofficial parody/helper site. Not affiliated with Microsoft.

## Value-add backlog

- Add prompt recipe presets for common scenarios: email draft, executive summary, meeting agenda, troubleshooting, and Microsoft Learn path.
- Add "better prompt diff" showing the original question vs. the improved Copilot prompt.
- Add Slack/Teams-safe copy snippets that are playful but not mean.
- Add a "private mode" that keeps the query in the URL hash instead of query string.
- Add localization once the core flow is stable.
- Add lightweight visual tests with Playwright before publishing widely.
