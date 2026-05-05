# gazdigi* — Pre-Launch Checklist

Track each item before going live. Check the box when done.

---

## SEO

- [ ] **Confirm production domain** — canonical and all OG/Twitter image URLs currently use `https://gazdigi.com/`. Verify this is the actual live domain before deploying.
- [ ] **Create a dedicated OG image** — `hero.jpg` is portrait-oriented and will crop badly in social link previews. Create a landscape 1200 × 630 px image and update the `og:image` / `twitter:image` tags in `<head>`.
- [ ] **Verify `foundingDate`** — JSON-LD structured data has `"foundingDate": "2016"`. Correct if needed.
- [ ] **Confirm Twitter/X handle** — `@gazdigi` is set in `twitter:site` and `twitter:creator`. Verify this handle exists and is active.
- [ ] **Add `sitemap.xml`** — create and upload to root. Submit to Google Search Console after launch.
- [ ] **Add `robots.txt`** — create with `Sitemap:` directive pointing to `sitemap.xml`.
- [ ] **Set up Google Search Console** — verify ownership and submit sitemap.
- [ ] **Set up Google Business Profile** — claim/create listing for Miami, FL to boost local SEO.
- [ ] **Add favicon** — no favicon is set. Add `favicon.ico`, a 32×32 PNG, and an `apple-touch-icon` (180×180 PNG). Link them in `<head>`. *(in progress on this branch)*

---

## Content & Links

- [ ] **Fix Instagram link** — contact section has `href="#"` for `@gazdigi`. Replace with `https://www.instagram.com/gazdigi`.
- [ ] **Replace screenshot filenames in Work section** — `Screenshot 2026-04-15 at 5.44.58 PM.png` etc. are being served publicly. Rename to clean slugs (e.g. `studio-setup-full-cart.jpg`) and update `src` attributes.
- [ ] **Fill the "Coming Soon" work slot** — placeholder image in the work strip needs a real photo before launch.
- [ ] **Verify `hero.jpg` aspect ratio for OG** — if reusing hero.jpg as OG image, confirm its dimensions and crop to 1200 × 630.

---

## Analytics & Tracking

- [ ] **Add Google Analytics 4 (GA4)** — no analytics tag is present. Add GA4 snippet to `<head>`.
- [ ] **Add Hotjar or Microsoft Clarity** *(optional)* — session recording to understand how visitors interact with the page.

---

## Technical / Hosting

- [ ] **Confirm HTTPS/SSL** — make sure the host has a valid SSL cert so `https://gazdigi.com` resolves correctly.
- [ ] **Test on production domain** — verify canonical tag resolves, no mixed-content warnings, all images load.
- [ ] **Run Lighthouse audit** — target 90+ on Performance, Accessibility, Best Practices, SEO. Fix any flagged issues.
- [ ] **Validate structured data** — paste `index.html` into [Google's Rich Results Test](https://search.google.com/test/rich-results). Fix any errors.
- [ ] **Test Open Graph preview** — use the [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) and [Twitter Card Validator](https://cards-dev.twitter.com/validator) to confirm link previews render correctly.
- [ ] **Check image file sizes** — `hero.jpg` and work photos should be compressed and served as WebP where possible. Target under 200 KB per image.
- [ ] **Set cache headers** — configure host to send long `Cache-Control` headers for images and fonts.

---

## Accessibility

- [ ] **Audit alt text** — all images in the work strip have alt text; confirm they are descriptive enough for screen readers.
- [ ] **Check color contrast** — `--fg3` on `--bg` (light gray on light cream) may fail WCAG AA. Verify with a contrast checker.
- [ ] **Keyboard navigation** — test Tab through nav, hero CTAs, and contact links.

---

## Pre-Launch Final Checks

- [ ] **Proofread all copy** — hero sub, about body, service descriptions, contact availability line.
- [ ] **Test on mobile (real device)** — iPhone and Android, both portrait and landscape.
- [ ] **Test in Safari, Chrome, Firefox** — verify animations, fonts, and layout render correctly.
- [ ] **Remove or redirect any test/dev URLs** — ensure no `localhost` references remain in production.
