# Cloud — Competitor Deep Research & Product Planning

**Project:** Cloud — Cloud Infrastructure Management Workspace Research  
**Research language:** Easy Hindi (Hinglish)  
**Scope:** Public product research; original product planning only.

## 1. Reference platforms
- AWS Management Console: https://aws.amazon.com/console/
- AWS documentation: https://docs.aws.amazon.com/
- AWS Well-Architected: https://aws.amazon.com/architecture/well-architected/
- Azure Portal: https://portal.azure.com/
- Azure documentation: https://learn.microsoft.com/en-us/azure/
- Azure Architecture Center: https://learn.microsoft.com/en-us/azure/architecture/

## 2. Product purpose
**AWS Management Console** browser-based interface hai jahan AWS services ko search, configure, monitor aur manage kiya ja sakta hai. Services mein compute, storage, networking, databases, identity, security, analytics and monitoring shamil hain.

**Azure Portal** Microsoft Azure resources ko create, configure, organize, monitor aur troubleshoot karne ka web interface hai. Resource groups, subscriptions, dashboards, access control, policies and monitoring important concepts hain.

Dono cloud providers ke products aur naming alag hain. Cloud app ko provider-neutral resource model banana chahiye, lekin provider-specific capabilities ko clearly label karna chahiye.

## 3. AWS Console — major navigation and feature areas
1. Console home and service search
2. Recently visited / favorites
3. Resource Groups and tagging
4. Compute services (for example EC2, containers and serverless)
5. Storage services (for example S3 and block/file storage)
6. Database services
7. Networking and content delivery
8. Identity and Access Management
9. Security services
10. Monitoring and observability
11. Billing, cost and usage
12. CloudFormation / infrastructure as code
13. Support and account settings

Service-specific screens vary widely; the console is a common entry point, not one uniform application.

## 4. Azure Portal — major navigation and feature areas
1. Portal home and global search
2. Dashboard and favorites
3. Subscriptions and resource groups
4. All resources / resource detail
5. Compute and app services
6. Storage accounts
7. Virtual networks and networking
8. Databases
9. Microsoft Entra ID and access management
10. Azure Policy and governance
11. Monitor, metrics, logs and alerts
12. Cost Management and billing
13. Deployment / templates and automation
14. Support and help

Azure resource organization commonly uses management groups, subscriptions, resource groups and resources. Access is controlled through role-based access control and related identity/governance services.

## 5. Cloud — recommended original page map
1. Cloud Overview Dashboard
2. Provider Accounts and Connections
3. Resource Explorer
4. Resource Detail and Activity
5. Compute
6. Storage
7. Databases
8. Networking
9. Identity and Access
10. Security Posture
11. Monitoring and Alerts
12. Cost Explorer and Budgets
13. Infrastructure Templates / Deployments
14. Policy and Governance
15. Backup and Disaster Recovery
16. Change History / Audit
17. Team, Roles and Settings

## 6. Core workflows
### Connect a cloud account
Select provider → start OAuth/role-based connection flow → show exact requested permissions → user grants access → validate account/tenant → import inventory → show last sync and connection health. Avoid asking users to paste long-lived root/admin keys.

### Provision a resource
Choose provider and region → select resource type → fill configuration → validate cost/security/policy → show plan/preview → require approval if policy says so → deploy → track operation → verify resource state.

### Monitor and respond
Connect metrics/log sources → define thresholds → alert → correlate resource/service → assign owner → run approved remediation → verify and audit.

### Cost management
Collect usage/cost data → group by account, project, service, region and tags → compare trends → set budget thresholds → identify idle/oversized resources → propose savings → require approval before changes.

## 7. Essential feature set
- Multi-provider account connection
- Unified inventory with provider-native IDs
- Search, filters, tags and ownership
- Resource health and activity timeline
- Cost and usage explorer
- Budget and anomaly alerts
- Identity and permission review
- Security posture and policy checks
- Deployment templates and change preview
- Monitoring and incident links
- Backup / recovery status
- Audit trail and compliance evidence

## 8. Original differentiator ideas
- **Unified cloud map:** connect resources across providers and show application dependencies.
- **Safe change planner:** preview impact, cost delta, permissions and rollback plan before execution.
- **Cost-to-owner mapping:** identify team/service owner for each cost item using tags and directory mapping.
- **Policy explanation:** translate policy failures into easy language and show a safe fix.
- **Cloud activity story:** resource creation, deployment, incident, cost change and owner action in one timeline.

## 9. Architecture, security and governance
- Use short-lived role-based credentials / OAuth where possible; avoid storing root credentials.
- Keep provider secrets in a managed vault and rotate them.
- Apply least privilege and separate read-only from provisioning permissions.
- Enforce tenant isolation and server-side authorization.
- Every resource action should record actor, account, region, resource ID, request, result and timestamp.
- Destructive operations need preview, approval, confirmation and recovery plan.
- Respect provider API quotas, pagination, eventual consistency and regional differences.
- Clearly label stale inventory and last successful synchronization.
- Use policy-as-code and configuration drift checks carefully; do not auto-remediate without approval.

## 10. Suggested MVP phases
**Phase 1:** Read-only account connection, resource inventory, search, dashboard and sync status.  
**Phase 2:** Cost explorer, monitoring, alerts, access review and audit history.  
**Phase 3:** Policy engine, deployment preview, approved automation, backup/recovery and multi-cloud dependency map.

## 11. Copyright and research boundaries
This is independent product research using public vendor documentation. Do not copy AWS/Azure logos, branding, proprietary text, exact UI layouts or source code. Build an original provider-neutral interface and clearly identify provider-specific actions. Cloud services, prices, permissions and console capabilities change; validate against current official docs before implementation.

## 12. Research source index
- https://aws.amazon.com/console/
- https://docs.aws.amazon.com/
- https://aws.amazon.com/architecture/well-architected/
- https://portal.azure.com/
- https://learn.microsoft.com/en-us/azure/
- https://learn.microsoft.com/en-us/azure/architecture/
