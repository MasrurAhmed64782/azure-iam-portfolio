# Creating a Dynamic Device Security Group for Windows Devices Using Rule-Based Membership

## Overview

Dynamic groups in Microsoft Entra ID automatically manage their membership based on rules — eliminating manual group maintenance. This lab demonstrates creating a dynamic device group that automatically includes only Windows devices whose names start with "NJ", representing New Jersey devices.

---

## Problem Statement

Manually managing group memberships is time-consuming and error-prone, especially in large organizations. The goal of this lab is to:

- Create a **dynamic device group** that auto-populates based on device attributes
- Target only **Windows devices** with names starting with **"NJ"**
- Eliminate manual membership management through **rule-based automation**

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Azure Portal | Primary interface for all configurations |
| Microsoft Entra ID | Identity and access management platform |
| Dynamic Device Groups | Rule-based automatic group membership |

---

## Key Steps

### 1. Navigate to Groups
- Opened **Azure Portal → Microsoft Entra ID → Groups**
- Clicked **New Group**

### 2. Configure the Group
- Group name: **"New Jersey Windows Devices"**
- Membership type: **Dynamic Device**
- Owner: **Main Admin**

### 3. Configure Dynamic Membership Rules
Two expressions were added to define membership:

**Expression 1 — Device Name Filter:**
| Field | Value |
|-------|-------|
| Property | displayName |
| Operator | Starts With |
| Value | NJ |

**Expression 2 — OS Type Filter:**
| Field | Value |
|-------|-------|
| Property | deviceOSType |
| Operator | Equals |
| Value | Windows |

### 4. Create and Verify
- Group created successfully
- Verified — "New Jersey Windows Devices" appears in the Groups list

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ Dynamic Group Created | "New Jersey Windows Devices" group successfully created |
| ✅ Rule-Based Membership | Group auto-populates based on device name and OS type |
| ✅ Scoped to NJ Windows Devices | Only Windows devices starting with "NJ" qualify |
| ✅ Zero Manual Maintenance | New devices meeting criteria join automatically |

---

## Key Concepts

**Dynamic Device Groups** use attribute-based rules to automatically manage membership. When a device's attributes change (e.g., renamed or OS updated), group membership updates automatically.

**Multi-Expression Rules** allow fine-grained targeting — combining displayName and deviceOSType ensures only the right devices are included, avoiding false positives.

**Practical Use Case** — This group could be used to target Intune device compliance policies, software deployments, or Conditional Access rules specifically at NJ Windows devices.

---

## References

- [Microsoft Docs — Dynamic Membership Rules for Groups](https://learn.microsoft.com/en-us/entra/identity/users/groups-dynamic-membership)
- [Microsoft Docs — Create or Update a Dynamic Group](https://learn.microsoft.com/en-us/entra/identity/users/groups-create-rule)
