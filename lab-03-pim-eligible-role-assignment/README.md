# Implementing Just-In-Time Privileged Access Using PIM — Eligible Role Assignment & Self-Activation

## Overview

Permanently assigned privileged roles are a major security risk. Microsoft Entra Privileged Identity Management (PIM) solves this by making users *eligible* for a role rather than permanently assigned — they must explicitly activate it when needed, with justification. This lab demonstrates configuring and activating an eligible role assignment end-to-end.

---

## Problem Statement

Granting permanent administrative roles increases the attack surface of an identity environment. The goal of this lab is to:

- Assign a privileged role as **eligible** (not permanent) to a user
- Require the user to **self-activate** the role with a justification
- Demonstrate **Just-In-Time (JIT)** access — a core Zero Trust principle

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Azure Portal | Primary interface for all configurations |
| Microsoft Entra ID | Identity and access management platform |
| Privileged Identity Management (PIM) | Just-in-time role activation and governance |

---

## Key Steps

### 1. Navigate to Privileged Identity Management
- Opened **Azure Portal → All Services**
- Searched for and opened **Privileged Identity Management**

### 2. Add an Eligible Role Assignment
- Went to **Microsoft Entra Roles → Manage → Roles**
- Clicked **Add Assignments**
- Selected role: **User Administrator**
- Selected member: **Greg Johnson**
- Assignment type: **Eligible**

### 3. Sign In as Greg Johnson & Activate the Role
- Opened a new browser session and signed in as **Greg Johnson**
- Navigated to **Privileged Identity Management → My Roles**
- Located the **User Administrator** eligible role
- Clicked **Activate**
- Entered justification: **"User Creation"**
- Role was successfully activated

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ Eligible Assignment Created | Greg Johnson assigned as eligible for User Administrator |
| ✅ JIT Activation Demonstrated | Role activated on-demand with justification |
| ✅ Zero Standing Privilege | Greg Johnson has no permanent admin access |
| ✅ Audit Trail | Activation reason logged for compliance purposes |

---

## Key Concepts

**Privileged Identity Management (PIM)** enables organizations to manage, control, and monitor access to important resources. Instead of permanent role assignments, users are made *eligible* and must activate the role when needed.

**Just-In-Time (JIT) Access** means privileged access is granted only when needed and for a limited time — dramatically reducing the risk of compromised admin accounts.

**Activation Justification** creates an audit trail explaining why elevated access was requested, supporting compliance and security investigations.

---

## References

- [Microsoft Docs — What is Privileged Identity Management?](https://learn.microsoft.com/en-us/entra/id-governance/privileged-identity-management/pim-configure)
- [Microsoft Docs — Assign Entra Roles in PIM](https://learn.microsoft.com/en-us/entra/id-governance/privileged-identity-management/pim-how-to-add-role-to-user)
