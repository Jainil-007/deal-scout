# Deal Scout Daily

New businesses for sale, priced against their cash flow.

A single-page site that lists businesses for sale from BizBuySell and ranks each one
by its asking price as a multiple of cash flow (SDE). Filter by state, by how recently
a listing appeared, by deal quality (2–4× cash flow with $150K+ cash flow, and other
presets), by price and by keyword.

Open it here: https://jainil-007.github.io/deal-scout/

## Files

- `index.html` — the whole interface
- `art.js` — the drawn scene used for each type of business
- `data.json` — the listings

## Updating

Replace `data.json` and push. The page reads it on load. Each listing is:

```json
{ "id": "", "title": "", "location": "City, ST", "price": 0, "cashFlow": 0,
  "revenue": 0, "summary": "", "seenAt": 0, "dated": true }
```

`dated: true` means the listing came from the "recently listed" feed on the day given
by `seenAt`, so it counts towards Today / 2 / 4 / 7 / 30 days. `dated: false` means it
was already on the market and its posting date isn't known; it shows under "Anytime".

Figures are the seller's or broker's claims. Deal Scout isn't affiliated with BizBuySell.
