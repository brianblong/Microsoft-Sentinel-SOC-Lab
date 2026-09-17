# Roadmap

## Phase 0 — Planning and governance

### Deliverables

- [x] Repository framework
- [x] Project charter
- [x] Initial roadmap
- [x] Rules of engagement
- [x] Budget guardrails
- [x] Current-state architecture diagram
- [x] IP address and naming plan
- [x] Azure subscription and licensing inventory
- [x] Phase 1 backlog

### Exit criteria

- Safety boundaries and authorized assets are recorded.
- Monthly budget and alert thresholds are selected.
- Naming, tagging, and documentation conventions are established.

## Phase 1 — SC-200 Sentinel foundation

Target duration: 3–5 weeks.

### Learn before deploying

- Azure subscriptions, resource groups, RBAC, naming, tagging, budgets, and the shared-responsibility model
- Log Analytics workspace architecture, retention, ingestion, and cost controls
- Microsoft Sentinel architecture and the purpose of data connectors
- Windows security telemetry fundamentals
- KQL fundamentals before writing production-style analytics rules

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

### Learn before deploying

- VLANs, trunks, routing, firewall policy, management networks, and rollback before changing the physical switch
- Active Directory fundamentals and recovery before promoting a domain controller
- Windows event logging, Sysmon, Linux Syslog, and Auditd before enabling broad ingestion
- Defender product roles and licensing boundaries before integration
- Logic Apps identities, permissions, and approval controls before automating response
- Docker networking and application logging before onboarding container workloads

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

### Learn before building

- Python project structure, testing, configuration, logging, and secrets management
- Safe threat emulation, authorization boundaries, cleanup, and emergency-stop design
- MITRE ATT&CK mapping and detection-validation methodology
- Randomization, protected ground truth, experiment design, and scoring integrity
- API design, job scheduling, data schemas, and failure handling
- Measurement limitations before interpreting detection and response metrics

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
