# Restricting External Guest Collaboration to an Approved Domain Using Entra External Identities

## 🎥 Lab Demo
[▶ Watch on Google Drive](https://drive.google.com/file/d/1cGMqbUHEk7BzzIyBZ3H5pYGcUk0QkyvR/view?usp=drive_link)

---

## Overview

By default, Microsoft Entra ID allows guest invitations to any external email domain. This lab demonstrates how to restrict external collaboration to a single approved domain, ensuring guest access is only extended to trusted partner organizations.

---

## Problem Statement

- Restrict external collaboration **only to an approved domain**
- Prevent guest invitations from being sent to any other domain
- Enforce an **allowlist-based collaboration model**

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Entra Admin Center | Primary interface for external identity configuration |
| External Identities | Guest access and B2B collaboration settings |
| External Collaboration Settings | Domain restriction configuration |

---

## Key Steps

### 1. Navigate to External Collaboration Settings
- Opened **Entra Admin Center → External Identities → External Collaboration Settings**

### 2. Configure Collaboration Restrictions
- Selected: **"Allow invitations only to the specified domains"**
- Entered approved domain: **theboringcompany.com**

### 3. Save Settings
- Clicked **Save**
- Confirmation: **External collaboration settings updated successfully**

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ Domain Allowlist Configured | Only theboringcompany.com can receive guest invitations |
| ✅ All Other Domains Blocked | Invitations to any other domain will be rejected |
| ✅ Settings Saved | Policy applied successfully |
| ✅ Data Governance Enforced | External sharing restricted to trusted partner only |

---

## Key Concepts

**Allowlist vs. Blocklist Model:**
- *Allow only specified domains* — strictest option; only listed domains can be invited (used in this lab)
- *Block specified domains* — all domains allowed except listed ones
- *Allow all domains* — default, no restrictions

**B2B Collaboration** in Entra ID allows external users to sign in with their own credentials while accessing your organization's resources.

---

## References

- [Microsoft Docs — External Collaboration Settings](https://learn.microsoft.com/en-us/entra/external-id/external-collaboration-settings-configure)
- [Microsoft Docs — Allow or Block Domains for B2B](https://learn.microsoft.com/en-us/entra/external-id/allow-deny-list)
