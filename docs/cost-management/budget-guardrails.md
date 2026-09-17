# Budget Guardrails

## Phase 1 budget decision

- **Provisional monthly maximum:** USD 25
- **Scope:** Phase 1 Azure resource group and associated Sentinel/Log Analytics usage
- **Alert thresholds:** 50%, 75%, 90%, and 100% of the monthly maximum
- **Alert recipient:** Project owner; confirm the destination privately before deployment
- **Review cadence:** Weekly and immediately after enabling a new connector
- **Approval rule:** Do not raise the maximum or start a paid trial without recording the reason and end date.

Azure budgets notify but do not automatically stop resources. Prefer a narrow data
collection rule, deliberate retention, and a workspace daily cap as defense in depth.
Choose the exact daily cap after measuring the first endpoint; setting it too low can
interrupt security visibility.

## Before deployment

- Confirm or amend the USD 25 maximum monthly Azure budget.
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
