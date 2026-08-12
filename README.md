# I build AI systems that refuse to ship unverified output.

Most of what I run is a one-person, AI-operated equity research desk. These repos are its organs,
extracted from the systems that actually run — each README says what the private original does
daily, and each demo shows the engineering, keyless, in about 90 seconds.

**[manager-13f](https://github.com/alexbesp18/manager-13f)** — SEC 13F filings → verified, options-aware one-page intelligence sheets. Reads put/call sleeves correctly, and refuses to render when a filing's number scale is ambiguous. Keyless cached demo: a Duquesne Family Office (Druckenmiller) 13F specimen.

**[market-technicals](https://github.com/alexbesp18/market-technicals)** — the desk's daily heartbeat: a large-universe technicals engine whose numbers must reproduce an independent reference calculation before they count. The demo runs the parity suite on a bundled neutral universe — corrupt one value and it fails loudly, naming the symbol and field.

**[macro-regime](https://github.com/alexbesp18/macro-regime)** — once-daily trend + VIX regime read with 2/3-close confirmation hysteresis and fail-closed freshness gates. It computes; a human decides. It never transmits a trade.

**[commodity-convexity](https://github.com/alexbesp18/commodity-convexity)** — convexity scoring for commodity equities where thin data or weak survivability can VETO an attractive score — and the veto names its weakest gate.

**[shadow-eval](https://github.com/alexbesp18/shadow-eval)** — how a model earns a seat at the desk: pre-registered statistical gates (rank agreement, weighted kappa, hallucination rate, MDE power) published before results. A good-looking score alone is not a promotion.

**[equity-research-kit](https://github.com/alexbesp18/equity-research-kit)** — research artifacts treated as software: evidence correction, visual lint, and a spreadsheet clean-open gate that reports UNAVAILABLE rather than a fake pass.

**[ops-log](https://github.com/alexbesp18/ops-log)** — the fleet's public operating record. Failures are published alongside wins, with the fix each one got.

Behind these: ~12 scheduled systems firing ~130 times a day, and 600+ delegated agent runs across four model families — every one logged, with a different family reviewing high-stakes changes; ops-log above is the public slice of that record.

Contact: [alex@egmail.net](mailto:alex@egmail.net)
