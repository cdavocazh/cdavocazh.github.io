---
hide:
  - navigation
  - toc
---

# Kris Zhang

### AI / Growth PM — agentic systems, financial data, product strategy

Singapore-based. Staff Product Manager (Growth) at DCS Group (DeCard) — a B2C PayFi /
crypto-card business. Outside work I build multi-agent systems for systematic trading
analysis, macro market intelligence, and financial research.

[GitHub](https://github.com/cdavocazh){ .md-button } [LinkedIn](https://www.linkedin.com/in/kriszhang01/){ .md-button }

---

## Projects

<div class="grid cards" markdown>

-   :material-graph-outline: **[Macro Trader](projects/macro-trader.md)**

    ---

    End-to-end multi-agent pipeline for systematic trading analysis. Six agents —
    perception, trade review, idea generation, risk QA, infra health, process
    review — under a DAG orchestrator with deterministic risk gates, per-agent
    context budgets, and TF-IDF memory with 90-day retention.

    *Python · Claude Code agents · DAG orchestration · SQLite · systemd*

-   :material-chart-timeline-variant: **[Market Tracker](projects/market-tracker.md)**

    ---

    Automated market-tracking stack: 88+ macro indicators, quarterly financials for
    ~500 US large-caps, streaming news with sentiment scoring, futures positioning,
    Polymarket, Hyperliquid, Bitcoin and onchain metrics, Twitter-list summarization.
    Public macro layer + live dashboard.

    *Python · multi-source ingestion · FinBERT · Dash / React / Grafana · systemd*

-   :material-cog-outline: **[Financial Agent](projects/financial-agent.md)**

    ---

    Macro & financial-analysis agent where Claude Code is the runtime — no agent
    framework. A skill dispatcher routes ~50 analysis commands (macro regime,
    financial-stress scoring, late-cycle detection, stop-loss technicals, equity
    analysis) to a deterministic Python tool layer.

    *Python · Claude Code skills · MCP · dispatcher pattern · agent-native retrieval*

</div>

---

## Focus areas

- **Agentic systems** — orchestration patterns, memory design, evaluation, cost/latency routing
- **Financial & market-data pipelines** — macro, equity, crypto, onchain, prediction markets
- **Product management** — AI-product strategy, growth loops, payments / fintech / PayFi

See [About](about.md) for background and contact.
