# Shariah Token Checker

A deep-research Shariah-compliance checker for cryptocurrency tokens, packaged as an [Agent Skill](https://github.com/agentskills/agentskills) (the open `SKILL.md` format). Give it a token name or contract address and it researches what the asset actually is, then applies the five classical Islamic-finance screens — **māl** (valid, ownable property), **riba** (interest), **gharar** (excessive uncertainty), **maysir** (gambling/speculation), and **underlying utility & activity** — and returns a structured, scholar-calibrated report rather than a one-word verdict.

## ⚠️ Important disclaimer

**This is not a fatwa.** The output is a research aid, not a binding religious ruling. Cryptocurrency has **no scholarly consensus** — qualified scholars genuinely disagree, and the same token can be ruled differently by different authorities. The skill presents where the major scholarly camps would likely land and what would change the answer; it does not pronounce a final verdict. **For a binding ruling, consult a qualified scholar or a reputable Shariah advisory service.**

## Example

Invoke it by asking a natural-language question — you don't need to mention "skill" or "shariah" explicitly:

> Is $TOKEN at `0x1234...abcd` shariah-compliant? Deep research.

Other phrasings that trigger it:

> Can I invest in this coin as a Muslim?

> Compare the Islamic permissibility of $TOKEN_A and $TOKEN_B.

Saying "deep research" or "comprehensive" tells it to widen the research (8–20+ searches across the token's identity, fundamentals, market behavior, and the relevant fiqh) before screening.

## Install

### Claude Code

Clone or copy the `shariah-token-checker/` folder into one of your skills directories:

```bash
# Personal — available across all your projects
git clone https://github.com/<your-username>/shariah-token-checker.git ~/.claude/skills/shariah-token-checker

# OR project-scoped — available only in the current project
git clone https://github.com/<your-username>/shariah-token-checker.git .claude/skills/shariah-token-checker
```

Make sure `SKILL.md` sits at the root of the `shariah-token-checker/` folder (not nested in a subfolder), then start a new Claude Code session so the skill is picked up.

### Claude.ai (web/desktop)

1. Download this repository as a ZIP (**Code → Download ZIP** on GitHub).
2. In Claude, go to **Settings → Customize** and upload the ZIP.
3. The upload must be a ZIP archive with `SKILL.md` at the root.

Once installed, just ask a halal/haram crypto question and the skill triggers automatically.

## What's inside

The skill ships with three reference files that the model reads as it works:

- **`references/screening-framework.md`** — the five screens explained in depth, with the underlying fiqh concepts and guidance on how to weigh each one. Read before writing the analysis.
- **`references/token-categories.md`** — how the screens apply differently across token types (memecoins, P2E/GameFi, payment coins, DeFi/yield tokens, stablecoins, asset-backed/RWA, governance, and NFT-linked tokens), plus the red flags specific to each.
- **`references/scholarly-positions.md`** — the three scholarly camps (permissive, conditional, prohibitive), named scholars and fatwa bodies, and how to phrase a calibrated conclusion. Read before writing the verdict.

`SKILL.md` at the root ties these together and defines the four-phase workflow (identify the token → establish what it actually is → apply the five screens → render a calibrated verdict).

## Compatibility (not just Claude)

This skill follows the open [Agent Skills `SKILL.md` standard](https://github.com/agentskills/agentskills), so it is **not tied to Claude**. The content is plain, model-agnostic markdown with no vendor-specific tool calls, which means any agent or harness that supports the format can load and run it, including:

- **Claude** — Claude Code, Claude.ai, and the Claude Agent SDK (see [Install](#install) above)
- **OpenAI Codex CLI**, **Google Gemini CLI**
- **GitHub Copilot** (via VS Code's agent skills support), **Cursor**, **Cline**, **Windsurf**, **OpenCode**, and other skills-compatible tools

For a harness that supports Agent Skills, place the `shariah-token-checker/` folder in that tool's skills directory (consult its docs for the path) and start a new session. For any other agent, you can simply paste the contents of `SKILL.md` (and the relevant `references/` files) into the system prompt or context manually.

**One requirement applies everywhere:** this is a research-heavy skill, so the agent must have **live web search / browsing capability**. Without the ability to research what a token actually is, the screening cannot be performed reliably.

## License

Licensed under the Apache License 2.0. See [LICENSE](./LICENSE) for the full text.
