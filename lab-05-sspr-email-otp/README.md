# Enabling Self-Service Password Reset (SSPR) and Configuring Email OTP as an Authentication Method

## 🎥 Lab Demo
[▶ Watch on Google Drive](https://drive.google.com/file/d/1hlQxYZtM7MLR-08QS6XeVV-qVCLkiHnv/view?usp=drive_link)

---

## Overview

Self-Service Password Reset (SSPR) empowers users to reset their own passwords without contacting the helpdesk. This lab demonstrates enabling SSPR for all users and configuring Email OTP as a supported authentication method.

---

## Problem Statement

- Enable **SSPR for all users** in the tenant
- Configure **Email OTP** as a supported verification method
- Reduce helpdesk dependency while maintaining secure identity verification

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Azure Portal | Primary interface for all configurations |
| Microsoft Entra ID | Identity and access management platform |
| Self-Service Password Reset (SSPR) | User-driven password recovery |
| Email OTP | One-time passcode delivered via email |

---

## Key Steps

### 1. Enable Self-Service Password Reset
- Opened **Azure Portal → Microsoft Entra ID → Password Reset**
- Set SSPR to **All** — enabled for all users in the tenant

### 2. Configure Email OTP as Authentication Method
- Navigated to **Security → Authentication Methods**
- Selected **Email OTP**
- Enabled Email OTP for all users
- Clicked **Save**
- Received confirmation: **Policy successfully saved**

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ SSPR Enabled | All users can now reset their own passwords |
| ✅ Email OTP Configured | Email OTP added as a supported authentication method |
| ✅ Policy Saved | Confirmation received — settings applied successfully |
| ✅ Helpdesk Burden Reduced | Users no longer need IT intervention for password resets |

---

## Key Concepts

**Self-Service Password Reset (SSPR)** allows users to reset their passwords independently using pre-registered verification methods.

**Email OTP** delivers a one-time passcode to the user's registered email address — a simple and accessible verification method that works without a smartphone.

---

## References

- [Microsoft Docs — How SSPR Works](https://learn.microsoft.com/en-us/entra/identity/authentication/concept-sspr-howitworks)
- [Microsoft Docs — Authentication Methods — Email OTP](https://learn.microsoft.com/en-us/entra/identity/authentication/concept-authentication-email-otp)
