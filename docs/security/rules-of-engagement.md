# Lab Rules of Engagement

## Authorization boundary

Security testing is permitted only against assets owned by the project owner or explicitly authorized for this lab. Household, school, employer, public-cloud, and internet systems are out of scope unless separately and explicitly authorized.

## Environment boundaries

- Place attack-simulation systems in a dedicated lab segment.
- Deny unnecessary access to household and management networks.
- Restrict outbound internet access to documented requirements.
- Do not expose intentionally vulnerable services directly to the internet.
- Separate analyst-visible data from protected scenario ground truth.

## Required scenario controls

Every executable scenario must document:

- Authorized target assets
- ATT&CK tactic, technique, and sub-technique
- Preconditions and required privileges
- Expected system and telemetry effects
- Maximum duration and resource limits
- Emergency stop method
- Cleanup and restoration procedure
- Success and detection criteria

## Prohibited activity

- Testing third-party systems without authorization
- Credential use outside accounts created for the lab
- Uncontrolled propagation or persistence
- Destructive encryption, wiping, or denial of service
- Exfiltration of real personal or confidential information
- Publishing functional secrets or unsanitized identifying data

## Emergency stop

The final validation platform must support disabling the scheduler, stopping active execution, isolating the attack segment, and preserving sufficient evidence to understand what occurred.

