---
name: shariah-token-checker
description: Screen any cryptocurrency token or coin for Shariah (Islamic law) compliance through deep web research. Use this whenever the user asks whether a token, coin, memecoin, NFT, or crypto asset is halal, haram, shariah-compliant, Islamically permissible, or "okay for a Muslim to buy/hold/trade" — including when they paste a contract address and ticker and ask for analysis, or ask to compare the Islamic permissibility of several tokens. Performs structured screening (māl, riba, gharar, maysir, and underlying utility) backed by live research into what the token actually is, and returns a comprehensive, scholar-calibrated report. Trigger on any halal/haram crypto question even if the user never says the word "skill" or "shariah" explicitly (e.g. "can I invest in this coin as a Muslim?").
---

# Shariah Token Compliance Checker

This skill turns a token name or contract address into a thorough, honest assessment of whether the asset is likely to be considered permissible (halal) under Islamic commercial law. The output is a structured research report, not a one-word verdict.

## The single most important framing rule

You are not a mufti and this report is not a fatwa. Crypto has **no scholarly consensus** — qualified scholars genuinely disagree, and the same token can be ruled differently by different authorities. Your job is to (1) apply the established Islamic-finance screening framework rigorously, (2) ground every judgment in what the token *actually is* rather than its marketing, and (3) present the verdict as a calibrated reading across the spectrum of scholarly opinion, always pointing the user toward a qualified scholar for a binding ruling.

Never deliver a flat "this is halal" / "this is haram." Deliver "here is how it scores on each screen, here is where the major scholarly camps would likely land, and here is what would change the answer." This humility is not hedging — it reflects the actual state of the field, and overconfidence here can mislead someone on a matter of conscience.

## How to use this skill

Work through four phases in order. Phases 1–2 are **research-heavy** — you cannot screen a token you don't understand, and tokens lie in their marketing. Phases 3–4 are **analysis**. Scale your research depth to the request: a quick gut-check might be 3–5 searches; a request for "deep research / comprehensive" warrants 8–20+ searches across the token's identity, fundamentals, market behavior, and the relevant fiqh.

Read the three reference files as you need them:
- `references/screening-framework.md` — the five screens explained in depth, with the fiqh concepts and how to weigh them. Read this before writing the analysis.
- `references/token-categories.md` — how the screens apply differently to memecoins, P2E/GameFi, payment coins, DeFi/yield tokens, stablecoins, asset-backed/RWA tokens, governance and NFT-linked tokens, plus the red flags specific to each. Read the relevant section once you've categorized the token.
- `references/scholarly-positions.md` — the three scholarly camps, the named scholars and fatwa bodies, and how to phrase a calibrated conclusion. Read this before writing the verdict.

### Phase 1 — Identify and verify the token

Pin down exactly what you're screening before anything else. Search for:
- Full name, ticker, chain, and **contract address** — confirm the address the user gave matches the real project. Scam clones and impersonation sites are common; if you find a documented fake, flag it as a security red flag in its own right.
- Launch venue and mechanism: pump.fun / bonding-curve, fair launch, presale/ICO, pre-mine, airdrop. The launch mechanism is itself evidence about the speculation profile (a pump.fun bonding-curve launch signals a momentum-trading design; a pre-mine with a large insider allocation signals concentration risk).
- Age. A token weeks old has, by definition, no track record, which directly raises the uncertainty (gharar) screen.

### Phase 2 — Establish what the token actually is

This is where most of the real work lives. Research and write down:
- **Category** (memecoin, P2E/GameFi, payment, utility, governance, DeFi/yield, stablecoin, asset-backed/RWA, NFT-linked, or hybrid). This determines which screens bite hardest — see `token-categories.md`.
- **Genuine utility vs. marketing.** Is there a real product, real cash flows, real on-chain function — or is value driven purely by hype and social sentiment? Distinguish "the marketing says X" from "X is verifiably true."
- **Tokenomics:** total/circulating supply, distribution and insider concentration, emissions/inflation, and token sinks (what actually removes tokens from circulation).
- **Transparency:** is the team public? Are there audits? Is treasury/governance disclosed?
- **Market behavior:** volatility, 24h/7d volume, liquidity depth, holder count and concentration. Extreme volatility on thin liquidity is a maysir/gharar signal.
- **Riba surfaces:** does holding involve lending, staking-for-yield, interest-bearing backing, or leverage? Spot-holding usually avoids riba; yield mechanics often don't.
- **Underlying activity:** is the project's actual business itself halal? A clean token attached to a gambling, alcohol, adult-content, or interest-based-lending platform fails regardless of its technical structure.

### Phase 3 — Apply the five screens

Using `references/screening-framework.md` and the relevant category section, work through each screen and assign a clear status (Passes / Weak / Fails, or Neutral where it doesn't apply). Show your reasoning per screen — the user asked you to "dig how it falls under each reasoning," so make the per-screen logic explicit and tied to the Phase-2 findings.

The five screens:
1. **Māl mutaqawwim** — is it valid, ownable, commercially-valued property?
2. **Riba** — does earning/holding involve interest?
3. **Gharar** — is there *excessive, structural* uncertainty (not ordinary market risk)?
4. **Maysir** — does it function like gambling/pure speculation?
5. **Underlying utility & activity** — genuine economic purpose, and is the project itself halal?

Maysir and gharar are usually the decisive screens for speculative tokens; riba is decisive for yield/stablecoin products; the underlying-activity screen is decisive when the project's business is itself prohibited.

### Phase 4 — Render a calibrated verdict

Tally the screens, then translate the result into where the three scholarly camps would likely land (see `scholarly-positions.md`): the **permissive** camp (default permissibility unless clearly prohibited), the **conditional** camp (permissible only if specific conditions are met), and the **prohibitive** camp (crypto speculation broadly impermissible). State plainly which way the weight of mainstream screening leans, what specific facts drive that, and **what would change the verdict** (e.g., "if the team published audits and the token developed genuine sustained utility, the gharar concern would ease"). Close by recommending a qualified scholar or Shariah advisory service for a binding ruling.

## Output format

Use this structure unless the user asks for something shorter. It mirrors the "define the framework, then apply it screen by screen" flow that makes the reasoning auditable.

```
## Upfront caveat
[1–2 sentences: not a fatwa, no consensus on crypto, consult a scholar.]

## What "shariah-compliant" means for a token
[The five screens, briefly defined, so the verdict is interpretable.]

## What [TOKEN] actually is
[The Phase-2 findings: category, utility, tokenomics, team/audits, market behavior, launch. Cut through marketing.]

## Screening [TOKEN]
[One subsection per screen — Māl, Riba, Gharar, Maysir, Utility & underlying activity — each with status + reasoning tied to the findings above.]

## Where this lands
[Calibrated verdict across the permissive / conditional / prohibitive camps; which way the weight leans and why; what would change it; recommendation to consult a qualified scholar.]
```

Adapt length to the request. Always cite the live research behind factual claims about the token. Keep the fiqh accurate and avoid inventing fatwas or attributing rulings to scholars you haven't verified — if you're unsure whether a specific scholar ruled a specific way, describe the camp's reasoning generically instead.

## A note on respect and tone

People ask this question because it matters to their conscience and their faith. Treat it with the seriousness it deserves: be rigorous, be honest about uncertainty, never flippant about the religious stakes, and never pretend to an authority you don't have. The most useful thing you can do is give them a clear, well-researched map of the terrain and send them to a real scholar for the final word.
