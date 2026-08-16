<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/alexbesp18/alexbesp18/main/assets/banner-dark.png">
  <img alt="Alexander Bespalov — long-horizon agent systems, built to run unattended. I build AI systems that refuse to ship unverified output. 15 public systems · 374 tests · keyless." src="https://raw.githubusercontent.com/alexbesp18/alexbesp18/main/assets/banner-light.png" width="100%">
</picture>

I build governed AI/data platforms for operating teams. Everything on this page is keyless — each repo carries a demo that runs in about ninety seconds — **15 systems, 374 tests, all green from a clean clone on 2026‑08‑15**, in two lanes. Nothing here needs an API key, an account, or my machine. Here is one of them:

### Ninety seconds, one real filing

```bash
git clone https://github.com/alexbesp18/manager-13f && cd manager-13f
uv sync && uv run pytest                              # 33 offline tests
uv run python examples/build_cached_duquesne_demo.py  # zero keys, zero network
```

That builds this — a real SEC 13F filing (Duquesne Family Office, Q1 2026, 70 positions, put/call sleeves read correctly) rendered into a verified one‑page intelligence sheet from a committed fixture:

<a href="https://raw.githubusercontent.com/alexbesp18/alexbesp18/main/assets/specimen-duquesne-full.png"><img alt="manager-13f specimen: Duquesne Family Office 13F intelligence sheet — header band with gross/long/call/put/net, then holdings grouped by sleeve with weight, QoQ action, price, YTD, RSI, analyst consensus" src="https://raw.githubusercontent.com/alexbesp18/alexbesp18/main/assets/specimen-duquesne-top.png" width="100%"></a>
<sub>Top of the sheet; click for the whole page. If the filing's number scale had been ambiguous, the engine would have refused to render it and said so.</sub>

### How a number earns its way out

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/alexbesp18/alexbesp18/main/assets/desk-dark.png">
  <img alt="Source → Engine → Gate → two exits: PASS (a verified sheet, brief, or worklist, with the receipt) or REFUSE (stops and names why: symbol and field, ambiguous scale, weak score, over budget, low confidence → a person). The refuse exit is the product." src="https://raw.githubusercontent.com/alexbesp18/alexbesp18/main/assets/desk-light.png" width="100%">
</picture>

---

### Markets lane — extracted from systems that run daily

The one‑person, AI‑operated equity research desk is the proving ground. These six are its organs, extracted from the systems that actually run on a schedule — each README says what the private original does every day.

| System | What it does | The gate that says no | Tests |
|---|---|---|---:|
| **[manager-13f](https://github.com/alexbesp18/manager-13f)** | SEC 13F filings → verified, options‑aware one‑page intelligence sheets; reads put/call sleeves correctly | refuses to render when a filing's number scale is ambiguous | 33 |
| **[market-technicals](https://github.com/alexbesp18/market-technicals)** | the desk's daily heartbeat: large‑universe technicals over a bundled neutral universe | a **parity contract** — every number must reproduce an independent reference; corrupt one value and it fails loudly, naming the symbol and field | 30 |
| **[macro-regime](https://github.com/alexbesp18/macro-regime)** | once‑daily trend + VIX regime read with 2/3‑close confirmation hysteresis | fail‑closed freshness gates; it computes, a human decides — it never transmits a trade | 83 |
| **[commodity-convexity](https://github.com/alexbesp18/commodity-convexity)** | convexity scoring for commodity equities | thin data or weak survivability **vetoes** an attractive score, and the veto names its weakest gate | 14 |
| **[shadow-eval](https://github.com/alexbesp18/shadow-eval)** | how a model earns a seat at the desk: rank agreement, weighted kappa, hallucination rate, MDE power | pre‑registered promotion gates published *before* results — a good‑looking score alone is not a promotion | 11 |
| **[equity-research-kit](https://github.com/alexbesp18/equity-research-kit)** | research artifacts treated as software: ingestion, evidence correction, visual lint | a spreadsheet clean‑open gate that reports UNAVAILABLE rather than a fake pass | 80 |

### Operations lane — reference implementations, synthetic fixtures

The same discipline pointed at business decisions instead of markets. These are reference implementations on synthetic fixtures — not extracted from a running system — and each one publishes a **decision contract**: who the user is, what it decides, and the boundary it refuses to cross.

| System | What it does | The boundary it refuses to cross | Tests |
|---|---|---|---:|
| **[call-intelligence](https://github.com/alexbesp18/call-intelligence)** | call transcripts → a validated 40‑field record | per‑field confidence routed to human review; a cost ceiling checked *before* work is done; a promotion gate a weak extractor cannot pass | 36 |
| **[weekly-performance-brief](https://github.com/alexbesp18/weekly-performance-brief)** | weekly segment results → the one brief a review actually needs | partial periods excluded; external segments can't become internal action items; never invents a cause for a change | 12 |
| **[capacity-scenario-planner](https://github.com/alexbesp18/capacity-scenario-planner)** | staffing before/after against a declared roster ceiling | separates a harmful plan from an efficiency gain, and prints the risk band it used | 13 |
| **[constrained-allocation-planner](https://github.com/alexbesp18/constrained-allocation-planner)** | explainable allocation under hard limits | confidence‑tiered moves, a real HOLD for the unallocated pool, a reported decision margin | 9 |
| **[conversation-coaching-brief](https://github.com/alexbesp18/conversation-coaching-brief)** | support conversations → one coachable behavior per team member | only when the issue repeats across enough reviewed conversations; coaching prompts, never performance ratings | 13 |
| **[creative-performance-lab](https://github.com/alexbesp18/creative-performance-lab)** | pre‑flight scoring of creative concepts against a prior library | flags lookalikes before spend; thresholds labeled illustrative rather than tuned | 9 |
| **[support-review-pipeline](https://github.com/alexbesp18/support-review-pipeline)** | support conversations → structured review records | every quote stays traceable to its source message | 8 |
| **[alert-lifecycle-simulator](https://github.com/alexbesp18/alert-lifecycle-simulator)** | alert streams → a deduplicated worklist | a measured before/after instead of a wall of notifications | 6 |

### The operating record

**[ops-log](https://github.com/alexbesp18/ops-log)** — the fleet's public operating record: failures published alongside wins, with the fix each one got. 17 tests guard the exporter itself.

Behind these: a personal fleet of 47 scheduled jobs across two Macs and the cloud, and the delegated agent runs that build and check them, mostly across two coding agents. Every run the wrappers take is logged. ops-log carries the ledger — 717 runs across two months, a 5.3% failure rate, and an honest note on what it can and cannot prove: 3.4% of rows carry a review annotation, which measures how often that field was filled in, not how often a review happened. Historical review coverage is not provable from the file. It is published rather than backfilled, and annotation starts now.

<sub>Test counts are what each suite reports from a clean clone on 2026‑08‑15 (pytest or unittest); 251 + 70 + 36 + 17 = 374.</sub>

Contact: [alexbespalovtx@gmail.com](mailto:alexbespalovtx@gmail.com)
