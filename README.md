# newtype AI Stack

`newtype-ai-stack` is a lightweight methodology toolkit for analyzing AI industry-chain investment questions with the **newtype AI Stack** framework.

It turns companies, tickers, technologies, industry news, bottlenecks, and portfolio questions into structured research judgments:

- where an asset sits in the AI stack
- who benefits or loses from an AI industry event
- where scarcity is moving next
- whether a company is a bridge winner or an endgame winner
- how to organize candidates into Core 7 / N-Stack 20 / Watch List 50

It can be used with Codex, ChatGPT, Claude, Gemini, local agents, or any workflow that can load Markdown instructions and reference files.

> This toolkit provides a research framework only. It is not personalized investment advice.

## Use

You can read `SKILL.md` as the main router and load the relevant method pack from `references/` as needed.

For Codex, install from GitHub into your local skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
git clone https://github.com/newtype-01/newtype-ai-stack.git \
  "${CODEX_HOME:-$HOME/.codex}/skills/newtype-ai-stack"
```

Restart Codex after installation.

Then call:

```text
$newtype-ai-stack
```

For other tools, copy or reference `SKILL.md` plus the relevant files under `references/`.

## What It Covers

The toolkit uses one lightweight router in `SKILL.md` and loads detailed method packs from `references/` only when needed.

| User intent | Method pack |
| --- | --- |
| Map a company, ticker, product, technology, or concept to the AI stack | `references/stack-mapping.md` |
| Translate AI industry news into beneficiaries, losers, and validation signals | `references/stack-news.md` |
| Trace current and future scarcity bottlenecks | `references/scarcity-trace.md` |
| Judge bridge winners vs endgame winners | `references/bridge-vs-endgame.md` |
| Build a Core 7 / N-Stack 20 / Watch List 50 allocation framework | `references/position-sizing.md` |
| Shared stack definitions, scarcity levels, and compliance boundaries | `references/shared-framework.md` |

## The Seven-Layer AI Stack

```text
Layer 7  Apps
Layer 6  Models
Layer 5  Cloud / IaaS
Layer 4  Compute Hardware
Layer 3  Interconnect & Memory
Layer 2  Infrastructure
Layer 1  Energy
```

The core belief is that durable investment scarcity often concentrates below the application layer, especially in layers 1-4: energy, infrastructure, interconnect and memory, and compute hardware.

## Example Prompts

```text
$newtype-ai-stack 分析一下 VRT 在 AI 产业链的位置
```

```text
$newtype-ai-stack HBM 不再短缺后,下一个瓶颈是什么?
```

```text
$newtype-ai-stack NVDA 是过渡期赢家还是终局赢家?
```

```text
$newtype-ai-stack 给 NVDA, TSM, ASML, MU, VRT, CEG, AVGO 做一个 Core / N-Stack / Watch List 分仓
```

## Repository Layout

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── shared-framework.md
│   ├── stack-mapping.md
│   ├── stack-news.md
│   ├── scarcity-trace.md
│   ├── bridge-vs-endgame.md
│   └── position-sizing.md
├── README.md
├── README.zh.md
└── LICENSE
```

## Disclaimer

All outputs from this toolkit are research judgments based on the newtype AI Stack methodology. They do not constitute personalized investment advice, financial advice, or a recommendation to buy or sell any security.

Users should verify all real-time data independently, including prices, market caps, valuation multiples, financial statements, order books, capacity, market share, regulatory status, and management guidance. Investment decisions should account for personal risk tolerance, capital constraints, tax situation, and professional advice where appropriate.

## License

MIT
