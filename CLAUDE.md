# Zero to Investor - Landing Page

## What this is
A single-page sales/landing page for Zero to Investor, a paid Discord community
run by Nick, a UK personal-finance creator (dividend and retirement focus). It
sells lifetime access to the community for a one-off £19.99 via Stripe. The
page's only job is to convert visitors into paying members.

## How it's built
- One self-contained file: `index.html`. All CSS and JS are inline, and Nick's
  photo is embedded as a base64 data URI, so the page renders with no other
  assets.
- `thanks.html` is the page shown after payment.
- Fonts: Switzer for headings (loaded from Fontshare), Inter for body (loaded
  from Google Fonts). Both are free for commercial use. Do not reintroduce
  Fraunces or any serif.
- Dark "quiet wealth" theme. Use the existing CSS variables, do not hardcode new
  colours:
  - Backgrounds: --ink #0E0E11, --ink-2 #121217, --surface #17171D, --surface-2 #1D1D25
  - Text: --paper #ECEAE2, --paper-2 #B6B3A9, --paper-3 #8C8A81
  - Accent: --brass #C8A45C, --brass-bright #E2C588, --brass-deep #A8863F
- Stripe payment link, used in every join button:
  https://buy.stripe.com/9B6eVef66aAvdCzcp30Fi00

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
- The page niches to a PROBLEM, not a person: helping people make portfolio
  decisions and giving them somewhere to get a second opinion. Keep that framing.
- Differentiators, in rough priority: direct access to Nick, a private community
  of like-minded UK investors, lifetime one-off access with all future resources
  included, an organised library of education videos, budgeting spreadsheets.
- ADVICE BOUNDARY, do not cross: Nick is not a financial adviser and does not
  give regulated financial advice. The page must never promise advice,
  recommendations, or tell people what to buy. He helps people think through
  their own decisions and they decide. Preserve this in every edit. The footer
  disclaimer (not financial advice, not a financial adviser) stays.

## Open items (not yet resolved)
- Domain: the page uses zerotoinvestor.co.uk in the canonical tag and footer
  email. An earlier brief said zeroinvestor.co.uk (no "to"). Confirm which Nick
  actually owns at IONOS before launch and make them match.
- thanks.html: needs a decision on how the Discord invite reaches a buyer after
  payment (a public invite link on the page is a security risk). Likely route is
  Stripe to an email via Zapier, with the thanks page saying "check your email".
- Stripe: the product still reads "Investing Hub" and needs renaming to Zero to
  Investor.

## Working with Nick
- One scoped change at a time, and show what changed.
- Never open with agreement or praise, and never tell him he's right. If you
  disagree, say so and give the counter-case first.
- Before stating any current fact (platform feature, price, fund detail), verify
  it rather than asserting from memory.
