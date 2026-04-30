# Deploying a Log Analytics Workspace and Centralizing Microsoft Entra ID Diagnostic Log Collection

## 🎥 Lab Demo
[▶ Watch on Google Drive](https://drive.google.com/file/d/1ok0m33LV_g6AHDO1tWQtw17YWblZL7ae/view?usp=drive_link)

---

## Overview

Security monitoring depends on having all identity logs centralized in one place. This lab demonstrates deploying a Log Analytics Workspace in Azure and connecting Microsoft Entra ID diagnostic logs to it — enabling future querying, alerting, and SIEM integration.

---

## Problem Statement

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
- Opened **Azure Portal → All Services → Log Analytics Workspace**
- Created new resource group: **"labsworkspaceRG"**
- Instance name: **"labsworkspace"**
- Region: **East US**
- Workspace created successfully

### 2. Configure Entra ID Diagnostic Settings
- Navigated to **Microsoft Entra ID → Diagnostic Settings → Add Diagnostic Setting**
- Setting name: **"send logsdata"**

### 3. Selected Log Categories

| Category | Log Type |
|----------|----------|
| Identity | Audit Logs, Sign-in Logs, Non-Interactive User Sign-in Logs |
| Identity | Service Principal Sign-in Logs, Managed Identity Sign-in Logs |
| Identity | Provisioning Logs, ADFS Sign-in Logs |
| Risk | Risky Users, User Risk Events, Risky Service Principals |
| Risk | Service Principal Risk Events, Risky Agents, Agent Risk Events |
| Network | Network Access Traffic Logs, Remote Network Health Logs |
| Network | Network Access Alerts, Network Access Connection Events |
| Microsoft Graph | Graph Activity Logs, Azure AD Graph Activity Logs |
| Microsoft Graph | Graph Policy Logs, Graph Notification Activity Logs |
| Office 365 | Enriched Office 365 Audit Logs |
| AI | Network Access Generative AI Insights |

### 4. Set Destination and Save
- Destination: **labsworkspace (East US)**
- Clicked **Save** — diagnostic settings saved successfully
- Verified — labsworkspace diagnostic setting confirmed active

---

## Outcome

| Result | Details |
|--------|---------|
| ✅ Workspace Deployed | labsworkspace Log Analytics Workspace created in East US |
| ✅ Resource Group Created | labsworkspaceRG provisioned |
| ✅ All Log Categories Enabled | 25+ Entra ID log types forwarded to the workspace |
| ✅ Centralized Monitoring | Single destination for all identity and network access events |
| ✅ SIEM-Ready | Workspace can be connected to Microsoft Sentinel |

---

## Key Concepts

**Log Analytics Workspace** is the core storage and query engine for Azure Monitor — all forwarded logs can be queried using KQL (Kusto Query Language).

**Centralized Log Collection** is a foundational requirement for security operations — without it, detecting attack patterns across sign-ins, risk events, and provisioning changes is nearly impossible.

**Future Capabilities** — With logs flowing into the workspace, next steps include KQL queries, alerts, and Microsoft Sentinel integration for full SIEM/SOAR capability.

---

## References

- [Microsoft Docs — Log Analytics Workspace Overview](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/log-analytics-workspace-overview)
- [Microsoft Docs — Entra ID Diagnostic Settings](https://learn.microsoft.com/en-us/entra/identity/monitoring-health/howto-configure-diagnostic-settings)
