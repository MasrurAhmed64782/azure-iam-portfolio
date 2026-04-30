# Creating a User Account with Job Title, Department & Office Location

## 🎥 Lab Demo
[▶ Watch on Google Drive](https://drive.google.com/file/d/1udlKSlGoqGZrpAX7cybFzPqPBhCFksJR/view?usp=drive_link)

---

## Overview

A core responsibility of any identity administrator is provisioning new user accounts with accurate organizational attributes. This lab demonstrates how to create a new user in Microsoft Entra ID and populate key profile fields including job title, department, and office location.

---

## Problem Statement

When a new employee joins an organization, their identity needs to be created in the directory with accurate job information. This ensures:

- Correct role and department attribution in the directory
- Proper scoping for future access policies and group memberships
- Accurate organizational data for reporting and auditing purposes

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Azure Portal | Primary interface for all configurations |
| Microsoft Entra ID | Identity and access management platform |
| All Users | User provisioning and management interface |

---

## Key Steps

### 1. Navigate to All Users
- Opened the **Azure Portal** → **Microsoft Entra ID**
- Selected **All Users** from the left-hand navigation

### 2. Create a New User
- Clicked **+ New User** → **Create new user**
- Set the **User Type** to **Member**
- Entered the display name: **Mahdi Uddin**

### 3. Populate Job Information
- **Job Title:** Sales Manager
- **Department:** Sales
- **Office Location:** New Jersey

### 4. Review and Create
- Clicked **Review + Create** to finalize the account
- User **Mahdi Uddin** was successfully provisioned in the tenant

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ User Created | Mahdi Uddin successfully added to the Entra ID tenant |
| ✅ User Type Set | Account type set to Member (not Guest) |
| ✅ Job Attributes Populated | Job Title, Department, and Office Location all configured |
| ✅ Directory Accuracy | User profile reflects correct organizational information |

---

## Key Concepts

**User Provisioning** is the process of creating and configuring user accounts in an identity directory. Accurate provisioning ensures that access policies, group memberships, and reporting all function correctly from day one.

**User Type: Member vs Guest** — A *Member* is a full internal user within the tenant. A *Guest* is an external user (e.g., a contractor or partner) with limited access. Setting the correct type at provisioning time is important for access control.

**Organizational Attributes** like department and job title are not just cosmetic — they can be used to drive dynamic group memberships, Conditional Access policies, and access reviews in more advanced configurations.

---

## References

- [Microsoft Docs — Add or Delete Users in Entra ID](https://learn.microsoft.com/en-us/entra/fundamentals/add-users)
- [Microsoft Docs — User Profile Properties](https://learn.microsoft.com/en-us/entra/fundamentals/how-to-manage-user-profile-info)
