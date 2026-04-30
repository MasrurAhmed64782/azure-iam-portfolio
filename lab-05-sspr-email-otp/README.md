# Enabling Self-Service Password Reset (SSPR) and Configuring Email OTP as an Authentication Method

## Overview

Self-Service Password Reset (SSPR) empowers users to reset their own passwords without contacting the helpdesk — reducing IT overhead and improving user experience. This lab demonstrates enabling SSPR for all users and configuring Email OTP as a supported authentication method.

---

## Problem Statement

Without SSPR, users who forget their passwords must contact IT support, creating delays and increasing helpdesk costs. The goal of this lab is to:

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
| Email OTP | One-time passcode delivered via email for verification |

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

**Self-Service Password Reset (SSPR)** allows users to reset their passwords independently using pre-registered verification methods. This is a critical feature for reducing IT support costs and improving productivity.

**Email OTP** delivers a one-time passcode to the user's registered email address, providing a simple and accessible verification method that works without a smartphone or authenticator app.

**Authentication Methods Policy** in Entra ID centrally controls which verification methods are available to users across SSPR, MFA, and passwordless sign-in scenarios.

---

## References

- [Microsoft Docs — How SSPR Works](https://learn.microsoft.com/en-us/entra/identity/authentication/concept-sspr-howitworks)
- [Microsoft Docs — Authentication Methods — Email OTP](https://learn.microsoft.com/en-us/entra/identity/authentication/concept-authentication-email-otp)
