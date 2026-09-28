# EnviroProcure

**An offline-first tool for comparing water-treatment equipment procurement options.**

[中文说明](README.md) · [Calculation methodology](docs/METHODOLOGY.md)

Version 0.1.0 is a working starter project with entirely synthetic examples. No customer deployments, adoption metrics, or achieved savings are claimed.

## Use

Download and extract the project, then open `index.html` in a modern browser. No installation, server, account or API key is needed. The interface is currently in Simplified Chinese; the repository includes English onboarding documentation.

Edit project assumptions and supplier inputs, then leave the input field to update the comparison. Export CSV for spreadsheet review. Export/import JSON to back up and resume a complete project. Browser local storage is a convenience, not a durable backup.

## Features

- Consistent annual throughput, operating days, electricity price and assessment horizon.
- Upfront equipment/delivery cost and annual electricity, chemical and maintenance cost.
- Technical-review, delivery and warranty gates before ranking.
- Transparent weighted cost, quality, delivery and service scoring.
- Risk likelihood/impact, follow-up action and owner.
- Local persistence, JSON import/export, CSV export and print styles.

One project supports 1–12 suppliers. Currency labels include CNY, USD, AUD and EUR; there is no exchange-rate conversion. All inputs must already use a common currency and tax basis.

## Cost model

```text
Annual volume = daily flow × annual operating days
Annual operating cost = annual volume × (energy per m³ × electricity price + chemical cost per m³)
                        + annual maintenance
Assessment-period total = equipment + installation/delivery + years × annual operating cost
```

This is an undiscounted, constant-cost comparison over a chosen horizon, not a complete life-cycle cost model. It excludes financing, residual value, tax differences, price escalation, downtime, labor and major replacement costs. Quality/service scores and technical acceptance are user judgments; the tool does not certify performance or regulatory compliance.

Scores are relative to the eligible candidate set. Cost score = minimum eligible total cost / candidate total cost × 100; delivery score = shortest eligible lead time / candidate lead time × 100. Weights are normalized to sum to one. Ineligible bids never set scoring baselines. Ties retain equal ranks.

## Development

Node.js 22+ is needed only for tests. There are no package dependencies.

```sh
npm test
```

Core arithmetic and validation live in `assets/engine.js` and run in both Node and the browser. See [contribution instructions](CONTRIBUTING.md) for reporting reproducible issues.

The initial scaffold was developed with AI assistance. Maintainers should review assumptions, understand the code they change, and document actual validation. Building this project does not establish eligibility for any external sponsorship program.

## License

MIT — see [LICENSE](LICENSE).
