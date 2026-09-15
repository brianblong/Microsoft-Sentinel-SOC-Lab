# Detection Engineering

Organize detections by target platform while preserving shared metadata and test expectations.

```text
detections/
├── sentinel/
├── splunk/
└── wazuh/
```

Each detection should document:

- Purpose and threat hypothesis
- Required data sources and fields
- Query or rule implementation
- Frequency, lookback, grouping, and thresholds
- Entity mappings
- MITRE ATT&CK mappings
- Expected true-positive activity
- Known false positives and tuning
- Validation scenario and result
- Version and change history

