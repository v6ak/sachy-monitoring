# Generating Grafana dashboards and alerts

These instructions are shared for coding agents (Copilot, Claude Code, Codex, Antigravity, and similar tools).

## Generating Grafana dashboards through GitHub Copilot

### Preparation

- Forward the database to `localhost:8086`.
- Create a token with read-only access and store it in local variable `TOKEN`.
- Put GitHub Copilot into Agent mode.

### Prompt

Please generate a Flux-based Grafana dashboard. The datasource is `influxdb-flux`.

Maybe I should give you access to the database and you will inspect it and create a suitable dashboard.

I don't have influx installed locally. You can use curl or Docker instead.

You can connect to URL: `http://localhost:8086/`. The token is in local variable `TOKEN`. Organization name is `"čes.org"`. Bucket name is `bucketakke`.

For range limits, use:

`range(start: v.timeRangeStart, stop: v.timeRangeStop)`

### Common issues

- If JSON is used, ensure the request has `Content-Type: application/json`.
- A wrong `Content-Type` can trigger a misleading error that suggests adding `yield()`, but adding `yield()` does not fix that issue.

## Generating alerts through GitHub Copilot

Copilot may hallucinate that alerts can be generated and embedded directly in the dashboard, but Grafana dashboards cannot contain alert definitions.

## Dashboard definitions

- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/blocking-metrics-dashboard.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/certificates-dashboard-2.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/certificates-dashboard.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/game-metrics-dashboard.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/grafana-dashboard.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/jvm-metrics-dashboard.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/lila-fishnet-metrics-dashboard.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/lila-metrics-dashboard.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/lobby-metrics-dashboard.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/new-metrics-dashboard.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/ping-metrics-dashboard.json`
- `/tmp/workspace/v6ak/sachy-monitoring/dashboards/round-metrics-dashboard.json`
