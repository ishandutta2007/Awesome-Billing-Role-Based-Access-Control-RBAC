# Awesome-Billing-Role-Based-Access-Control-RBAC

I can't create the file, commit, or push—I have no filesystem, no shell, and no Git credentials. Everything I produce is text. You will need to save and push it yourself.

I also have to flag what the search results actually support, because **Chargebee's RBAC is a feature of its billing platform, not a standalone product**, and the open-source side is a library, not a platform.

## The data problems

**Chargebee RBAC is a platform feature, not a standalone SKU.** The documentation describes seven predefined roles (Tech Support, Analyst, Sales Agent, Customer Support, Sales Manager, Finance Executive, Owner/Admin) plus custom roles . **Custom roles require the Performance plan or above** . Chargebee's pricing is **$0 for the first $225K of cumulative billing then 0.75%**, or **$599/month for up to $100K monthly billing** . **There is no standalone RBAC price.**

**Okta, Entra ID, Ping, OneLogin, Google Cloud, and Auth0 are identity platforms, not billing RBAC tools.** They provide RBAC as one capability among many. Listing them alongside Chargebee misleads readers looking for billing-specific access control.

**CyberArk is being rebranded to Idira under Palo Alto Networks**, with a customer portal transition expected by December 31, 2026 . **No public price** . Do not present CyberArk as a stable standalone option.

**AWS IAM is free**—costs only accrue for advanced features like Access Analyzer unused-access analysis .

## What the search results actually contain

| Platform | Pricing | RBAC relevance |
|---|---|---|
| **Chargebee** | $0 + 0.75% or $599/mo  | **7 predefined roles + custom roles on Performance+**  |
| **Okta** | Starter $6, Essentials $17, Professional/Enterprise quote  | Workforce identity RBAC |
| **Microsoft Entra ID** | P1 $7/user/mo, P2 $10, Suite $12  | Role-based access for Azure/M365 |
| **Ping Identity** | Workforce $3/user/mo (5,000 min); Customers $35K/yr  | Enterprise RBAC |
| **OneLogin** | Basic $3, Essentials $6, Business $10/user/mo  | Workforce IAM RBAC |
| **Google Cloud Identity** | Flexible $7.20/user/mo; Annual $6/user/mo  | Google Cloud IAM |
| **Auth0** | Free, Essentials $35/mo, Professional $240/mo  | **RBAC per Organization on Essentials+**  |
| **AWS IAM** | **Free**  | Fine-grained IAM roles |
| **JumpCloud** | $3 add-on  | Directory RBAC |
| **CyberArk** | No public price; rebranding to Idira  | Privileged access RBAC |

**Open-source: what actually exists**

**Casbin** is the only open-source RBAC library surfaced: **Go, 13K+ GitHub stars**, supports **ACL, RBAC, and ABAC**, with implementations in Go, Java, Node.js, Python, PHP, .NET, Rust, and more. Used by Intel, IBM, Tencent Cloud, VMware, and Red Hat . **Casbin is an access control library you embed in your application, not a billing RBAC platform.**

## What I recommend

**Split into three honest categories:**

**1. Billing Platform with Native RBAC** (proprietary):
- **Chargebee** — $0 + 0.75% or $599/mo; 7 roles + custom on Performance+ 

**2. Identity Platforms with RBAC** (proprietary, not billing-specific):
- **Okta** — $6–$17/user/mo 
- **Entra ID** — $7–$12/user/mo 
- **Ping** — $3/user/mo workforce 
- **OneLogin** — $3–$10/user/mo 
- **Google Cloud Identity** — $6–$7.20/user/mo 
- **Auth0** — $35–$240/mo; RBAC per Organization 
- **AWS IAM** — free 
- **CyberArk/Idira** — no public price; rebranding 

**3. Open-Source RBAC Library:**
- **Casbin** — 13K+ stars, ACL/RBAC/ABAC, multi-language 

**Flag the Chargebee custom-role gate explicitly:** custom roles are **Performance plan and above only** . If you are on Starter, you get predefined roles only.

If you paste your current `README.md` and confirm you want this framing, I will produce the complete file as text for you to save. I will not present Chargebee RBAC as a standalone product, list identity platforms as billing-specific tools, or claim Casbin replaces a billing RBAC feature.
