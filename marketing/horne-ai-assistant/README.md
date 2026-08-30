# AI Assistant Sales Email — Horne Heating and Air Conditioning

Design/content package only. Nothing here was sent or deployed.

## Files

- `email-horne-FINAL.html` — the finished email, ready for review in a browser (images load from `assets/` alongside it — see note below on why this isn't the file to actually send).
- `email-horne-READY-TO-SEND.eml` — the actual sendable message: a real RFC 5322 MIME file (`multipart/related` with `multipart/alternative` text/plain + text/html, and the three screenshots attached as inline `image/png` parts referenced via `cid:`). This is what makes the images work in a real inbox — see SENDING INSTRUCTIONS below.
- `email-template-REUSABLE.html` — the same email with `[COMPANY NAME]`, `[RECIPIENT]`, `[AI ASSISTANT COMPANY NAME/HEADER]`, `[SENDER EMAIL]`, `[DEMO CALENDAR LINK]`, and `[INDUSTRY-SPECIFIC QUESTION]` swapped in as placeholders, for reuse with future prospects.
- `preview-desktop.png` / `preview-mobile.png` — rendered screenshots of the Horne email at desktop and mobile widths.
- `assets/lead-capture-screenshot.png` — MOCKUP: AI Assistant collecting a quote request (not a live conversation), badged as such in the image.
- `assets/hvac-response-screenshot.png` — MOCKUP: AI Assistant answering an HVAC troubleshooting question (not a live conversation), badged as such in the image.
- `assets/customer-portal-screenshot.png` — MOCKUP: an illustrative portal design built for this email, not a live screenshot of the real product — badged as such in the image. (A real screenshot of the actual `toms-svg/customer-chatbot-portal` Overview screen was tried and is documented below for reference, but the approved version of this email uses the illustrative mockup instead.)
- `assets/src-lead-capture.html`, `assets/src-hvac-response.html`, `assets/src-portal.html` — editable source for the three mockups. Edit and re-render these to produce new screenshots for future prospects/industries.

## Customer portal screenshot — note on what was tried

A real screenshot of the actual Customer Portal was captured from `toms-svg/customer-chatbot-portal` (`main` branch, production, read-only — nothing was pushed back to it): the customer-facing "Overview" tab of the `Dashboard` component, rendered locally with fabricated safe demo props (no real customer data, no live Supabase/Stripe/Telnyx connection, no Admin Portal or Cold Caller Portal code touched). That version is not used in the current email — the illustrative mockup was kept instead per direction. If a real screenshot is wanted again later, the method is: check out `main` into a scratch git worktree, temporarily export the `Dashboard` component, point the app's entry at a small harness that renders it with hand-written demo data, screenshot with a headless browser, then discard the worktree.

## Live links wired in

- CTA button ("Schedule a Quick Demo") → `https://calendly.com/techopsmanserv/30min`
- Customer portal → `https://customer-chatbot-portal.onrender.com` (linked from the "Your Customer Portal" paragraph and under the portal screenshot)

The reusable template keeps `[DEMO CALENDAR LINK]` as a placeholder (a future prospect/rep may use a different scheduling link) but hardcodes the portal URL, since that's the same product URL for every customer.

## Sending instructions (manual, from techopsmanserv@gmail.com)

See the chat response for the simple step-by-step. In short: open `email-horne-FINAL.html` in a browser, copy the rendered page, and paste it into a new Gmail compose window (Gmail re-hosts the pasted images itself — no external hosting needed). `email-horne-READY-TO-SEND.eml` is the fallback path for a desktop mail client (Thunderbird/Apple Mail/Outlook) if paste ever drops formatting.

## Outstanding before sending

- Confirm the "No long-term contract" pricing claim against current business policy before this or any future version goes out.
