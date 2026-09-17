# IP Address and Naming Plan

- **Version:** 1.0
- **Date:** 2026-09-17
- **Publication rule:** Keep real public addresses and identifying device names out of Git.

## Address plan

The plan reserves RFC 1918 example ranges for the future Phase 2 lab. It does not
require the home LAN to be renumbered during Phase 1.

| Segment | VLAN | IPv4 subnet | Gateway | Intended systems | Default policy |
|---|---:|---|---|---|---|
| Management | 10 | `10.20.10.0/24` | `10.20.10.1` | Proxmox, switch, firewall administration | Administrator devices only |
| Servers | 20 | `10.20.20.0/24` | `10.20.20.1` | AD DS, DNS, application servers | Deny from untrusted segments |
| Endpoints | 30 | `10.20.30.0/24` | `10.20.30.1` | Windows and Linux clients | Required server and internet flows only |
| Security tools | 40 | `10.20.40.0/24` | `10.20.40.1` | Sensors, collectors, management tools | Restricted management access |
| Simulation | 50 | `10.20.50.0/24` | `10.20.50.1` | Authorized test and scenario systems | Isolated; explicit allow rules only |

Reserve `.1` for the gateway, `.2-.49` for infrastructure, `.50-.99` for servers,
`.100-.199` for DHCP clients, and `.200-.254` for temporary lab assignments. Confirm
that `10.20.0.0/16` does not overlap the actual home LAN, VPN, or Tailscale routes before
implementing it. If it overlaps, select another RFC 1918 `/16` and update this file.

## Host naming

Use lowercase in Azure resource names and uppercase Windows computer names.

| Asset | Pattern | Example |
|---|---|---|
| Windows endpoint | `LAB-W11-NN` | `LAB-W11-01` |
| Windows server | `LAB-SRV-NN` | `LAB-SRV-01` |
| Domain controller | `LAB-DC-NN` | `LAB-DC-01` |
| Linux server | `lab-lnx-nn` | `lab-lnx-01` |
| Proxmox node | `lab-pve-nn` | `lab-pve-01` |
| Network device | `lab-net-role-nn` | `lab-net-fw-01` |

## Azure naming

Pattern: `<type>-<project>-<environment>-<region>-<instance>`.

| Resource | Example |
|---|---|
| Resource group | `rg-soclab-dev-centralus-01` |
| Log Analytics workspace | `law-soclab-dev-centralus-01` |
| Data collection rule | `dcr-soclab-winsec-dev-01` |
| Azure Monitor connection | `dce-soclab-dev-centralus-01` |
| Automation rule | `ar-soclab-triage-dev-01` |
| Logic App | `logic-soclab-enrich-dev-01` |

Use the same region token consistently. A globally unique service may require a short,
non-identifying suffix. Do not embed a person's name, email address, tenant ID,
subscription ID, or public IP address in a resource name.

## Required Azure tags

| Tag | Phase 1 value | Purpose |
|---|---|---|
| `project` | `sentinel-soc-lab` | Cost grouping |
| `environment` | `dev` | Environment boundary |
| `owner` | `project-owner` | Sanitized ownership marker |
| `managed-by` | `manual` | Change method; update if IaC is adopted |
| `data-classification` | `lab` | Prevent production or personal data use |
| `expires-on` | ISO date chosen at deployment | Cleanup review trigger |

## DNS and exposure rules

- Use an internal lab DNS suffix selected at Phase 2 deployment; do not use `.local`.
- Do not publish lab administration services to the internet.
- Prefer outbound agent connections and an authenticated VPN for remote administration.
- Record every inter-VLAN allow rule, its owner, reason, and removal condition.

