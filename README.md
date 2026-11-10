# Awesome-Billing-Role-Based-Access-Control-RBAC
# Awesome-Billing-Role-Based-Access-Control-RBAC

## Top Billing Role-Based Access Control (RBAC) Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Fine-Grained Authorization, Billing Role Isolation & Least-Privilege Access Control*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Billing Role-Based Access Control (RBAC)**. These tools help organizations enforce least-privilege access across billing systems, identity providers, and cloud platforms—ensuring finance teams, support agents, and administrators only access the billing data and actions they need.

**Examples** include Chargebee Role-Based Access Control, Okta RBAC, Microsoft Entra ID Roles, CyberArk RBAC, AWS IAM Roles, Ping Identity RBAC, JumpCloud RBAC, OneLogin Roles, Google Cloud IAM, and Auth0 Roles (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosted authorization engines, policy-as-code frameworks, and identity platforms with native RBAC—ideal for SaaS builders, platform engineers, security architects, and developers building transparent, vendor-neutral billing access control.

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The Identity and Access Management (IAM) and Role-Based Access Control (RBAC) market is estimated at approximately **$25.5B–$26.8B in 2025** and projected to reach **$29.3B–$29.7B in 2026** (with core RBAC representing ~$14.3B), expanding at ~11–14% CAGR through 2034. The sector exhibits a **moderately fragmented** market structure: while hyperscalers (Microsoft, AWS, Google) and identity leaders (Okta, CyberArk) hold roughly 30–40% aggregate market share, specialized billing RBAC engines, cloud-native authorization vendors, and niche policy platforms prevent winner-take-all monopolization.

## SaaS/Hosted Platforms

| Platform | Company Valuation / Revenue | Pricing | Free Tier / Free Trial Limits | Description |
| :--- | :--- | :--- | :--- | :--- |
| **[Microsoft Entra ID Roles](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-id)** | ~$3.1T Market Cap (Microsoft) | Paid plans start at $7.00/user/month (P1) or $10.00/user/month (P2) | Free plan included with cloud subscriptions (unlimited users/groups, basic directory features, external identities up to 50,000 monthly active users (MAUs) free); 30-day trial for P1/P2 | Cloud IAM with built-in roles and custom role definitions; role assignments bind security principals to role definitions at specific scopes. |
| **[AWS IAM Roles](https://aws.amazon.com/iam/)** | ~$2.2T Market Cap (Amazon) | $0.00 (Core IAM has no platform cost; pay only for underlying AWS resources accessed) | Free forever (100% free with no monthly expiration or feature cap for standard IAM roles, policies, and users; AWS Free Tier provides 12 months free / Always Free quotas on connected cloud resources) | Identity and access management with identity-based policies, resource-based policies, permission boundaries, and SCPs for fine-grained billing actions. |
| **[Google Cloud IAM](https://cloud.google.com/iam)** | ~$2.1T Market Cap (Alphabet) | $0.00 (Standard Cloud IAM is entirely free; pay only for underlying GCP services consumed) | Free forever (Indefinite free usage with no fees for IAM roles, permissions, or API calls; Cloud Identity Free includes up to 50 user licenses; GCP offers a 90-day $300 trial credit for new accounts) | Cloud IAM with predefined and custom roles, granular billing account permissions (`billing.accounts.*`), and hierarchical policy inheritance. |
| **[Okta RBAC](https://www.okta.com/)** | ~$33.4B Market Cap | Paid Workforce plans start at $6.00/user/month (Starter tier, $1,500/year annual minimum contract) | 30-day free trial limited to up to 10 users per tenant with access to core SSO, MFA, Universal Directory, and up to 5 active workflows | Identity platform with standard admin roles and custom admin roles with granular permissions for least-privilege API access. |
| **[CyberArk RBAC](https://www.cyberark.com/)** | ~$25.0B Acquisition Valuation / ~$20B Market Cap | Standard AWS Marketplace packages start at $149/user/month ($44,712/year for a minimum block of 25 users; enterprise volume contracts scale down to ~$50–$92/user/month) | Guided 30-day Proof of Concept (PoC) / evaluation upon enterprise sales request with partner scoping (no public self-service free tier) | Privileged access management with built-in roles mapped to license types, enforcing separation between billing-relevant privileged operations. |
| **[Auth0 Roles](https://auth0.com/)** | ~$6.5B Acquisition Valuation (Subsidiary of Okta) | Paid B2C plans start at $35/month (up to 500 MAUs); B2B SaaS plans start at $150/month (up to 500 MAUs) | Free forever plan with limit of up to 25,000 Monthly Active Users (MAUs), unlimited social logins, 1 custom domain, and 1 enterprise connection; paid tiers offer 22-day self-serve trial | Identity platform with Authorization Core providing RBAC with roles containing permissions spanning multiple APIs for B2B/SaaS billing. |
| **[Chargebee Role-Based Access Control](https://www.chargebee.com/)** | ~$3.5B Valuation | Performance plan starts at $599/month (billed annually at $7,188/year for up to $100k/mo MRR + 0.75% overage) | Free Starter tier covers up to $250,000 in cumulative lifetime billing (0.75% overage fee thereafter); offers 14-day fully-featured free trial | Subscription billing platform with predefined and CSV-configured custom roles covering Customers, Subscriptions, and Product Catalog. |
| **[Ping Identity RBAC](https://www.pingidentity.com/)** | ~$2.8B Acquisition Valuation (Thoma Bravo) | Workforce Essential plan starts at $3/user/month (requires mandatory minimum 5,000 users = $180,000/year contract floor); CIAM starts at $35,000/year | Guided 30-day sandbox / enterprise evaluation trial upon sales request; no perpetual free tier | Enterprise identity platform with internal authorization roles grantable via REST or admin UI, supporting conditional role grants for billing workflows. |
| **[JumpCloud RBAC](https://jumpcloud.com/)** | ~$2.6B Valuation | Standalone SSO & MFA starts at $11/user/month ($13 monthly); Device Identity starts at $13/user/month | 30-day free trial with full feature and device access (legacy accounts created prior to Feb 1, 2024 have 10 users / 10 devices free forever) | Cloud directory platform with admin/sudo permission management, user groups, and temporary elevated privileges for time-bound billing access. |
| **[OneLogin Roles](https://www.onelogin.com/)** | ~$500M+ Acquisition Valuation (One Identity) | Essentials tier starts at $3/user/month; Advanced/Business starts at $4–$6/user/month | 30-day free trial sandbox for administrative testing and policy configuration (up to 25 test users) | Identity platform structuring roles as collections of apps to simplify billing system access provisioning and automated deprovisioning. |

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
