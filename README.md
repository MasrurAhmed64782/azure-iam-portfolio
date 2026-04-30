# Azure Entra ID — IAM Lab Portfolio

A collection of hands-on Identity & Access Management (IAM) labs performed in Microsoft Azure Entra ID. This repository documents real-world IAM configurations including Administrative Units, Conditional Access Policies, Privileged Identity Management, Identity Governance, and Security Monitoring.

> **Author:** Masrur Ahmed  
> **Platform:** Microsoft Azure / Entra ID  
> **Focus:** Identity Governance, Access Control, Zero Trust Principles

---

## Labs

| # | Lab Title | Key Concepts |
|---|-----------|--------------|
| 01 | [Creating a Restricted AU for NJ & Assigning User Admin Role](./lab-01-nj-administrative-unit/README.md) | Administrative Units, Scoped RBAC, Role Assignment |
| 02 | [Creating a User Account with Job Title, Department & Office Location](./lab-02-create-user-mahdi-uddin/README.md) | User Provisioning, Member Accounts, Organizational Attributes |
| 03 | [Implementing Just-In-Time Privileged Access Using PIM](./lab-03-pim-eligible-role-assignment/README.md) | PIM, Eligible Role Assignment, JIT Access |
| 04 | [Configuring Risk-Based Conditional Access with MFA Enforcement](./lab-04-risk-based-conditional-access-mfa/README.md) | ID Protection, Risk-Based Policy, MFA |
| 05 | [Enabling SSPR and Configuring Email OTP Authentication](./lab-05-sspr-email-otp/README.md) | SSPR, Email OTP, Authentication Methods |
| 06 | [Enabling QR Code Authentication and Enforcing MFA via Conditional Access](./lab-06-qr-code-mfa-conditional-access/README.md) | QR Code Auth, Conditional Access, MFA Baseline |
| 07 | [Creating a Dynamic Device Security Group Using Rule-Based Membership](./lab-07-dynamic-device-security-group/README.md) | Dynamic Groups, Device Attributes, Rule-Based Membership |
| 08 | [Configuring an Access Package and Catalog for Sales Team Entitlement Management](./lab-08-access-package-catalog-sales/README.md) | Identity Governance, Entitlement Management, Access Packages |
| 09 | [Implementing Risk-Based Conditional Access to Block High-Risk Android Devices](./lab-09-block-high-risk-android-conditional-access/README.md) | Conditional Access, Block Policy, Device Platform |
| 10 | [Restricting External Guest Collaboration to an Approved Domain](./lab-10-external-collaboration-domain-restriction/README.md) | External Identities, B2B Collaboration, Domain Allowlist |
| 11 | [Deploying a Log Analytics Workspace and Centralizing Entra ID Diagnostic Logs](./lab-11-log-analytics-workspace-diagnostics/README.md) | Log Analytics, Diagnostic Settings, Security Monitoring |

---

## Skills Demonstrated

- Creating and managing **Administrative Units** with scoped RBAC
- Provisioning users with accurate **organizational attributes**
- Implementing **Just-In-Time privileged access** with PIM
- Configuring **risk-based and baseline Conditional Access** policies
- Enabling **SSPR, Email OTP, and QR Code** authentication methods
- Building **dynamic device groups** with attribute-based rules
- Managing **entitlement and access packages** via Identity Governance
- Blocking high-risk access with **platform-specific Conditional Access**
- Restricting **external B2B collaboration** to approved domains
- Centralizing **identity diagnostic logs** with Log Analytics

---

## Repository Structure

```
azure-iam-portfolio/
├── README.md
├── lab-01-nj-administrative-unit/
│   └── README.md
├── lab-02-create-user-mahdi-uddin/
│   └── README.md
├── lab-03-pim-eligible-role-assignment/
│   └── README.md
├── lab-04-risk-based-conditional-access-mfa/
│   └── README.md
├── lab-05-sspr-email-otp/
│   └── README.md
├── lab-06-qr-code-mfa-conditional-access/
│   └── README.md
├── lab-07-dynamic-device-security-group/
│   └── README.md
├── lab-08-access-package-catalog-sales/
│   └── README.md
├── lab-09-block-high-risk-android-conditional-access/
│   └── README.md
├── lab-10-external-collaboration-domain-restriction/
│   └── README.md
└── lab-11-log-analytics-workspace-diagnostics/
    └── README.md
```
