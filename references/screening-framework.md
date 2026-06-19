# Screening Framework: The Five Screens

This file explains each screen in enough depth to reason carefully rather than mechanically. The goal is genuine fiqh-grounded judgment, not a checklist. Read it before writing the analysis section of a report.

Islamic commercial law begins from a default of permissibility (*ibāḥah al-aṣliyyah*): a thing is allowed unless something specific renders it forbidden. So screening is really a search for disqualifiers. The five screens below are the disqualifiers (and one qualifier — valid property) that the mainstream of Islamic-finance scholarship applies to crypto.

---

## Screen 1 — Māl mutaqawwim (valid, ownable property)

**The question:** Is the token something Shariah recognizes as property that can be lawfully owned and exchanged?

**The test:** Classical fiqh treats something as *māl mutaqawwim* (valued property) when it is (a) capable of ownership, (b) capable of storage/possession, and (c) possesses recognized commercial value (*taqawwum*). A standard fungible token on an established chain generally satisfies all three: it can be held in a wallet, transferred, and has a market price.

**How it tends to resolve:** This is the one screen most real tokens *pass*. Several authorities (e.g. Malaysia's Shariah Advisory Council) reached permissibility precisely by classifying major cryptocurrencies as tradeable digital commodities (*'urūḍ*) rather than as currencies. A small prohibitive minority argues crypto fails even this screen — no intrinsic value, no issuing authority — but the more common position is that market-recognized value is sufficient for *taqawwum*.

**When it actually fails:** purely fictitious "tokens" with no real existence, or assets whose only function is to represent something already prohibited (e.g. a token that is a claim on a haram revenue stream).

---

## Screen 2 — Riba (interest)

**The question:** Does acquiring, holding, or earning on the token involve interest — a guaranteed return on money lent, or an unequal/deferred exchange of like-for-like monetary value?

**The test:** Riba comes in two classical forms — *riba al-nasī'ah* (interest on a loan / deferred exchange) and *riba al-faḍl* (unequal exchange of the same commodity). For tokens, the live risks are: staking or "savings" products that pay a fixed/guaranteed yield; lending protocols; stablecoins backed by interest-bearing reserves (the holder is indirectly earning on riba-based instruments); and margin/leverage, which is borrowing at interest.

**How it tends to resolve:** Simple spot purchase and holding usually *passes* — there is no lender/borrower relationship. The screen bites when the token's design or the user's intended use layers on yield, lending, or leverage. Ask specifically how the user plans to use it, not just what the token is.

**Key nuance:** rewards are not automatically riba. A reward for *doing work* (validating, providing a genuine service, or a profit-share from real activity) can be permissible; a *guaranteed return purely for parking capital* looks like riba. The distinction is whether the return is tied to genuine risk-bearing activity or is a fixed charge for the use of money.

---

## Screen 3 — Gharar (excessive uncertainty)

**The question:** Is the transaction afflicted by *excessive, structural* uncertainty — as opposed to the ordinary, acceptable risk of commerce?

**The test — and the most-misunderstood point in the whole framework:** Gharar is **not** "the price might go down." Normal commercial risk — not knowing whether a business will succeed — is fully acceptable in Islam; risk-bearing is how profit is legitimately earned. Gharar refers to uncertainty so fundamental to the *transaction itself* that it becomes inherently unfair: undefined subject matter, unknowable terms, hidden information, inability to assess what you're actually getting. Related defects scholars name alongside it are *jahalah* (ignorance about the asset) and *tadlīs* (concealment/deception).

**Apply it to tokens like this:**
- **Anonymous team, no audits, undisclosed treasury/governance** → information you *cannot obtain* about an asset you're buying. That is structural gharar, not market risk.
- **Brand-new token (days/weeks old)** → no track record to assess; the uncertainty is about the fundamental nature of the thing.
- **Opaque or manipulable tokenomics** (hidden mint authority, concealed insider unlocks) → you cannot know what you're really holding.
- **Documented scam clones / impersonation** → raises the odds the "thing" itself is not what it appears.

**How it tends to resolve:** Established, audited, transparent projects can pass. Anonymous, unaudited, opaque, or freshly-launched tokens tend to *fail* or score *weak* — and this is one of the two screens that most often sink speculative tokens.

---

## Screen 4 — Maysir (gambling / pure speculation)

**The question:** Does engaging with the token function like gambling — gains arising from chance and momentum rather than from genuine value or productive activity?

**The test:** *Maysir* (gambling) is explicitly prohibited. The essence scholars identify is a zero-sum wager on an uncertain outcome where one party's gain is the other's loss and the result turns on chance/sentiment rather than real economic merit. The widely-cited modern framing: when an asset's value is driven by short-term hype and emotional reaction rather than legitimate economic merit, the *activity* shares the essential structure of maysir — whether it happens on a blockchain or at a casino table.

**Signals that push a token toward maysir:**
- Value driven by social-media hype, FOMO, and viral culture rather than utility or cash flow.
- Extreme volatility on thin liquidity; pump-and-dump dynamics; susceptibility to manipulation.
- Launch and trading venues built around momentum speculation (e.g. bonding-curve meme launchpads).
- A structure where returns depend on later entrants buying in higher (a greater-fool / payout-pool shape).
- The user's own intent: day-trading purely on price momentum is closer to maysir than buying a productive asset to hold.

**How it tends to resolve:** This is the decisive screen for memecoins and most low-utility speculative tokens, where the dominant scholarly view is that they are *highly problematic*. Tokens with genuine, sustained utility and value tied to real activity can pass; pure hype vehicles generally *fail*.

**Important distinction:** maysir is about the *value mechanism and intent*, not the theme. A token attached to an innocent product can still fail maysir if its actual market behavior is pure speculation — and conversely, the presence of a real product is not by itself enough to clear maysir if the token economy is hype-driven.

---

## Screen 5 — Underlying utility and activity (manfa'ah + the haram-business screen)

**The question:** Two parts. (a) Does the token serve a genuine economic purpose (*manfa'ah*)? (b) Is the underlying project/business itself lawful?

**The test:**
- **Utility:** Many scholars require real, *sustainable* utility — a function or value source beyond "people will buy it because others are buying it." Weigh whether the utility is genuine and durable, or cosmetic cover for a speculative instrument. A real product that nonetheless depends entirely on continuous new-user inflow to sustain token value is weak on this screen.
- **Underlying activity:** Even a structurally clean token is impermissible if it funds or represents a prohibited activity — gambling/casino platforms, alcohol, pork, conventional interest-based finance, adult content, and similar. Screen the *business*, not just the coin.

**How it tends to resolve:** A token attached to a halal product with genuine utility *strengthens* the overall case (and can move a borderline token from "avoid" toward "conditionally acceptable"). A token whose underlying activity is itself haram *fails outright*, regardless of how clean its technical structure looks. A token with no real utility leans on the maysir screen to do the disqualifying.

---

## Weighing the screens together

Don't average the screens mechanically — weight them by what's load-bearing for the token in front of you:
- **Speculative / memecoins:** maysir and gharar dominate.
- **Yield / DeFi / staking / stablecoins:** riba dominates.
- **GameFi / P2E:** maysir (and sometimes the gambling-mechanics version of the underlying-activity screen) dominate.
- **Anything attached to a prohibited business:** the underlying-activity screen is dispositive on its own.

A token can pass māl and riba cleanly and still be assessed non-compliant because it fails maysir and gharar — that combination is exactly the profile of most speculative micro-cap tokens. Make the weighting explicit in the report so the user understands *why* a particular screen decided the outcome.
