
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

🚀 Try It Yourself
All steps use free tools and the Azure free tier. Great for students and entry-level professionals.

🧑‍💻 Author
Swadesh Rawana - Linkdn : http://linkedin.com/in/swadesh-rawana-297858352
