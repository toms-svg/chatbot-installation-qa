# AI Assistant Sales Email — Horne Heating and Air Conditioning

Design/content package only. Nothing here was sent or deployed.

## Files

- `email-horne-FINAL.html` — the finished email, ready for review in a browser (images load from `assets/` alongside it — see note below on why this isn't the file to actually send).
- `email-horne-READY-TO-SEND.eml` — the actual sendable message: a real RFC 5322 MIME file (`multipart/related` with `multipart/alternative` text/plain + text/html, and the three screenshots attached as inline `image/png` parts referenced via `cid:`). This is what makes the images work in a real inbox — see SENDING INSTRUCTIONS below.
- `email-template-REUSABLE.html` — the same email with `[COMPANY NAME]`, `[RECIPIENT]`, `[AI ASSISTANT COMPANY NAME/HEADER]`, `[SENDER EMAIL]`, `[DEMO CALENDAR LINK]`, and `[INDUSTRY-SPECIFIC QUESTION]` swapped in as placeholders, for reuse with future prospects.
- `preview-desktop.png` / `preview-mobile.png` — rendered screenshots of the Horne email at desktop and mobile widths.
- `assets/lead-capture-screenshot.png` — MOCKUP: AI Assistant collecting a quote request (not a live conversation), badged as such in the image.
- `assets/hvac-response-screenshot.png` — MOCKUP: AI Assistant answering an HVAC troubleshooting question (not a live conversation), badged as such in the image.
- `assets/customer-portal-screenshot.png` — REAL PRODUCT SCREENSHOT (not a mockup). Captured by rendering the actual `Dashboard` "Overview" component from `toms-svg/customer-chatbot-portal` (production `main` branch, the merged Claude V2 frontend rebuild) with fabricated, safe demo props — no real customer data, no live Supabase/Stripe/Telnyx connection was used. Company name shown is a generic placeholder ("Sample Home Services Co."), not Horne's real account. See CUSTOMER PORTAL SCREENSHOT PROVENANCE below.
- `assets/src-lead-capture.html`, `assets/src-hvac-response.html` — editable source for the two chat mockups. Edit and re-render these to produce new screenshots for future prospects/industries.
- `assets/src-portal.html` — superseded. This was an earlier illustrative portal mockup, kept only for history; it is no longer referenced by any email (replaced by the real product screenshot above).

## Customer portal screenshot provenance

- Source repo: `toms-svg/customer-chatbot-portal`, `main` branch (production, read-only — nothing was pushed back to it).
- Screen shown: the customer-facing "Overview" tab of the Customer Portal (`Dashboard` component, `activeView === 'overview'`) — chosen because it's the single screen that best shows a prospective buyer what they'd get: account metrics, recent conversations, recent leads.
- Method: checked out `main` into a scratch git worktree (outside this repo, discarded after the screenshot), temporarily exported the `Dashboard` component and pointed the app's entry point at a small harness rendering it with hand-written demo data — no `.env` secrets, no real Supabase project, no network calls. The worktree was deleted afterward; no commits were made to `customer-chatbot-portal`.
- Excluded by construction: Admin Portal, Cold Caller Portal, Telnyx, Stripe, API keys/credentials, and debug information — none of those code paths were touched or rendered.

## Live links wired in

- CTA button ("Schedule a Quick Demo") → `https://calendly.com/techopsmanserv/30min`
- Customer portal → `https://customer-chatbot-portal.onrender.com` (linked from the "Your Customer Portal" paragraph and under the portal screenshot)

The reusable template keeps `[DEMO CALENDAR LINK]` as a placeholder (a future prospect/rep may use a different scheduling link) but hardcodes the portal URL, since that's the same product URL for every customer.

## Sending instructions (manual, from techopsmanserv@gmail.com)

See the chat response for the simple step-by-step. In short: open `email-horne-FINAL.html` in a browser, copy the rendered page, and paste it into a new Gmail compose window (Gmail re-hosts the pasted images itself — no external hosting needed). `email-horne-READY-TO-SEND.eml` is the fallback path for a desktop mail client (Thunderbird/Apple Mail/Outlook) if paste ever drops formatting.

## Outstanding before sending

- Confirm the "No long-term contract" pricing claim against current business policy before this or any future version goes out.
