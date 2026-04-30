# Implementing Risk-Based Conditional Access to Block High-Risk Android Devices from All Cloud Applications

## Overview

While some risk-based policies step up authentication with MFA, others require a harder response — blocking access entirely. This lab demonstrates creating a Conditional Access policy that blocks high-risk Android devices and users from accessing any cloud application, while excluding the admin account to prevent lockout.

---

## Problem Statement

Android devices present a unique risk surface — they may be unmanaged, rooted, or compromised. Combined with high user or sign-in risk signals, access from these devices should be blocked entirely. The goal of this lab is to:

- **Block all access** from Android devices when high risk is detected
- Apply the policy to **all cloud applications**
- **Exclude the admin account** to prevent accidental lockout

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Azure Portal | Primary interface for all configurations |
| Microsoft Entra ID | Identity and access management platform |
| Conditional Access | Policy-based access control engine |
| Entra ID Protection | Risk signal source |

---

## Key Steps

### 1. Navigate to Conditional Access
- Opened **Azure Portal → Microsoft Entra ID → Security → Conditional Access**
- Clicked **New Policy**

### 2. Configure Users
- **Users:** All Users
- **Excluded:** Main Admin (to prevent admin lockout)

### 3. Configure Target Resources
- **Target Resources:** All Resources *(formerly known as All Cloud Apps)*

### 4. Configure Conditions
| Condition | Setting |
|-----------|---------|
| User Risk | High |
| Sign-in Risk | High |
| Device Platform | Android |

### 5. Configure Grant Controls
- **Block Access** selected

### 6. Enable and Create the Policy
- Policy name: **"Block Android if High Risk"**
- Policy state: **Enabled**
- Clicked **Create**
- Verified — policy appears when searching "Block Android if High Risk"

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ Policy Created | "Block Android if High Risk" Conditional Access policy enabled |
| ✅ Android Devices Blocked | High-risk Android sign-ins blocked from all cloud apps |
| ✅ Admin Excluded | Main admin excluded to prevent lockout |
| ✅ All Cloud Apps Protected | Policy covers all resources in the tenant |
| ✅ Verified | Policy confirmed active in Conditional Access policies list |

---

## Key Concepts

**Block vs. Grant Controls** — Conditional Access policies can either grant access (with or without conditions like MFA) or block it entirely. For high-risk scenarios, blocking is the appropriate response.

**Admin Exclusion** is a critical best practice when creating blocking policies — always exclude at least one break-glass or admin account to avoid being locked out of the tenant.

**Platform-Specific Policies** allow organizations to apply different security postures to different device types — Android, iOS, Windows, and macOS can each have tailored policies.

**Defense in Depth** — This policy works alongside risk-based MFA policies (Lab 04) to create layered protection: medium risk triggers MFA, high risk on Android triggers a full block.

---

## References

- [Microsoft Docs — Conditional Access — Block Access](https://learn.microsoft.com/en-us/entra/identity/conditional-access/howto-conditional-access-policy-block-access)
- [Microsoft Docs — Device Platform Condition](https://learn.microsoft.com/en-us/entra/identity/conditional-access/concept-conditional-access-conditions#device-platforms)
