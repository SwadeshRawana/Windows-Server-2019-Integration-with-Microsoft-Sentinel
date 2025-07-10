# Windows-Server-2019-Integration-with-Microsoft-Sentinel
A beginner-friendly project that demonstrates how to set up a Windows Server 2019 VM in Hyper-V, connect it to Azure using Azure Arc, and collect event logs into Microsoft Sentinel for security monitoring and analysis using KQL.

# 🔐 Windows Server 2019 + Microsoft Sentinel Integration

This project demonstrates how to deploy a Windows Server 2019 VM in Hyper-V, connect it to Microsoft Sentinel via Azure Arc and Azure Monitor Agent, and collect event logs for analysis using KQL.

## 📦 What’s Included

- 🖥 Setup on Hyper-V
- ☁️ Azure Arc onboarding
- 📈 Microsoft Sentinel log integration
- 🔍 KQL queries to analyze Security Events

## 📄 Guide
See `Windows_Server_2019_Sentinel_Integration_Guide.txt` for the full step-by-step process.

## 📊 KQL Examples

```kql
SecurityEvent
| summarize count() by EventID
