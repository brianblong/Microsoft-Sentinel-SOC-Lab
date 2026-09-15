# Budget Guardrails

## Before deployment

- Select a maximum monthly Azure budget.
- Configure budget notifications at multiple thresholds.
- Record which resources continue billing when idle.
- Estimate daily ingestion before enabling verbose data sources.
- Choose retention settings deliberately.
- Apply consistent ownership, environment, and expiration tags.

## Ingestion controls

- Start with one endpoint and a narrow event set.
- Measure table-level volume before expanding.
- Avoid ingesting duplicate telemetry without a validation purpose.
- Use filtering and data-collection transformations where appropriate.
- Keep packet captures and raw high-volume data outside Sentinel unless required.

## Weekly review

| Item | Result |
|---|---|
| Current accumulated Azure cost | TBD |
| Estimated month-end cost | TBD |
| Log Analytics ingestion by table | TBD |
| Unexpected active resources | TBD |
| Resources safe to stop or remove | TBD |

## Decommission requirement

Every Azure deployment guide must include a verified shutdown or deletion procedure. Export reusable rules, queries, templates, and sanitized evidence before removing a resource.

