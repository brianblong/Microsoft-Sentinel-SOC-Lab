# Phase 1 Backlog — SC-200 Sentinel Foundation

Target duration: 3–5 weeks. Execute in order and keep the first vertical slice small.

## Definition of ready

- [ ] Complete the go/no-go checklist in `azure/subscription-licensing-inventory.md`.
- [ ] Confirm the budget and alert recipient in `cost-management/budget-guardrails.md`.
- [ ] Confirm the address plan does not overlap active local or VPN routes.
- [ ] Select one owned Windows lab endpoint and document its rollback method privately.

## P0 — Foundation and cost controls

- [ ] Create one tagged Phase 1 Azure resource group.
- [ ] Create one Log Analytics workspace in the selected region.
- [ ] Enable Microsoft Sentinel on that workspace.
- [ ] Configure Azure RBAC using least privilege.
- [ ] Create the Azure budget and threshold notifications before ingesting data.
- [ ] Record retention, daily-cap, and deletion decisions.
- [ ] Write and test the resource-removal procedure.

**Acceptance:** Resource inventory, access, budget alerts, expected cost sources, and
rollback steps are documented without secrets.

## P0 — First Windows telemetry

- [ ] Install or register the supported collection path for one Windows endpoint.
- [ ] Configure Azure Monitor Agent and a narrow data collection rule.
- [ ] Enable the Windows Security Events via AMA connector.
- [ ] Confirm fresh records arrive in the expected table.
- [ ] Measure daily ingestion by table and record the result.

**Acceptance:** A query returns a fresh event from the selected endpoint and ingestion
volume is measurable.

## P0 — KQL, detection, and incident

- [ ] Save queries for freshness, event counts, ingestion volume, failed logons, and host activity.
- [ ] Generate a benign, authorized test event on the lab endpoint.
- [ ] Build one scheduled analytics rule with entity mapping and ATT&CK mapping.
- [ ] Confirm the rule produces an alert and incident.
- [ ] Tune the threshold or exclusions and record the reason.

**Acceptance:** A custom detection reliably turns the known test activity into one
investigable incident without using real credentials or destructive behavior.

## P1 — Investigation and visualization

- [ ] Assign and triage the incident.
- [ ] Build the timeline, identify affected entities, and scope related activity.
- [ ] Record evidence, disposition, ATT&CK technique, and lessons learned.
- [ ] Create an initial workbook showing endpoint events and detection results.
- [ ] Add sanitized screenshots or exports only when they contain no identifiers.

**Acceptance:** A reader can reproduce the investigation from repository artifacts.

## P1 — Integration and SC-200 evidence

- [ ] Inventory available Defender, Entra ID, and Microsoft 365 connectors.
- [ ] Enable only licensed, useful, cost-understood integrations.
- [ ] Update `sc-200/objective-mapping.md` with links to completed evidence.
- [ ] Run the shutdown/removal procedure or a non-destructive dry run.
- [ ] Complete the Phase 1 retrospective and create Phase 2 follow-up items.

## Phase 1 exit criteria

- Telemetry ingestion and cost are measured.
- At least one custom detection produces an investigable incident.
- The incident is triaged, scoped, mapped to ATT&CK, and documented.
- Resources can be safely disabled or removed using a recorded procedure.

