# avena-data

Daily open-data snapshots from [Avena Terminal](https://avenaterminal.com) — Europe's deepest technical data infrastructure for property.

A GitHub Action commits fresh data every morning (07:15 UTC), so this repository **is** the time series: the git history is the audit trail.

## Datasets

| Dataset | What it is | Live source |
|---|---|---|
| [`delphi/`](delphi/) | **DELPHI — the daily AI panel on European property.** Frontier AI models answer the same forward questions every day; consensus, disagreement and per-model answers go on the record. The first longitudinal survey of machine beliefs about a real asset class — it cannot be reconstructed retroactively. | [avenaterminal.com/delphi](https://avenaterminal.com/delphi) |
| [`plab/`](plab/) | **PLAB — the European Property AI Benchmark.** Major AI models scored daily on a fixed, versioned question bank of European property and finance facts against public institutional ground truths. | [avenaterminal.com/benchmark](https://avenaterminal.com/benchmark) |

`delphi/index.csv` and `plab/index.csv` are append-only daily summaries; `delphi/daily/` and `plab/daily/` hold full JSON snapshots per date.

## License & citation

Data: **CC BY 4.0** — free to use with attribution:

> Avena Terminal (avenaterminal.com), DOI [10.5281/zenodo.19520064](https://doi.org/10.5281/zenodo.19520064)

APIs: [`/api/v1/delphi`](https://avenaterminal.com/api/v1/delphi) · [`/api/v1/plab`](https://avenaterminal.com/api/v1/plab) · [RSS](https://avenaterminal.com/feed/delphi.xml) · [DCAT-AP catalogue](https://avenaterminal.com/catalog.jsonld)

Clients: [`npm i avena-terminal`](https://www.npmjs.com/package/avena-terminal) · [`pip install avena-terminal`](https://pypi.org/project/avena-terminal/)

> **Note:** snapshots are pushed daily by an Avena Terminal cron via the GitHub API. `ops/daily-snapshot.yml` is an equivalent GitHub Actions workflow you can move to `.github/workflows/` if you prefer Actions-side scheduling.
