# I build AI systems that refuse to ship unverified output.

I build governed AI/data platforms for operating teams. Everything below is keyless and runs in
about 90 seconds — 15 systems, 370 tests, in two lanes.

### Markets lane

The one-person, AI-operated equity research desk is the proving ground. These repos are its
organs, extracted from the systems that actually run — each README says what the private
original does daily.

**[manager-13f](https://github.com/alexbesp18/manager-13f)** — SEC 13F filings → verified, options-aware one-page intelligence sheets. Reads put/call sleeves correctly, and refuses to render when a filing's number scale is ambiguous. Keyless cached demo: a Duquesne Family Office (Druckenmiller) 13F specimen.

**[market-technicals](https://github.com/alexbesp18/market-technicals)** — the desk's daily heartbeat: a large-universe technicals engine whose numbers must reproduce an independent reference calculation before they count. The demo runs the parity suite on a bundled neutral universe — corrupt one value and it fails loudly, naming the symbol and field.

**[macro-regime](https://github.com/alexbesp18/macro-regime)** — once-daily trend + VIX regime read with 2/3-close confirmation hysteresis and fail-closed freshness gates. It computes; a human decides. It never transmits a trade.

**[commodity-convexity](https://github.com/alexbesp18/commodity-convexity)** — convexity scoring for commodity equities where thin data or weak survivability can VETO an attractive score — and the veto names its weakest gate.

**[shadow-eval](https://github.com/alexbesp18/shadow-eval)** — how a model earns a seat at the desk: pre-registered statistical gates (rank agreement, weighted kappa, hallucination rate, MDE power) published before results. A good-looking score alone is not a promotion.

**[equity-research-kit](https://github.com/alexbesp18/equity-research-kit)** — research artifacts treated as software: evidence correction, visual lint, and a spreadsheet clean-open gate that reports UNAVAILABLE rather than a fake pass.

---

### Operations lane

The same discipline pointed at business decisions instead of markets. These are reference
implementations on synthetic fixtures — not extracted from a running system — and each one
publishes a **decision contract**: who the user is, what it decides, and the boundary it
refuses to cross.

**[weekly-performance-brief](https://github.com/alexbesp18/weekly-performance-brief)** — weekly segment results → the one brief a review actually needs. Partial periods are excluded, external segments can't become internal action items, and it describes changes without inventing causes for them.

**[capacity-scenario-planner](https://github.com/alexbesp18/capacity-scenario-planner)** — staffing before/after against a declared roster ceiling, separating a harmful plan from an efficiency gain and printing the risk band it used.

**[constrained-allocation-planner](https://github.com/alexbesp18/constrained-allocation-planner)** — explainable allocation under hard limits: confidence-tiered moves, a real HOLD for the unallocated pool, and a reported decision margin.

**[conversation-coaching-brief](https://github.com/alexbesp18/conversation-coaching-brief)** — support conversations → one coachable behavior per team member, and only when the issue repeats across enough reviewed conversations. Coaching prompts, never performance ratings.

**[creative-performance-lab](https://github.com/alexbesp18/creative-performance-lab)** — pre-flight scoring for creative concepts against a prior library, flagging lookalikes before spend. Its thresholds are labeled illustrative rather than tuned.

**[alert-lifecycle-simulator](https://github.com/alexbesp18/alert-lifecycle-simulator)** — alert streams → a deduplicated worklist with a measured before/after, instead of a wall of notifications.

**[support-review-pipeline](https://github.com/alexbesp18/support-review-pipeline)** — support conversations → structured review records where every quote stays traceable to its source message.

**[call-intelligence](https://github.com/alexbesp18/call-intelligence)** — call transcripts → a validated 40-field record, with per-field confidence routed to human review, a cost ceiling checked before work is done, and a promotion gate a weak extractor cannot pass.

---

### The operating record

**[ops-log](https://github.com/alexbesp18/ops-log)** — the fleet's public operating record. Failures are published alongside wins, with the fix each one got.

Behind these: a personal fleet of 47 scheduled jobs across two Macs and the cloud, and 700+ delegated agent runs across four model families. Every run the wrappers take is logged. ops-log carries the ledger itself — 717 runs across two months, a 5.3% failure rate, and an honest note on what it can and cannot prove: 3.4% of rows carry a review annotation, which measures how often that field was filled in, not how often a review happened. Historical review coverage is not provable from the file. It is published rather than backfilled, and annotation starts now.

Contact: [alex@egmail.net](mailto:alex@egmail.net)
