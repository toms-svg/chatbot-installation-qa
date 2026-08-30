# AI Assistant Sales Email — Horne Heating and Air Conditioning

Design/content package only. Nothing here was sent or deployed.

## Files

- `email-horne-FINAL.html` — the finished email for Horne Heating and Air Conditioning, ready for review. Open directly in a browser to see it exactly as a recipient would (images load from `assets/` alongside it).
- `email-template-REUSABLE.html` — the same email with `[COMPANY NAME]`, `[RECIPIENT]`, `[AI ASSISTANT COMPANY NAME/HEADER]`, `[SENDER EMAIL]`, `[DEMO CALENDAR LINK]`, and `[INDUSTRY-SPECIFIC QUESTION]` swapped in as placeholders, for reuse with future prospects.
- `preview-desktop.png` / `preview-mobile.png` — rendered screenshots of the Horne email at desktop and mobile widths.
- `assets/lead-capture-screenshot.png` — mockup: AI Assistant collecting a quote request (not a live conversation).
- `assets/hvac-response-screenshot.png` — mockup: AI Assistant answering an HVAC troubleshooting question (not a live conversation).
- `assets/customer-portal-screenshot.png` — mockup of the customer portal AI Assistant overview screen. This repository does not contain the actual approved portal UI, so this is an illustrative mockup, not a real product screenshot — labeled as such in the image itself.
- `assets/src-*.html` — editable source for the three mockups (used to render the PNGs via a headless browser). Edit and re-render these to produce new screenshots for future prospects/industries.

## Before sending (not done here)

- Replace the local `assets/...png` image paths in the HTML with hosted HTTPS URLs, or attach the images as inline CID attachments — most inboxes cannot resolve local/relative file paths, and inlining them as base64 would push the message over Gmail's clipping threshold.
- Replace `[DEMO CALENDAR LINK]` with a real scheduling link.
- Confirm the "No long-term contract" pricing claim against current business policy before this or any future version goes out.
