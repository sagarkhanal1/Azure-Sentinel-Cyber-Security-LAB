# Azure Sentinel Cyber Security Lab

A cloud security lab demonstrating Microsoft Sentinel setup, Azure monitoring, Windows security event collection, and basic SIEM investigation workflow.

## Project Summary

This project documents the setup of a Microsoft Sentinel lab in Azure. It includes creating cloud resources, configuring a virtual machine, setting up a Log Analytics Workspace, connecting Microsoft Sentinel, collecting Windows security events, and preparing data for investigation and visualisation.

The goal is to practise cloud SIEM fundamentals and become familiar with the workflow used in security monitoring environments.

## Skills Demonstrated

- Azure resource group setup
- Virtual machine deployment
- Virtual network and NSG configuration
- Log Analytics Workspace creation
- Microsoft Sentinel onboarding
- Windows Security Events collection
- Azure Monitor Agent configuration
- Data Collection Rule setup
- Watchlist creation
- SIEM documentation

## Lab Architecture

```text
Azure Virtual Machine
        ↓
Azure Monitor Agent
        ↓
Data Collection Rule
        ↓
Log Analytics Workspace
        ↓
Microsoft Sentinel
        ↓
Queries, alerts, watchlists, investigation
```

## Tools and Services

| Area | Technology |
|---|---|
| Cloud platform | Microsoft Azure |
| SIEM | Microsoft Sentinel |
| Log storage | Log Analytics Workspace |
| Endpoint telemetry | Windows Security Events |
| Data collection | Azure Monitor Agent |
| Network controls | Virtual Network and NSG |

## Walkthrough

### 1. Create Virtual Machine

An Azure virtual machine was created to act as the monitored endpoint.

<img width="537" height="551" alt="Azure virtual machine" src="https://github.com/user-attachments/assets/59a3d302-e816-488d-b14d-0dbf684edfaf" />

### 2. Create Resource Group

A resource group was created to organise the lab resources.

<img width="1742" height="490" alt="Resource group" src="https://github.com/user-attachments/assets/56dea842-d41d-4057-98fb-a285d223eb79" />

### 3. Configure Network Security Group

Network security group settings were reviewed and configured for the lab environment.

<img width="1817" height="555" alt="Network security group" src="https://github.com/user-attachments/assets/e592bc00-bc2f-4283-889f-321665d63237" />

### 4. Create Virtual Network

A virtual network was configured to support the Azure VM.

<img width="1659" height="424" alt="Virtual network" src="https://github.com/user-attachments/assets/b8ef0a3f-2fd4-4abe-84f7-669270b1f666" />

### 5. Configure Lab Inbound Rule

A temporary inbound rule was created for lab testing purposes. In a real production environment, inbound exposure should be tightly restricted and monitored.

<img width="1888" height="552" alt="NSG inbound rule" src="https://github.com/user-attachments/assets/a10b1b47-87f9-4eb1-a620-7b43b8f6694b" />

### 6. Connect to Virtual Machine

The virtual machine was accessed for configuration and validation.

<img width="1435" height="932" alt="Remote desktop connection" src="https://github.com/user-attachments/assets/ad084d71-ec32-4455-8a06-55aa4a1f1420" />

<img width="1161" height="900" alt="Windows VM configuration" src="https://github.com/user-attachments/assets/85b646e1-9dee-4332-bec2-4db596e4d44c" />

### 7. Create Log Analytics Workspace

A Log Analytics Workspace was created to store collected security events.

<img width="862" height="716" alt="Log Analytics Workspace" src="https://github.com/user-attachments/assets/154e57c4-ef74-4aa7-96f7-3ec1ab7dadc5" />

### 8. Add Microsoft Sentinel

Microsoft Sentinel was enabled on the Log Analytics Workspace.

<img width="919" height="619" alt="Microsoft Sentinel setup" src="https://github.com/user-attachments/assets/988fafae-9680-4be3-84ba-209b3c875ecf" />

### 9. Install Windows Security Events Connector

The Windows Security Events connector was added so endpoint security events could be collected.

<img width="911" height="862" alt="Windows Security Events connector" src="https://github.com/user-attachments/assets/d67fd98b-baa7-489e-a7ba-570eede555de" />

### 10. Configure Data Collection Rule

Windows Security Events were configured through Azure Monitor Agent and a Data Collection Rule.

<img width="1877" height="758" alt="Data collection rule" src="https://github.com/user-attachments/assets/0334e09e-d80b-4d9e-a1d4-8d054ffe6c51" />

### 11. Validate Azure Monitor Agent

The Azure Monitor Agent was reviewed to confirm collection configuration.

<img width="1890" height="893" alt="Azure Monitor Agent" src="https://github.com/user-attachments/assets/ea51d5f1-891c-4ba3-9079-3ac5e1b58663" />

### 12. Review Log Analytics Workspace

The workspace was checked to confirm the environment was ready for query and investigation work.

<img width="1881" height="856" alt="Log Analytics Workspace review" src="https://github.com/user-attachments/assets/b3dfa608-4566-4497-aa16-137b8e2b14e0" />

### 13. Create Watchlist and GeoIP Mapping Concept

A watchlist was created as part of the Sentinel investigation workflow.

<img width="1416" height="692" alt="Watchlist creation" src="https://github.com/user-attachments/assets/d51332dd-e258-4bb4-bc07-18b599d596f0" />

<img width="1897" height="887" alt="Sentinel watchlist" src="https://github.com/user-attachments/assets/0edd70b3-5624-4689-9a0a-03aac9a3c740" />

## Key Takeaways

- Microsoft Sentinel uses Log Analytics Workspace as the foundation for security data collection.
- Azure Monitor Agent and Data Collection Rules are important for endpoint telemetry ingestion.
- Cloud SIEM work involves both infrastructure setup and investigation workflow.
- Network exposure in a lab should be clearly labelled as temporary and not production-safe.
- Recruiter-facing security projects should explain the purpose behind each screenshot.

## Future Improvements

- Add KQL queries used for analysis.
- Add incident investigation examples.
- Add Sentinel analytics rule examples.
- Add MITRE ATT&CK mapping for selected detections.
- Add a cost-control note for Azure lab cleanup.
