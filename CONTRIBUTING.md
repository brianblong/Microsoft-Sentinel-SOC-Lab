# Contributing

This is currently a personal learning project. Contributions may be accepted later after a license and review process are selected.

## Working conventions

1. Create a focused branch for each meaningful change.
2. Do not include secrets, personal data, or unsanitized evidence.
3. Explain the learning objective and security impact.
4. Include validation steps and rollback guidance.
5. Map detections and simulations to MITRE ATT&CK where applicable.
6. Update relevant documentation in the same change.

## Commit style

Use concise, outcome-oriented messages:

```text
docs: define Phase 1 Sentinel architecture
feat: add Windows failed-logon detection
test: validate T1110 scenario telemetry
fix: exclude approved service accounts from alert
```

## Pull-request checklist

- [ ] Scope is limited and clearly explained.
- [ ] No secrets or identifying data are present.
- [ ] Documentation is updated.
- [ ] Tests or manual validation steps are included.
- [ ] Cost and rollback impact are documented.
- [ ] ATT&CK and SC-200 mappings are included when applicable.

