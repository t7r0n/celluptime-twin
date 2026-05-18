# Robot Cell Reliability Twin

A local manufacturing-cell reliability prototype that models synthetic robot-cell variation, failure risk, and release readiness.

`forge-robotics-cell-reliability-twin` favors explicit fixtures, deterministic checks, and reviewable artifacts over hidden services or live data.

## Engineering read

Manufacturing Cell Reliability Twin: Scan-Simulate-Automate With Failure Economics.

## What is measured

- Synthetic cycle, part, fixture, sensor, and throughput records.
- Reliability analysis for variation tolerance, downtime risk, and throughput constraints.
- Static dashboard, evidence graph, and benchmark output for reproducible review.

## One-pass run

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

## Evidence packet

- `outputs/dashboard.html`
- `outputs/decision_report.md`
- `outputs/evidence_graph.mmd`
- `outputs/risk_or_quality_report.csv`
- `outputs/benchmark.md`
- `outputs/demo_pack.md`

## Checks

```bash
uv run ruff check .
uv run pytest -q
uv run app verify
```

## No-secrets boundary

`Robot Cell Reliability Twin` checks in synthetic fixtures only. Runtime state, dashboards, caches, virtual environments, and generated packs stay out of git.
