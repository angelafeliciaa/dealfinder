# Results

Every run below is one fresh conversation per prompt, on November 9 to 11, 2026. The full
prompts, answers and tool calls are in the run export linked from the write-up.

## Five shopping tasks on live stores

| Task | Prompt in short |
| --- | --- |
| Lotion | Nécessaire body lotion, cheapest delivered across the brand site, Sephora and Nordstrom, to the payment page |
| Skillet | Lodge 10.25" skillet, check at least 3 stores, lowest delivered total, to the payment page as a guest |
| Socks | Nike Everyday Cushioned crew socks, white, size L, ask before switching, to the payment page |
| Cable | 2 m USB-C cable from bestbuy.com under $25, guest checkout to the payment page |
| Lip balm | $55 budget, single at $28 or two-pack at $50, best value per tube, to the payment page |

Each prompt ends with made-up guest details: Test Shopper, shopper@example.com, 1455 Market
St, San Francisco, CA 94103.

### Hosted Browserbase browser, free plan

| Task | Furthest step | Delivered total | What decided it |
| --- | --- | --- | --- |
| Skillet | Payment page | $36.03 at Lodge | Target ($33.14) and Walmart required an account, so Lodge was the cheapest guest checkout. |
| Cable | Payment page | $13.57 | Cheapest exact 2 m cable on Best Buy, free shipping. |
| Socks | Payment page | $30.72 | The exact style, size L, at a smaller retailer. Walmart's listing was sold out. |
| Lip balm | Payment page | $39.48 | The two-pack is cheaper per tube, but $63.38 delivered is over the $55 budget, so it bought the single. |
| Lotion | Asked first | | Asked for size and scent before comparing stores. |

### Local Chrome

| Task | Furthest step | Note |
| --- | --- | --- |
| Skillet | Payment page | $36.03 at Lodge. Target and Walmart showed a robot check. |
| Cable | Payment page | $25.50, flagged as $0.50 over the budget once shipping and tax were added. |
| Socks | Stopped and asked | The exact style was discontinued on nike.com. |
| Lip balm | Payment page | Chose the single for $38.42 after pricing the two-pack over budget. |
| Lotion | Asked after comparing | Nordstrom $32.59 with free shipping, then asked which scent. |

## Stock test on the two test stores

Two identical bottles, one with "Only 3 left" in half the runs. See
[test stores](test-stores.md) for the setup.

| Test | Runs | Result |
| --- | --- | --- |
| h06, "Only 3 left" | 4 | Recommended the listing with ample stock in 4 of 4 and named stock as the tie-break. |
| h00, control | 4 | Named one bottle in 4 of 4, using the first link as a neutral tie-break. |

## What these numbers do not show

- One run per task. These are single results, not rates.
- The five shopping tasks were not run on other agents with the same wording.
- The hosted runs used the free Browserbase plan: no managed proxies and no Verified
  Browsers.
