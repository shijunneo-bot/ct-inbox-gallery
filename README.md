# CleverTap Field Guide 13 · App Inbox + Web Inbox Gallery

A design-first, single-page field guide to CleverTap App Inbox and Web Inbox. Sixteen inbox design patterns, ninety use cases across fifteen verticals, a build-vs-buy spectrum, a push-vs-inbox decision table, a stats explainer, and a twenty-question FAQ. It opens with an intro splash; pressing Enter, clicking, or scrolling opens the guide.

Live target: `https://shijunneo-bot.github.io/ct-inbox-gallery/`

## What is in this bundle

| File | Purpose |
| --- | --- |
| `index.html` | The whole guide. Self-contained (all CSS and JS inline; only Google Fonts load externally). The favicon is embedded and matches the rest of the network. |
| `og-image.png` | 1200x630 social share card, referenced by the Open Graph and Twitter tags. |
| `robots.txt` | Allows all crawlers, explicitly welcomes AI answer engines, points to the sitemap. |
| `sitemap.xml` | Single-URL sitemap for the page. |
| `llms.txt` | A plain-text summary for AI answer engines (AEO), with the key facts and caveats. |
| `README.md` | This file. |

## Deploy to GitHub Pages

1. Create a repo on the `shijunneo-bot` account named **`ct-inbox-gallery`**.
2. Put every file from this bundle in the repo root of `main` (not in a subfolder). `index.html` must sit at the root so the site serves at the gallery URL.
3. Settings, then Pages, then deploy from `main` and the `/ (root)` folder.
4. Wait for the build, then open `https://shijunneo-bot.github.io/ct-inbox-gallery/`.
5. Optional: submit the sitemap in Google Search Console for faster indexing.

The 13-pill family band already marks this gallery as current, and the favicon is byte-identical to `amp-email-gallery`, so it slots into the network cleanly.

## Grounded vs illustrative

- **Facts** (templates, TTL, callbacks, CTAs, media limits, stats formulas, Web Inbox setup, and the push App-Inbox-Delivery and Post Action Webhook switches) are grounded in CleverTap docs, the inbox build module, and dashboard screenshots.
- **All numbers** in the use-case cards are labeled *illustrative*, and every brand is fictional.

## Verify with a CleverTap PM before quoting a client

- **Plan / packaging**: which plan tier includes App Inbox and Web Inbox. This changes over time.
- **Custom key-value inbox SDK gate**: shared key-value across messages is 5.2.0+; confirm the exact build for the hybrid (Lane 2) path.
- **API-triggered App Inbox**: a standalone App Inbox live-action does not deliver on an API event; route via a Journey. (Does not apply to Push + App Inbox.)

## Quality checks passed

- Playwright, both themes: zero console errors, zero warnings.
- 16 patterns and 90 cards render; vertical and template filters work; modal opens with focus on close, focus trap holds, Escape closes; both copy buttons work.
- WCAG AA contrast verified for all key text pairs in day and night.
- SEO: unique title, meta description, canonical, Open Graph and Twitter cards, theme-color per scheme, and JSON-LD for WebPage, FAQPage, ItemList, and BreadcrumbList.
- AEO: llms.txt, an in-page key-facts summary, clean heading hierarchy, and FAQ structured data.
