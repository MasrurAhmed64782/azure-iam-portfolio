# Deploying a Log Analytics Workspace and Centralizing Microsoft Entra ID Diagnostic Log Collection

## Overview

Security monitoring depends on having all identity logs centralized in one place. This lab demonstrates deploying a Log Analytics Workspace in Azure and connecting Microsoft Entra ID diagnostic logs to it — enabling future querying, alerting, and SIEM integration across the full range of identity event types.

---

## Problem Statement

Without centralized log collection, identity events are siloed and difficult to monitor, investigate, or audit. The goal of this lab is to:

- Deploy a **Log Analytics Workspace** as a centralized log destination
- Configure **Entra ID Diagnostic Settings** to forward all identity logs
- Establish the foundation for **security monitoring and incident response**

---

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Microsoft Azure Portal | Primary interface for all configurations |
| Log Analytics Workspace | Centralized log storage and query engine |
| Microsoft Entra ID Diagnostic Settings | Log forwarding configuration |
| Azure Monitor | Underlying monitoring infrastructure |

---

## Key Steps

### 1. Deploy the Log Analytics Workspace
- Opened **Azure Portal → All Services** → searched **"Log Analytics Workspace"**
- Clicked **Create**
- Created new resource group: **"labsworkspaceRG"**
- Instance name: **"labsworkspace"**
- Region: **East US**
- Validation passed — workspace created successfully

### 2. Configure Entra ID Diagnostic Settings
- Navigated to **Microsoft Entra ID → Diagnostic Settings**
- Clicked **Add Diagnostic Setting**
- Setting name: **"send logsdata"**

### 3. Select Log Categories
The following log categories were enabled:

| Category | Log Type |
|----------|----------|
| Identity | Audit Logs |
| Identity | Sign-in Logs |
| Identity | Non-Interactive User Sign-in Logs |
| Identity | Service Principal Sign-in Logs |
| Identity | Managed Identity Sign-in Logs |
| Identity | Provisioning Logs |
| Identity | ADFS Sign-in Logs |
| Risk | Risky Users |
| Risk | User Risk Events |
| Risk | Risky Service Principals |
| Risk | Service Principal Risk Events |
| Risk | Risky Agents |
| Risk | Agent Risk Events |
| Network | Network Access Traffic Logs |
| Network | Remote Network Health Logs |
| Network | Network Access Alerts |
| Network | Network Access Connection Events |
| Microsoft Graph | Microsoft Graph Activity Logs |
| Microsoft Graph | Azure AD Graph Activity Logs |
| Microsoft Graph | Microsoft Graph Policy Logs |
| Microsoft Graph | Graph Notification Activity Logs |
| Office 365 | Enriched Office 365 Audit Logs |
| AI | Network Access Generative AI Insights |

### 4. Set Destination and Save
- Destination: **Log Analytics Workspace → labsworkspace (East US)**
- Clicked **Save**
- Confirmation received: **Diagnostic settings saved successfully**
- Verified — labsworkspace diagnostic setting confirmed active

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ Workspace Deployed | labsworkspace Log Analytics Workspace created in East US |
| ✅ Resource Group Created | labsworkspaceRG provisioned for organizational management |
| ✅ All Log Categories Enabled | 25+ Entra ID log types forwarded to the workspace |
| ✅ Centralized Monitoring | Single destination for all identity and network access events |
| ✅ SIEM-Ready | Workspace can be connected to Microsoft Sentinel or other SIEMs |

---

## Key Concepts

**Log Analytics Workspace** is the core storage and query engine for Azure Monitor — all forwarded logs can be queried using KQL (Kusto Query Language) for investigation and alerting.

**Diagnostic Settings** in Entra ID control which log categories are forwarded and where — supporting Log Analytics, Storage Accounts, and Event Hubs as destinations.

**Centralized Log Collection** is a foundational requirement for security operations — without it, detecting attack patterns across sign-ins, risk events, and provisioning changes is nearly impossible.

**Future Capabilities** — With logs flowing into the workspace, the next steps include creating KQL queries, setting up alerts, and integrating with Microsoft Sentinel for full SIEM/SOAR capability.

---

## References

- [Microsoft Docs — Log Analytics Workspace Overview](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/log-analytics-workspace-overview)
- [Microsoft Docs — Entra ID Diagnostic Settings](https://learn.microsoft.com/en-us/entra/identity/monitoring-health/howto-configure-diagnostic-settings)
