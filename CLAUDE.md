# Zero to Investor - Landing Page

## What this is
The zerotoinvestor.co.uk site for Nick, a UK personal-finance creator. Pages:
- `/` (`index.html`): a simple holding page (wordmark, a line saying something
  is in the works, cheat sheet and YouTube links) until the community waitlist
  goes live.
- `/cheatsheet/`: the free ETF cheat sheet signup (Substack embed). Leave alone
  unless asked.

The old Discord sales page (£19.99 lifetime) and its `thanks.html` were taken
offline in Oct 2026. They are kept, unpublished, on the `discord-page-archive`
branch so they can be reused. Don't bring them back onto `main` unless Nick
asks; anything on `main` is public.

## How it's built
- Plain static HTML, one self-contained file per page, CSS and JS inline. No
  build step.
- Brand for current pages (matches the Substack and the cheat sheet): charcoal
  #191919 background, yellow #FFD200 accent, white text, Bebas Neue (Google
  Fonts) for the wordmark and headlines, system sans for body.

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
  investing content keep a not-financial-advice line in the footer; the
  holding page has none, by Nick's choice.

## Open items
- The community waitlist page is built on the `waitlist-page` branch and waits
  on its Google Sheet connection before it's merged.

## Working with Nick
- One scoped change at a time, and show what changed.
- Never open with agreement or praise, and never tell him he's right. If you
  disagree, say so and give the counter-case first.
- Before stating any current fact (platform feature, price, fund detail), verify
  it rather than asserting from memory.
