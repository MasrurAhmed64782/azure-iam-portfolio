# Enabling QR Code Authentication and Enforcing MFA for All Users via Conditional Access

## Overview

This lab covers two complementary identity security configurations: enabling QR code as a modern passwordless authentication method, and creating a Conditional Access policy that enforces MFA across all users in the tenant — ensuring a strong authentication baseline regardless of risk level.

---

## Problem Statement

Organizations need to balance strong authentication with usability. The goals of this lab are to:

- Enable **QR Code** as a modern, frictionless authentication method
- Enforce **MFA for all users** via Conditional Access as a security baseline
- Ensure no user can access resources without strong authentication

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Azure Portal | Primary interface for all configurations |
| Microsoft Entra ID | Identity and access management platform |
| Authentication Methods | QR Code configuration |
| Conditional Access | Tenant-wide MFA enforcement policy |

---

## Key Steps

### 1. Enable QR Code Authentication
- Opened **Azure Portal → Microsoft Entra ID → Security → Authentication Methods**
- Selected **QR Code**
- Enabled for **All Users**
- Clicked **Save** — authentication method saved successfully

### 2. Create MFA for All Conditional Access Policy
- Navigated to **Security → Conditional Access**
- Clicked **New Policy**
- Policy name: **"MFA for All"**
- **Users:** All Users
- **Grant:** Grant Access → **Require Multi-Factor Authentication**
- Policy state: **Enabled**
- Clicked **Create**
- Verified — policy appears when searching "MFA for All" in the policies list

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ QR Code Enabled | QR Code authentication available for all users |
| ✅ MFA Policy Created | "MFA for All" Conditional Access policy active |
| ✅ Tenant-Wide Coverage | All users required to use MFA to access resources |
| ✅ Verified | Both configurations confirmed active |

---

## Key Concepts

**QR Code Authentication** is a modern passwordless method where users scan a QR code with the Microsoft Authenticator app to sign in — improving usability particularly for shared or frontline worker devices.

**Baseline MFA Policy** via Conditional Access is a security best practice recommended by Microsoft. Requiring MFA for all users dramatically reduces the risk of account compromise from phishing and credential theft.

**Defense in Depth** — combining a new authentication method (QR code) with an enforcement policy (MFA for All) demonstrates layered identity security.

---

## References

- [Microsoft Docs — QR Code Authentication](https://learn.microsoft.com/en-us/entra/identity/authentication/concept-authentication-qr-code)
- [Microsoft Docs — Conditional Access — Require MFA](https://learn.microsoft.com/en-us/entra/identity/conditional-access/howto-conditional-access-policy-all-users-mfa)
