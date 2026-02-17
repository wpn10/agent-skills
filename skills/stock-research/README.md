# Stock Research: Short-Term Trade Ideas & Leveraged ETF Finder

Find actionable long/short setups, swing trade candidates, and leveraged ETF plays -- all with defined entries, targets, and stop losses.

## What It Does

This skill turns your AI agent into a short-term trading research assistant. Give it a ticker, sector, or strategy and it returns structured trade ideas with clear risk/reward parameters. No ticker? It scans the broad market for the best current opportunities.

**What you get for every trade idea:**
- Long or short positioning with a clear thesis
- Entry zone, price target, and stop loss
- Risk/reward ratio (minimum 2:1)
- Timeframe (days to weeks)
- Catalyst and confidence level

## How It Works

The skill follows a six-step research workflow:

1. **Market Context** -- reads current sentiment, VIX, index performance, and upcoming catalysts
2. **Candidate Screening** -- finds stocks with momentum breakouts, breakdowns, or catalyst-driven setups
3. **Trade Analysis** -- structures each idea with entry/target/stop/R:R
4. **Leveraged ETF Matching** -- maps directional bets to 2x/3x ETFs (TQQQ, SOXL, TNA, etc.)
5. **Risk Dashboard** -- overall market risk score, correlation warnings, key upcoming events

## Usage

```
/stock-research [ticker-or-sector-or-strategy]
```

**Examples:**
- `/stock-research` -- scan the market for the best trades right now
- `/stock-research NVDA` -- analyze NVIDIA for a short-term setup
- `/stock-research semiconductors` -- find trades in the semiconductor sector
- `/stock-research momentum breakouts` -- screen for stocks breaking out of consolidation
- `/stock-research leveraged ETFs` -- focus on leveraged ETF opportunities

## Output Preview

Every research output includes:

| Section | What's In It |
|---------|-------------|
| Market Pulse | Sentiment, indices, VIX, key catalysts |
| Trade Ideas | 3-5 long/short setups with full parameters |
| Leveraged ETF Plays | Bull/bear ETF pairs aligned with market thesis |
| Risk Dashboard | Risk score (1-10), allocation guidance, event calendar |

## Covered Instruments

- Individual stocks (any US-listed equity)
- Leveraged ETFs: TQQQ/SQQQ, SPXL/SPXS, SOXL/SOXS, LABU/LABD, FNGU/FNGD, TNA/TZA, NUGT/DUST, UVXY
- Sector ETFs with directional momentum

## Important

This skill generates AI-powered research for informational purposes only. It is not financial advice. All trading involves risk of loss. Leveraged ETFs carry amplified risk and are designed for short-term trading only. Always do your own due diligence.
