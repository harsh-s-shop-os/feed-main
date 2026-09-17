# Changelog

Human-readable log of what changed in the onboarding prototype, for product review. Updated at each local commit — most recent first.

## 2026-09-18 — Brand Memory: discard on edits, no scrolling, fewer and clearer cards

**Discard, not just save**
Editing a card now shows a check and a cross, not just a check. Check keeps what you typed; the cross puts the card back exactly as it was — text and any tags you removed while editing.

**Toned down the edit chrome**
No background box behind the text you're editing, and no background on the check/cross buttons — just the icons, so editing doesn't call more attention to itself than the card's content does.

**Tag crosses only take up space while the card is being edited**
A tag pill used to reserve room for its remove-cross at all times (revealed on hover). Now the cross has zero width until the card enters editing state, then the pill opens up to show it. No dead space on cards you're not touching.

**Dropped the fixed-height, scrolling cards**
Cards were pinned to one height with an internal scrollbar; nothing in them was ever long enough to need it. Cards now size to their own content — short cards are short, longer ones are taller.

**Fewer cards, clearer purpose**
Cut Pricing, Channels, Drops and collections, standalone Business landscape, Growth direction, and the "Still missing" card. Merged the two Product information cards into one. Company now carries a bit more of what Business landscape used to say, since that's where it belongs. Catalog is now "Product catalog" and says plainly what's being pulled together. Audience keeps its text, loses its (repetitive) tags. Competitors keeps its tags, loses its description — just the names. Voice and tone moved up next to the new "Brand guidelines" card (the old untitled Brand Kit card now has a name). Nine cards total, down from fifteen.

**New: a Shopify connect row**
Reuses the exact connector-row shape from the Signals column — logo, name, one line, a white Connect button — with copy written for this moment ("Connect Shopify for detailed product analytics."). It's the one card in the column that isn't a finding, so it carries no edit icon; clicking Connect gives it its own short, self-contained "Connecting → Connected" state.


## 2026-09-18 — Brand Memory: editable, scrollable cards during loading

**The first column of the loading state ("Brand Memory") is now editable**
Each card is a fixed height and scrolls inside itself if the copy runs long, so editing one card never pushes the others down the column. A pencil icon in the top-right corner opens editing — click it and the card's description becomes an input; click the checkmark (or press Enter) to save, or press Escape to cancel. A soft fade at the bottom of a card is the cue that there's more to scroll to.

**New: generic, reusable card titles**
Card titles are no longer one-off headlines specific to a single demo brand (e.g. "The Flex henley is leading the brand right now"). They're now a fixed set of category labels — "About the brand," "Product information," "Business landscape," "Growth direction" — that make sense for any brand ShopOS reads. The label stays put; only the finding underneath it (what was actually read off the store) is what gets edited.

**Only text cards are editable**
The Brand Kit card (logo, colors, typeface swatches) carries no edit icon — it isn't a text finding, so there's nothing to type into.

**Confirmed: this column only ever appears during loading**
It's built fresh each time onboarding runs and is never carried into the finished feed — nothing else needed to change here, but flagging it since it came up as a question this session.

## 2026-09-17 — Onboarding flow: two new paths, a product-first wizard, and polish

**New: two more ways to start, right on the first screen**
Below the "Enter your store URL" field, there are now two extra options: **"See ShopOS in action"** and **"I don't have a Brand"**. Typing a real URL into the field automatically hides these two options (typing anything else does not); the field also silently blocks characters that can't appear in a URL as you type.

**New: "See ShopOS in action" → pick a demo brand**
Clicking it opens a brand-picker screen with 7 sample brands (Dunder Mifflin, Los Pollos Hermanos, Chocolate Frogs, Fishwife, Miu Miu, Vacation Inc., Dorsey). Picking one and continuing runs the same setup/loading experience as a real store. Only the parts of the screen that actually change (the subtitle, the body, the button label) animate — the logo and headline never move.

**New: "I don't have a Brand" → a 3-question wizard**
Instead of jumping straight to setup with no information, this now asks three quick questions, one at a time: what's your product, who's your audience, what should we call your Brand. Answering one reveals the next; each answered question collapses to show just the answer with a pencil icon to go back and edit it. Editing an earlier answer discards whichever questions came after it, so the flow always makes sense. The brand name you type here now also shows up in the "URL" field on the loading screen, instead of a generic placeholder.

**Fixes and polish**
- The "Build My Team" button on the first screen always shows in its active white state — it no longer greys out when the input is empty.
- Clicking anywhere inside a text field (not just precisely on the text) now focuses it.
- The "Try your own Brand" button on the brand-picker screen is no longer stretched to match the width of the button next to it — it sizes to its own label.
- Fixed a background color mismatch (was pure black, should be the site's standard near-black) on both the URL screen and the brand-picker screen.
- Fixed a couple of small spacing/alignment misses in the new 3-question wizard so its icons and text line up with the rest of the screen.
- Set up version control for this prototype so changes can be tracked going forward.
