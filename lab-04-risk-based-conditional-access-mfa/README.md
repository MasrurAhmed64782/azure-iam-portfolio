# Configuring Risk-Based Conditional Access with MFA Enforcement Using Microsoft Entra ID Protection

## Overview

Microsoft Entra ID Protection uses machine learning to detect risky sign-ins and compromised users. This lab demonstrates how to create a risk-based Conditional Access policy that automatically requires Multi-Factor Authentication (MFA) when medium or high risk is detected — protecting the organization without disrupting low-risk users.

---

## Problem Statement

Not all sign-ins carry the same risk. Requiring MFA for every login adds friction, but allowing high-risk sign-ins without additional verification is dangerous. The goal of this lab is to:

- Enforce MFA **only when risk is detected** (medium or high)
- Apply the policy to **all users** across the tenant
- Leverage **Entra ID Protection** signals for intelligent, automated enforcement

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Azure Portal | Primary interface for all configurations |
| Microsoft Entra ID Protection | Risk detection and signal generation |
| Conditional Access | Policy engine for access control |
| Multi-Factor Authentication (MFA) | Step-up authentication enforcement |

---

## Key Steps

### 1. Navigate to ID Protection
- Opened **Microsoft Entra Portal → ID Protection**
- Went to **Risk-Based Conditional Access**

### 2. Create a New Policy
- Clicked **New Policy**
- **Users:** All Users
- **Conditions — User Risk:** Configured → set to **Medium and High**
- **Conditions — Sign-in Risk:** Configured → set to **Medium and High**

### 3. Configure Grant Controls
- **Grant Access** selected
- Required: **Multi-Factor Authentication**

### 4. Enable and Create the Policy
- Policy name: **"Medium or High Risk Require MFA Entra ID"**
- Policy state: **Enabled**
- Clicked **Create**
- Verified — policy appears when searched in the Conditional Access policies list

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ Policy Created | Risk-based Conditional Access policy successfully enabled |
| ✅ MFA Enforced on Risk | MFA required automatically for medium/high risk events |
| ✅ All Users Covered | Policy applies tenant-wide |
| ✅ Verified | Policy confirmed active in Conditional Access policies list |

---

## Key Concepts

**Entra ID Protection** continuously evaluates sign-in and user risk using signals like leaked credentials, impossible travel, anonymous IP addresses, and more.

**Risk-Based Conditional Access** allows organizations to automate responses to detected risk — stepping up authentication requirements rather than simply blocking access, reducing user friction while maintaining security.

**Medium and High Risk Thresholds** balance security and usability — low-risk sign-ins proceed normally while suspicious activity triggers MFA.

---

## References

- [Microsoft Docs — What is Entra ID Protection?](https://learn.microsoft.com/en-us/entra/id-protection/overview-identity-protection)
- [Microsoft Docs — Risk-Based Conditional Access Policies](https://learn.microsoft.com/en-us/entra/id-protection/howto-identity-protection-configure-risk-policies)
