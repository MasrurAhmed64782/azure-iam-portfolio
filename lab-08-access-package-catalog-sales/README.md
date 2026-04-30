# Configuring an Identity Governance Access Package and Catalog for Sales Team Entitlement Management

## 🎥 Lab Demo
[▶ Watch on Google Drive](https://drive.google.com/file/d/140yyDUO2MiEl5MIkhgsxhxUJdEHIJk6S/view?usp=drive_link)

---

## Overview

Microsoft Entra Entitlement Management allows organizations to automate access request workflows. This lab demonstrates creating an access catalog and package that allows sales team members to request access to sales resources through self-service.

---

## Problem Statement

- Create a **catalog** to organize sales-related resources
- Build an **access package** that bundles resource access into a single requestable unit
- Enable **self-service access requests** with a defined approver

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Azure Portal | Primary interface for all configurations |
| Microsoft Entra ID | Identity and access management platform |
| Identity Governance | Entitlement Management feature set |
| Access Packages | Bundled resource access units |
| Catalogs | Containers for organizing access packages |

---

## Key Steps

### 1. Create the Sales Catalog
- Opened **Azure Portal → Microsoft Entra ID → Identity Governance → Catalogs**
- Catalog name: **"Sales Catalog"** — created successfully

### 2. Create the Access Package
- Navigated to **Access Packages → New Access Package**
- Package name: **"Sales Project Package"**
- Catalog: **Sales Catalog**

### 3. Configure Resource Roles
- **Groups & Teams:** Sales Project Users → Role: **Member**
- **SharePoint Site:** Sales Project Users → Role: **Sales Project Users Members**

### 4. Configure Request Settings
- Who can request: **Users, service principals, and agent identities in your directory**
- Requestor: **Sales Employee**
- Request type: **Self-service**
- Fallback approver: **Main Admin**

### 5. Create and Verify
- Access package created successfully
- Verified — "Sales Project Package" appears in the Access Packages list

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ Catalog Created | "Sales Catalog" successfully created in Identity Governance |
| ✅ Access Package Created | "Sales Project Package" bundling group and SharePoint access |
| ✅ Self-Service Enabled | Sales employees can request access without IT involvement |
| ✅ Approver Configured | Main Admin set as fallback approver |

---

## Key Concepts

**Entitlement Management** automates the access request, approval, and expiration lifecycle — reducing manual provisioning and ensuring access is granted consistently.

**Access Packages** bundle multiple resource roles into a single requestable unit — users request one package and get all necessary access automatically.

---

## References

- [Microsoft Docs — What is Entitlement Management?](https://learn.microsoft.com/en-us/entra/id-governance/entitlement-management-overview)
- [Microsoft Docs — Create an Access Package](https://learn.microsoft.com/en-us/entra/id-governance/entitlement-management-access-package-create)
