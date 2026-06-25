# Let Me Copilot That For You

A playful, constructive reimagining of the classic "let me search that for you" interaction, tuned for Bing search and Copilot-era prompt coaching.

This is intentionally **not** a clone of the original site's assets, branding, copy, or code. It borrows the interaction pattern: generate a link, animate the act of asking, and point the viewer toward a helpful destination.

## What the original pattern does

Research summary from the current public site and search snippets:

- The homepage is a JavaScript-driven static page with a search input and two search buttons.
- Entering text generates a shareable URL using a query parameter like `?q=...`.
- Opening that URL animates a fake cursor, types the query into the search field, clicks the search button, shows a punchline, and redirects to a search destination.
- The current site also includes link copy, preview, URL shortening, share buttons, localization helpers, analytics, and merch/sponsor areas.

## What this version adds

- A kinder, workplace-safe voice.
- Copilot-style prompt coaching: context, outcome, and constraints.
- Bing AI Search is the default destination using `https://www.bing.com/mt?q=...`.
- Optional destinations include Copilot, Microsoft Learn, and Microsoft 365 search.
- Copilot destination copies the improved prompt before opening Copilot because the public Copilot site does not reliably support a prefilled prompt URL.
- The submit button animates before opening Bing with the rewritten prompt already searched.
- The share button uses the browser share sheet when available and falls back to copying the hosted link.
- Link creators can choose the recipient experience: stop on the coaching page, or auto-submit to Bing after the animation.
- Submit actions always open Bing AI Search in a new tab with the rewritten prompt. If a browser blocks the new tab, the page stays visible and asks the recipient to click submit.
- Rewritten prompts dynamically classify the original ask (compare, draft, plan, troubleshoot, summarize, research, code, explain, or general) and reconstruct it into a structured AI-ready request.
- Dynamic rewrites include a direct answer request, context/assumptions, intent-specific output format, key points, and clarifying questions.
- Rewritten prompts avoid awkward AI preambles and focus on making the user's original request clearer, more structured, and easier to answer.
- Bing ultimately controls whether an AI answer appears; account, region, query, and feature rollout can still affect the result.
- No analytics, no third-party scripts, no backend, and no stored user data.
- GitHub Pages-ready static deployment.
- Accessibility basics, responsive layout, and reduced-motion support.

## Deploy with GitHub Pages

1. Create a new public GitHub repository.
2. Upload the contents of this folder.
3. In the repo, go to **Settings > Pages**.
4. Set the source to **Deploy from a branch**, choose `main`, and select `/root`.

## URL format

```text
/?q=How%20do%20I%20use%20Copilot&to=bing&submit=auto&style=helpful
```

Parameters:

- `q`: the question or task to animate.
- `to`: `copilot`, `bing`, `learn`, or `work`.
- `submit`: `manual` or `auto`. Auto mode forces the destination to Bing and submits after the animation.
- `style`: `helpful` or `spicy`. This changes the on-page coaching voice, not the best-practice rewrite structure.

## Version display

The footer displays the current site version, for example:

```text
Version v0.8.5
```

After each publish, verify the visible footer version to make sure the browser is not showing a cached copy.

## Public positioning

Recommended tagline:

> A cheerful prompt-coaching nudge for people who ask before they search.

Recommended disclaimer:

> Unofficial prompt helper. Not affiliated with Microsoft.

Customer-ready content posture:

- Keep the tone playful, not mean.
- Avoid official Microsoft logos or brand marks unless approved.
- Do not collect analytics or store prompts.
- Treat copied prompts as user-provided content carried only in the URL.
- Be transparent that the site encourages AI-search responses but cannot force Bing to show one every time.

## Value-add backlog

- Add prompt recipe presets for common scenarios: email draft, executive summary, meeting agenda, troubleshooting, and Microsoft Learn path.
- Add "better prompt diff" showing the original question vs. the improved Copilot prompt.
- Add Slack/Teams-safe copy snippets that are playful but not mean.
- Add a "private mode" that keeps the query in the URL hash instead of query string.
- Add localization once the core flow is stable.
- Add lightweight visual tests with Playwright before publishing widely.

