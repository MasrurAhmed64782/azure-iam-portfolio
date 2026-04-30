# Implementing Risk-Based Conditional Access to Block High-Risk Android Devices from All Cloud Applications

## 🎥 Lab Demo
[▶ Watch on Google Drive](https://drive.google.com/file/d/1dFzlegPbrFD1H6AUTxIYrF-JYTmc1-2O/view?usp=drive_link)

---

## Overview

While some risk-based policies step up authentication with MFA, others require a harder response — blocking access entirely. This lab demonstrates creating a Conditional Access policy that blocks high-risk Android devices and users from accessing any cloud application.

---

## Problem Statement

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
- Opened **Azure Portal → Microsoft Entra ID → Security → Conditional Access → New Policy**

### 2. Configure Users
- **Users:** All Users
- **Excluded:** Main Admin (to prevent admin lockout)

### 3. Configure Target Resources
- **Target Resources:** All Resources *(formerly All Cloud Apps)*

### 4. Configure Conditions
| Condition | Setting |
|-----------|---------|
| User Risk | High |
| Sign-in Risk | High |
| Device Platform | Android |

### 5. Configure Grant Controls
- **Block Access** selected

### 6. Enable and Create
- Policy name: **"Block Android if High Risk"**
- Policy state: **Enabled**
- Verified — policy appears when searching "Block Android if High Risk"

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ Policy Created | "Block Android if High Risk" Conditional Access policy enabled |
| ✅ Android Devices Blocked | High-risk Android sign-ins blocked from all cloud apps |
| ✅ Admin Excluded | Main admin excluded to prevent lockout |
| ✅ All Cloud Apps Protected | Policy covers all resources in the tenant |

---

## Key Concepts

**Block vs. Grant Controls** — For high-risk scenarios, blocking is the appropriate response rather than stepping up with MFA.

**Admin Exclusion** is a critical best practice — always exclude at least one admin account to avoid being locked out of the tenant.

**Defense in Depth** — This policy works alongside the risk-based MFA policy (Lab 04): medium risk triggers MFA, high risk on Android triggers a full block.

---

## References

- [Microsoft Docs — Conditional Access — Block Access](https://learn.microsoft.com/en-us/entra/identity/conditional-access/howto-conditional-access-policy-block-access)
- [Microsoft Docs — Device Platform Condition](https://learn.microsoft.com/en-us/entra/identity/conditional-access/concept-conditional-access-conditions#device-platforms)
