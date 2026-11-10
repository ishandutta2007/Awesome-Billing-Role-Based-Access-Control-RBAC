# Awesome-Billing-Role-Based-Access-Control-RBAC
# Awesome-Billing-Role-Based-Access-Control-RBAC

# Top Billing Role-Based Access Control (RBAC) Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Fine-Grained Authorization, Billing Role Isolation & Least-Privilege Access Control*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Billing Role-Based Access Control (RBAC)**. These tools help organizations enforce least-privilege access across billing systems, identity providers, and cloud platforms—ensuring finance teams, support agents, and administrators only access the billing data and actions they need.

**Examples** include Chargebee Role-Based Access Control, Okta RBAC, Microsoft Entra ID Roles, CyberArk RBAC, AWS IAM Roles, Ping Identity RBAC, JumpCloud RBAC, OneLogin Roles, Google Cloud IAM, and Auth0 Roles (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosted authorization engines, policy-as-code frameworks, and identity platforms with native RBAC—ideal for SaaS builders, platform engineers, security architects, and developers building transparent, vendor-neutral billing access control.

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Chargebee Role-Based Access Control](https://www.chargebee.com/)**  
  Billing platform with predefined roles (Tech Support, Analyst, Sales Agent, Customer Support, Sales Manager, Finance Executive) and custom role support via CSV-based privilege configuration for modules including Customers, Subscriptions, and Product Catalog; explicit deny takes precedence when multiple roles are assigned [citation:1][citation:13].

- **[Okta RBAC](https://www.okta.com/)**  
  Identity platform with standard admin roles (ORG_ADMIN, APP_ADMIN, USER_ADMIN, READ_ONLY_ADMIN, etc.) and custom admin roles with granular permissions; IAM-based standard roles provide immutable preset permission sets for least-privilege API access [citation:2].

- **[Microsoft Entra ID Roles](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-id)**  
  Cloud IAM with built-in roles and custom role definitions; role assignments bind security principals (users, groups, service principals) to role definitions at specific scopes (tenant, administrative unit, or individual resource) [citation:3].

- **[CyberArk RBAC](https://www.cyberark.com/)**  
  Privileged access management with built-in roles (Privilege Cloud Administrators, Auditors, Safe Managers, Users, Session Risk Managers) mapped to license types; role-based access enforces separation between billing-relevant privileged actions [citation:4].

- **[AWS IAM Roles](https://aws.amazon.com/iam/)**  
  Identity and access management with identity-based policies, resource-based policies, permission boundaries, and service control policies (SCPs); policies define allowed actions, resources, and conditions for billing and cost management access [citation:5].

- **[Ping Identity RBAC](https://www.pingidentity.com/)**  
  Identity platform with internal authorization roles grantable via REST or admin UI; supports conditional role grants and fine-grained authorization policies for protecting billing-related workflows [citation:6].

- **[JumpCloud RBAC](https://jumpcloud.com/)**  
  Directory platform with admin/sudo permission management via user groups and device groups; supports temporary elevated privileges with automatic revocation for time-bound billing system access [citation:7].

- **[OneLogin Roles](https://www.onelogin.com/)**  
  Identity platform where roles are collections of apps; users assigned to roles gain access to all included applications, simplifying billing system access provisioning and deprovisioning .

- **[Google Cloud IAM](https://cloud.google.com/iam)**  
  Cloud IAM with predefined and custom roles, including granular permissions for billing accounts (e.g., `billing.accounts.getIamPolicy`, `billing.budgets.list`); supports resource hierarchy and policy inheritance [citation:9].

- **[Auth0 Roles](https://auth0.com/)**  
  Identity platform with Authorization Core providing RBAC with roles containing permissions from multiple APIs; recommended over the legacy Authorization Extension for performance and scalability in B2B/SaaS billing scenarios [citation:10].

## Open-Source GitHub Projects

- **[Casbin](https://github.com/casbin/casbin)**  
  Open-source authorization library supporting ACL, RBAC, ABAC, and custom models across Go, Java, Node.js, Python, PHP, .NET, Rust, and more; 13k+ GitHub stars with middleware integrations for popular web frameworks [citation:17].

- **[Casdoor](https://github.com/casdoor/casdoor)**  
  Open-source IAM/SSO platform with web UI supporting OAuth 2.0, OIDC, SAML, CAS, LDAP, and RBAC; multi-tenancy via organizations with per-organization users, applications, and roles [citation:21][citation:26].

- **[Keycloak](https://github.com/keycloak/keycloak)**  
  Open-source identity and access management with RBAC, fine-grained admin permissions (FGAP V2), and authorization services; supports realms, groups, and role mappings for billing system access control [citation:21][citation:29].

- **[ZITADEL](https://github.com/zitadel/zitadel)**  
  Open-source identity platform built on event sourcing with OIDC, SAML, and RBAC; provides audit trails for compliance and multi-instance isolation for tenant-specific billing access [citation:21].

- **[Permify](https://github.com/Permify/permify)**  
  Open-source authorization-as-a-service inspired by Google Zanzibar; supports RBAC, ReBAC, and ABAC with sub-10ms access checks and multi-tenant isolation for billing authorization logic [citation:25].

- **[go-iam](https://github.com/melvinodsa/go-iam)**  
  Lightweight multi-tenant IAM server in Go with RBAC, custom roles, resource grouping, and OAuth provider integration (Google, Microsoft, GitHub); includes React admin UI [citation:11].

- **[wardn](https://github.com/MogRex-Limited/wardn)**  
  Opinionated authorization library for Go with policy-file-defined permissions, roles, and scope hierarchy; includes built-in privilege escalation protection for role creation and assignment [citation:15].

- **[OPA (Open Policy Agent)](https://github.com/open-policy-agent/opa)**  
  Policy-as-code engine using Rego language for fine-grained authorization; supports multi-dimensional access control (WHO, WHAT, WHEN, WHERE, WHY) and audit logging for billing API access decisions [citation:18][citation:23].

### Additional Strong Open-Source Options

- **[Ory Keto](https://github.com/ory/keto)** for Zanzibar-style relationship-based access control with REST API.
- **[OpenFGA](https://github.com/openfga/openfga)** for fine-grained authorization inspired by Google Zanzibar, with SDKs and a playground.
- **[Cerbos](https://github.com/cerbos/cerbos)** for policy-as-code authorization with YAML-based policies and language-agnostic SDKs.
- **Apache Casbin ecosystem** including Casbin Server (CaaS), adapters for PostgreSQL/MongoDB/Redis, and middleware for Caddy, Envoy, and Istio [citation:22].

**Frameworks for building custom systems**: Combine **Casbin** for embedded authorization logic, **Keycloak** or **Casdoor** for identity and role management, and **OPA** for policy-as-code billing access decisions—integrated with **Stripe Billing** or **Chargebee** webhooks for real-time permission enforcement.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- RBAC implementations for billing must enforce separation of duties (e.g., invoice creation vs. refund approval) and comply with financial controls (SOX, PCI DSS where applicable).
- Self-hosted open-source authorization engines require careful policy design, regular access reviews, and audit logging to prevent privilege creep.

---

**Made for SaaS finance engineers, platform security teams, identity architects, and developers building billing access control.**  
Let's make billing RBAC more open, granular, and auditable.
