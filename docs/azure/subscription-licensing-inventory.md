# Azure Subscription and Licensing Inventory

- **Inventory date:** 2026-09-17
- **Handling:** Record status here, but keep account identifiers and billing details in a private location.

## Phase 1 requirements

| Capability | Minimum requirement | Recorded status | Phase 1 action |
|---|---|---|---|
| Microsoft Entra tenant | Tenant with an MFA-protected administrator | Verify before deployment | Confirm sign-in and MFA; do not record tenant ID here |
| Azure subscription | Active subscription permitted to create a resource group and Log Analytics workspace | Verify before deployment | Confirm offer, spending limit, and subscription state privately |
| Azure RBAC | Ability to create resources and assign only necessary lab roles | Verify before deployment | Document effective roles before changes |
| Microsoft Sentinel | Available in the chosen Azure region | Planned | Enable on the Phase 1 workspace only |
| Windows endpoint | Owned Windows 10/11 or Windows Server lab system | Planned | Use a disposable VM or dedicated lab endpoint |
| Azure Monitor Agent | Supported endpoint and outbound connectivity | Planned | Install through the Sentinel connector workflow |
| Microsoft Defender XDR | Optional; entitlement varies by product/license | Optional | Connect only products already licensed for the lab |
| Entra sign-in/audit logs | Tenant availability and connector permissions | Optional | Validate entitlement before connector activation |
| Microsoft 365 Defender data | Appropriate Microsoft 365/Defender license | Optional | Do not purchase solely to satisfy the first vertical slice |

## Private pre-deployment record

Record the following outside Git before creating resources:

- Tenant display name and tenant ID
- Subscription display name and subscription ID
- Subscription offer type, billing owner, and spending-limit behavior
- Administrator account and MFA verification date
- Effective Azure roles and their scopes
- Microsoft 365 and Defender licenses, trial expiration dates, and auto-renewal state
- Selected Azure region and confirmation that required services are available there
- Payment method owner and the person who receives budget alerts

## Go/no-go gate

Phase 1 deployment is **no-go** until all of these are true:

- [ ] The Azure subscription is active and its spending behavior is understood.
- [ ] MFA is enabled for the account used to administer the lab.
- [ ] The minimum required Azure roles are confirmed.
- [ ] A supported Azure region is selected.
- [ ] The monthly budget and alert recipient are confirmed.
- [ ] Trial and paid-license expiration or renewal terms are recorded privately.
- [ ] The Windows endpoint is owned, disposable or recoverable, and in scope.

Optional Defender, Entra, and Microsoft 365 connectors do not block Phase 1. Record them
as unavailable when the tenant lacks the required license rather than starting an
unplanned paid trial.

