# Infrastructure

Infrastructure code and sanitized configuration belong here.

```text
infrastructure/
├── azure/      # Bicep, ARM, Terraform, or deployment documentation
├── network/    # VLANs, address plans, firewall policy, and switch documentation
└── proxmox/    # VM templates, inventories, and provisioning configuration
```

Never commit Terraform state, credentials, exported private keys, or identifying configuration. Provide example variable files with placeholder values.

