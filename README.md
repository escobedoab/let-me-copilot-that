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
- Link creators can choose the recipient experience: stop on the coaching page (default), or auto-submit to Bing after the animation.
- Submit actions always open Bing AI Search in a new tab with the rewritten prompt. If a browser blocks the new tab, the page stays visible and asks the recipient to click submit.
- Rewritten prompts dynamically classify the original ask (compare, draft, plan, troubleshoot, summarize, research, code, explain, or general), identify intent/context/output needs, and then recreate a clearer prompt.
- Dynamic rewrites now use a five-part structure: intent, context needed, desired output, clarifying questions, and a final rewritten prompt.
- Rewritten prompts avoid awkward AI preambles and focus on making the user's original request clearer, more structured, and easier to answer.
- Exact prompt mode skips rewriting entirely; it animates and submits the original prompt exactly as typed.
- Exact prompt mode is the default style. Helpful and spicy modes show the rewrite scaffold immediately, then animate the original request inside it so the added structure is clear.
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
/?q=How%20do%20I%20use%20Copilot&to=bing&submit=manual&style=helpful
```

Parameters:

- `q`: the question or task to animate.
- `to`: `copilot`, `bing`, `learn`, or `work`.
- `submit`: `manual` or `auto`. Auto mode forces the destination to Bing and submits after the animation.
- `style`: `helpful`, `spicy`, or `exact`. Exact mode skips rewriting and sends the original prompt.

## Version display

The footer displays the current site version, for example:

```text
Version v0.9.1
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

