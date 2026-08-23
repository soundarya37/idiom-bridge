Idiom Bridge

A single-file browser toy that pairs Tamil and Hindi idioms with Spanish idioms that carry the same underlying meaning, expressed through completely different imagery.

Description

Idiom Bridge sits alongside Rasam vs. Salsa as a lighter, language-focused entry in the same cross-cultural mapping series. Where Rasam vs. Salsa connects flavors, Idiom Bridge connects expressions: a Tamil line about a frog in a well next to a Spanish line about not seeing past one's own nose, both meaning the same thing — a narrow, inexperienced view of the world.

The app has two modes:

Browse — click any card to reveal its literal translation, idiomatic meaning, and a category tag.
Guess the match — the Spanish column shuffles, and you pair each Tamil/Hindi idiom with its Spanish counterpart. Correct pairs draw a soft connecting line across the board; incorrect guesses shake gently and let you try again.

13 idiom pairs are seeded by hand rather than scraped, organized around plain-language tags like "impossible task," "fixed nature," and "wasted worth" so the throughline between pairs is legible at a glance.

Visual language
Palette — Ink & Clay: bone-paper background (
#F4F1EA), near-black ink for the Tamil/Hindi side (
#2B2E2B), muted terracotta for the Spanish side (
#8C6A56), soft sage for connector lines (
#5C6B5C), warm gray for meta text (
#7A776E)
Type — Fraunces (serif, idiom headlines), IBM Plex Mono (transliteration, tags, UI labels), Inter (body copy)
No build step — vanilla HTML/CSS/JS in a single file, no dependencies
Installation

No installation needed. Download idiom-bridge.html and open it in any modern browser.

bash
open idiom-bridge.html
Usage
Open the file in a browser.
Start in Browse mode to read through all 13 pairs at your own pace — click a card to flip open its meaning.
Switch to Guess the match to shuffle the Spanish column and test yourself. Click a Tamil/Hindi card, then click the Spanish card you think matches it.
A running score in the top right tracks matched pairs; a toast at the bottom confirms each correct match and shows the shared tag.
Extending the seed data

Idioms live in a single IDIOMS array near the top of the <script> tag. Each entry follows this shape:

js
{
  id: 14,
  native: { lang: "Tamil", script: "...", translit: "..." },
  spanish: { text: "..." },
  literal: { native: "...", spanish: "..." },
  meaning: "...",
  tag: "..."
}

Add a new object to the array and it appears automatically in both modes — no other code changes needed.

Accessibility
All cards are keyboard-focusable and respond to Enter/Space
Visible focus rings on interactive elements
prefers-reduced-motion disables the shake and toast transitions
Connector lines are decorative and hidden on narrow viewports, where the layout stacks to a single column
Roadmap
Add audio pronunciation for transliterations
Allow filtering by tag
Add a third language column (regional Mexican Spanish vs. Castilian variants, or a third home language)
Authors and acknowledgment

Seeded from idioms actually used in conversation, not pulled from generic "top idioms" lists — in keeping with the same approach as Rasam vs. Salsa.

License

For personal use.
