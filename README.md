# Robot Cell Reliability Twin

A local manufacturing-cell reliability prototype that models synthetic robot-cell variation, failure risk, and release readiness.

## Features

- Synthetic cycle, part, fixture, sensor, and throughput records.
- Reliability analysis for variation tolerance, downtime risk, and throughput constraints.
- Static dashboard, evidence graph, and benchmark output for reproducible review.

## Run Locally

```bash
uv sync
uv run app init-demo
uv run app ingest fixtures/
uv run app analyze
uv run app verify
uv run app dashboard
uv run app benchmark
uv run app export-demo-pack
uv run pytest -q
uv run ruff check .
```

## Outputs

- `outputs/dashboard.html`
- `outputs/decision_report.md`
- `outputs/evidence_graph.mmd`
- `outputs/risk_or_quality_report.csv`
- `outputs/benchmark.md`
- `outputs/demo_pack.md`

## Data Policy

This project runs fully locally on deterministic synthetic fixtures. It does not require external APIs, credentials, private datasets, network access, or production systems.
