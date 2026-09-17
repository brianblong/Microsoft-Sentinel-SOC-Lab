# Learning and Resource Workflow

This project uses a learn-before-build gate. Hands-on work should reinforce understood concepts rather than substitute for them.

## Milestone learning brief

Before each significant deployment or configuration change, record:

| Field | Description |
|---|---|
| Capability | What will be deployed or changed |
| Why it matters | Operational and SC-200 relevance |
| Concepts to learn first | Required theory and terminology |
| Official resources | Microsoft Learn or authoritative product documentation |
| Supplemental resources | Relevant YouTube videos, courses, labs, or books |
| Readiness check | Questions or a small exercise proving sufficient understanding |
| Risks | Security, cost, privacy, availability, and complexity |
| Rollback | How the change will be reversed safely |

## Resource-selection standard

Recommendations should be small and purposeful rather than long link collections.

- Prefer current official Microsoft Learn and product documentation for Sentinel, Defender, Entra ID, Azure, and SC-200.
- Use vendor documentation for Proxmox, switches, firewalls, Linux, Docker, and third-party tools.
- Treat YouTube and third-party courses as explanatory supplements, not authoritative configuration guidance.
- Check the publication or update date and confirm that the interface and product terminology are still relevant.
- State whether a resource is free or paid and estimate the time required.
- Explain exactly which lesson, chapter, or video section supports the upcoming milestone.
- Do not delay a small lab milestone merely to complete an oversized course.

## Readiness gate

The learner should be able to explain:

1. What the component does and why the lab needs it.
2. What data, permissions, network paths, and costs it introduces.
3. How success will be validated.
4. How to stop, disable, or remove it safely.

If these answers are unclear, pause deployment and complete the targeted prerequisite material first.

## Implementation loop

```text
Learn -> Explain -> Plan -> Deploy -> Validate -> Investigate -> Document -> Improve
```

## Resource record template

```markdown
### Resource title

- Type: Microsoft Learn | Documentation | YouTube | Course | Lab | Book
- Publisher:
- URL:
- Published or updated:
- Cost: Free | Paid
- Estimated time:
- Milestone supported:
- Why it is useful:
- Notes completed:
```
