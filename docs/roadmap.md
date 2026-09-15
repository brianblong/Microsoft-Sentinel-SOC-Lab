# Roadmap

## Phase 0 — Planning and governance

### Deliverables

- [x] Repository framework
- [x] Project charter
- [x] Initial roadmap
- [x] Rules of engagement
- [x] Budget guardrails
- [ ] Current-state architecture diagram
- [ ] IP address and naming plan
- [ ] Azure subscription and licensing inventory
- [ ] Phase 1 backlog

### Exit criteria

- Safety boundaries and authorized assets are recorded.
- Monthly budget and alert thresholds are selected.
- Naming, tagging, and documentation conventions are established.

## Phase 1 — SC-200 Sentinel foundation

Target duration: 3–5 weeks.

### Deliverables

- [ ] Azure resource organization and access controls
- [ ] Log Analytics workspace and Microsoft Sentinel
- [ ] One onboarded Windows endpoint
- [ ] Available Defender, Entra ID, and Microsoft 365 integrations
- [ ] Initial KQL query library
- [ ] Initial analytics rules and incident workflow
- [ ] Initial workbook
- [ ] Documented end-to-end investigation
- [ ] SC-200 objective coverage record

### Exit criteria

- Telemetry ingestion and cost can be measured.
- At least one custom detection produces an investigable incident.
- The incident is triaged, scoped, mapped to ATT&CK, and documented.
- Resources can be safely disabled or removed using a recorded procedure.

## Phase 2 — Hybrid enterprise-style SOC

Target duration: 6–10 weeks.

### Deliverables

- [ ] Managed switch, VLANs, and firewall policy
- [ ] Proxmox Windows 11, Windows Server, AD, and Ubuntu systems
- [ ] Linux Syslog and Auditd ingestion
- [ ] DNS, firewall, network-sensor, and Docker telemetry
- [ ] Custom analytics rules and hunting library
- [ ] Threat-intelligence integration
- [ ] Logic Apps playbooks with approval safeguards
- [ ] MITRE ATT&CK coverage workbook
- [ ] Incident-response playbooks and case reports

### Exit criteria

- Windows, Linux, identity, network, and application telemetry are represented.
- Detection content is tested, tuned, documented, and version controlled.
- At least one safe response workflow is automated.

## Phase 3 — SOC validation platform

### Deliverables

- [ ] Scenario definition format
- [ ] Randomized campaign selector and scheduler
- [ ] Isolated execution agents and emergency stop
- [ ] Analyst-hidden ground-truth store
- [ ] Telemetry and detection validation tests
- [ ] Detection, investigation, and mitigation timing
- [ ] False-positive and MITRE coverage reporting
- [ ] Multi-step campaign support
- [ ] Cross-SIEM validation for Sentinel and optional Wazuh/Splunk

### Exit criteria

- An analyst can investigate an unknown selected scenario without seeing ground truth.
- Results are scored reproducibly against documented expectations.
- Failed or partial detections create an actionable improvement backlog.

