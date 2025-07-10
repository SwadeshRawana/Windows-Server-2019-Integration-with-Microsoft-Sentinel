# 🔐 Windows Server 2019 + Microsoft Sentinel Integration

This project demonstrates how to set up a Windows Server 2019 virtual machine in Hyper-V, onboard it to Azure using Azure Arc, and collect Windows event logs into Microsoft Sentinel. It’s designed for students and entry-level professionals to practice hybrid cloud integration and SIEM log monitoring using KQL (Kusto Query Language).

---

## 📦 What’s Included

- 🖥 Setup of Windows Server 2019 in Hyper-V
- ☁️ Azure Arc onboarding for hybrid cloud connection
- 📈 Microsoft Sentinel log integration via Azure Monitor Agent
- 🔍 Event log collection (Security, System, Application)
- 📊 KQL queries to analyze login activity and security events

---

## 🛠 Project Structure

```
azure-sentinel-windows-logs/
├── README.md
├── setup-guide/
│   └── Windows_Server_2019_Sentinel_Integration_Guide.txt
├── kql-queries/
│   ├── all-events.kql
│   ├── failed-logins.kql
│   ├── top-accounts.kql
├── screenshots/
│   └── (Add your screenshots here)
```

---

## 📄 Setup Guide

Step-by-step instructions are available in:

```
setup-guide/Windows_Server_2019_Sentinel_Integration_Guide.txt
```

---

## 📊 Sample KQL Queries

### All Collected Event Logs (past 1 day)
```kql
Event
| where TimeGenerated > ago(1d)
| project TimeGenerated, EventID, Computer, RenderedDescription
```

### Count by Security Event ID
```kql
SecurityEvent
| summarize count() by EventID
```

### Failed Logins (Event ID 4625)
```kql
SecurityEvent
| where EventID == 4625
| project TimeGenerated, Account, Computer, LogonType, Status
```

---

## 🧠 What You Learn

- Hyper-V VM setup
- Azure hybrid cloud architecture (Azure Arc)
- Log Analytics Workspace (LAW)
- Microsoft Sentinel SIEM basics
- Writing and running KQL queries

---

## 🧑‍💻 Author

**Swadesh Rawana**  
📍 Cybersecurity & Network Systems Student  
🔗 [LinkedIn Profile](http://linkedin.com/in/swadesh-rawana-297858352)

---

## 📜 License

This project is open for learning and demonstration purposes.
