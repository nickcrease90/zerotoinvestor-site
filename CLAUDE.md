# Zero to Investor - Landing Page

## What this is
The zerotoinvestor.co.uk site for Nick, a UK personal-finance creator. Pages:
- `/waitlist/` (`waitlist/index.html`): the waitlist for the Zero to Investor
  community, which will run on Skool. It collects first name and email to prove
  demand before anything is built. Nothing is sold on the site.
- `/cheatsheet/`: the free ETF cheat sheet signup (Substack embed). Leave alone
  unless asked.
- `/` (`index.html`): redirects to `/waitlist/`.

The old Discord sales page (£19.99 lifetime) and its `thanks.html` were taken
offline in Oct 2026. They are kept, unpublished, on the `discord-page-archive`
branch so they can be reused. Don't bring them back onto `main` unless Nick
asks; anything on `main` is public.

## How it's built
- Plain static HTML, one self-contained file per page, CSS and JS inline. No
  build step.
- Brand for current pages (matches the Substack and the cheat sheet): charcoal
  #191919 background, yellow #FFD200 accent, white text, Bebas Neue (Google
  Fonts) for the wordmark and headlines, system sans for body. The stacked
  ZERO / TO / INVESTOR wordmark sits at the top of each page.
- Nick's photo on the waitlist page is a small embedded base64 JPEG.
- Waitlist form: posts first name, email and the page path to a Google Apps
  Script web app (`WAITLIST_ENDPOINT` in the page script), which writes a row to
  a Google Sheet in Nick's Workspace and sends the confirmation email from his
  address. While `WAITLIST_ENDPOINT` is empty the form refuses to submit, so no
  signups are lost. Never point it anywhere else.

## Promises the waitlist page makes (keep them true)
- £5 a month for waitlist members who join in the early access window, kept
  for as long as they stay a member; £10 a month when it opens to everyone.
  Skool bills in USD, which the page says.
- Launch contents: a short starter course, Nick answering questions, live
  Q&As, other members. Don't add launch promises Nick hasn't confirmed.
- Emails are only used for the community opening and not shared.
- No qualifications or CV-style credential lists on the page. The credibility
  line is one plain sentence about his time in the fund industry.

## Deploy
- The repo auto-deploys to Hostinger. A merge to `main` triggers a fresh deploy
  of `public_html`.
- Loop: make the edit, commit and push to main (or open a PR and merge it), and
  the live site updates within about a minute.
- Default to committing and pushing after a change unless told otherwise, so the
  change actually ships.

## Writing rules (important)
All copy must follow these. They are the difference between Nick's voice and
generic AI writing.
- No em dashes anywhere. Use commas, full stops or colons.
- No AI tells: no contrast framing ("not X, it's Y"), no rule-of-three (phrases
  or lists built in threes), no rhetorical transition questions, no glazing -ing
  verbs (highlighting, emphasising), no vague filler, no corporate or formal
  words, no grand or symbolic framing, no invented personas, no beginner
  hand-holding.
- Voice: conversational, peer-to-peer, UK English, contractions. Write like one
  experienced investor talking to another, not a brand talking to a customer.
- Frame things as frameworks and criteria, not warnings or problems.

## Positioning and copy guardrails
- ADVICE BOUNDARY, do not cross: Nick is not a financial adviser and does not
  give regulated financial advice. No page may promise advice,
  recommendations, or tell people what to buy. He helps people think through
  their own decisions and they decide. Preserve this in every edit. Pages with
  investing content keep a not-financial-advice line in the footer.

## Open items
- Set up the Google Sheet and Apps Script, then paste its web app URL into
  `WAITLIST_ENDPOINT` before the waitlist goes live.
- Nick is switching off the old £19.99 Stripe payment link himself.

## Working with Nick
- One scoped change at a time, and show what changed.
- Never open with agreement or praise, and never tell him he's right. If you
  disagree, say so and give the counter-case first.
- Before stating any current fact (platform feature, price, fund detail), verify
  it rather than asserting from memory.
