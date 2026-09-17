# Project Charter

## Mission

Build an incremental Microsoft-focused security operations lab that develops practical SC-200 skills and evolves into a vendor-aware SOC validation platform.

## Primary objectives

1. Learn Sentinel, Defender, KQL, incident response, threat hunting, and SOAR through implementation.
2. Operate a realistic hybrid Windows and Linux monitoring environment.
3. Engineer, test, tune, and document original detections.
4. Build an isolated scenario platform that hides attack selection from the analyst while retaining protected ground truth.
5. Measure detection coverage and operational performance.
6. Publish a sanitized, reproducible portfolio demonstrating security and software-development skills.

## Guiding principles

- Use a learn-before-build gate for every major capability: understand the concept, complete a short readiness check, and only then deploy or modify the lab.
- Pair each implementation milestone with current learning resources, prioritizing official Microsoft documentation and training while labeling YouTube videos and third-party courses as supplementary.
- Build one working vertical slice before adding breadth.
- Prefer reproducible configuration and version-controlled content.
- Treat cost, privacy, isolation, and cleanup as design requirements.
- Separate scenario execution from analyst-visible evidence.
- Test detections against known expected telemetry.
- Record failures and design changes as portfolio evidence.
- Keep the platform portable enough to validate Sentinel, Wazuh, or Splunk detections.

## Learn-before-build workflow

Every major task follows this sequence:

1. Identify the concepts and prerequisites that should be learned first.
2. Review a small, curated set of current resources.
3. Explain the architecture, security, cost, and rollback implications.
4. Pass a practical readiness check in the project notes.
5. Implement the capability in the lab.
6. Validate telemetry, security behavior, and expected results.
7. Document evidence, mistakes, and lessons learned in GitHub.

Resource recommendations should include official documentation or Microsoft Learn material when available. Relevant YouTube videos and third-party courses may supplement those sources, but their publisher, date, cost, expected time, and role in the milestone should be made clear. See the [learning workflow](learning/README.md).

## In scope

- Microsoft Sentinel and Log Analytics
- Microsoft Defender security products available to the lab
- Microsoft Entra ID and Microsoft 365 telemetry when licensing permits
- Proxmox-hosted Windows and Linux systems
- Active Directory, Docker applications, DNS, firewall, Syslog, and Auditd
- KQL detections, workbooks, hunting queries, and Logic Apps
- Python and PowerShell validation software
- Safe simulations mapped to MITRE ATT&CK
- Measurement, reporting, documentation, and portfolio presentation

## Out of scope

- Testing systems not owned by or explicitly authorized for the lab
- Malware deployment outside a deliberately isolated research environment
- Persistence intended to survive documented scenario cleanup
- Collection or publication of real personal, employer, or school data
- Production-grade availability guarantees

## Initial definition of success

Phase 1 is successful when one Windows security event travels through the complete lifecycle from generation to collection, KQL detection, Sentinel incident, investigation, response documentation, and validation evidence.
