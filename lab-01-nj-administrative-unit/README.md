# Creating a Restricted Administrative Unit for NJ & Assigning User Admin Role

## Overview

In many organizations, IT administrators need to manage users across different regions or departments without having access to the entire directory. This lab demonstrates how to use **Administrative Units (AUs)** in Microsoft Entra ID to scope admin permissions to a specific group of users — in this case, the New Jersey region.

---

## Problem Statement

Without Administrative Units, a User Administrator in Entra ID has permissions over **all users** in the tenant. This violates the principle of **least privilege** — a core Zero Trust security concept. The goal of this lab is to:

- Create a dedicated Administrative Unit for the New Jersey region
- Restrict the NJ Admin's permissions so they can **only manage NJ users**
- Prevent the NJ Admin from viewing or modifying users in other regions

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Azure Portal | Primary interface for all configurations |
| Microsoft Entra ID | Identity and access management platform |
| Administrative Units | Scoped management containers for users |
| User Administrator Role | Built-in RBAC role scoped to the AU |

---

## Key Steps

### 1. Navigate to Administrative Units
- Opened the **Azure Portal** → **Microsoft Entra ID**
- Selected **Administrative Units** from the left-hand navigation

### 2. Create the New Jersey Administrative Unit
- Clicked **+ Add** to create a new Administrative Unit
- Named it **"New Jersey"**
- Proceeded through the configuration and clicked **Review + Create**

### 3. Assign the User Administrator Role
- During AU creation, assigned the **User Administrator** role to the **New Jersey Admin** account
- This role is now **scoped exclusively to the NJ AU** — the NJ Admin cannot manage users outside this unit

### 4. Add Members to the AU
- Navigated into the newly created **New Jersey** Administrative Unit
- Added the following members:
  - **Bob Jones**
  - **Greg Johnson**

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ AU Created | "New Jersey" Administrative Unit successfully created in Entra ID |
| ✅ Scoped Role Assigned | NJ Admin granted User Administrator role scoped only to the NJ AU |
| ✅ Members Added | Bob Jones and Greg Johnson added as members of the NJ AU |
| ✅ Least Privilege Enforced | NJ Admin cannot view or manage users outside the NJ Administrative Unit |

---

## Key Concepts

**Administrative Units (AUs)** act like containers within Entra ID. By scoping a role to an AU, you limit that admin's permissions to only the users, groups, or devices inside that container — without any changes to the rest of the tenant.

**Least Privilege Access** is a foundational Zero Trust principle: users and admins should only have the minimum permissions required to do their job. Scoped roles via AUs enforce this at scale.

---

## References

- [Microsoft Docs — Administrative Units in Entra ID](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/administrative-units)
- [Microsoft Docs — User Administrator Role](https://learn.microsoft.com/en-us/entra/identity/role-based-access-control/permissions-reference#user-administrator)
