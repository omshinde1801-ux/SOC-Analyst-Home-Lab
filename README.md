# SOC Analyst Home Lab

### Wazuh SIEM-Based Windows Security Monitoring and Alert Investigation

## Project Overview

This project demonstrates a SOC Analyst home lab built using Wazuh SIEM to monitor Windows endpoint security events and investigate authentication-related alerts.

The lab uses Docker-based Wazuh services and a Windows endpoint configured with the Wazuh Agent.

## Objectives

- Deploy Wazuh SIEM using Docker.
- Connect and monitor a Windows endpoint.
- Review security events using the Wazuh Dashboard.
- Investigate Windows authentication-related events.
- Analyze failed-logon events and document investigation findings.
- Understand the fundamentals of security alert triage.

## Tools and Technologies

- Wazuh SIEM
- Wazuh Agent
- Docker Desktop
- Windows 11
- Windows Security Logs

## Lab Architecture

Windows Endpoint  
↓  
Wazuh Agent  
↓  
Wazuh Manager  
↓  
Wazuh Indexer  
↓  
Wazuh Dashboard  
↓  
Security Event Investigation

## Practical Investigation

### Windows Failed-Logon Analysis

- **Windows Event ID:** 4625
- **Wazuh Rule ID:** 60122
- **Observed Alert:** Logon Failure - Unknown user or bad password

The investigation involved filtering Windows Security Event ID 4625, reviewing matching events, and inspecting available authentication-related fields.

Four matching events were observed during the selected time range documented in the report.

A failed-logon event does not by itself prove a brute-force attack. Additional evidence and event correlation are needed to determine whether activity is suspicious.

## Key Learnings

- SIEM deployment and basic configuration.
- Windows endpoint monitoring.
- Security event filtering and inspection.
- Authentication event analysis.
- Basic alert triage and investigation documentation.

## Future Improvements

- Validate Sysmon event collection.
- Investigate additional security scenarios.
- Correlate related events during investigations.
- Document complete investigations with supporting evidence.
- Expand detection and monitoring capabilities.

## Project Report

See `SOC-Analyst-Home-Lab-Report.pdf` in this repository for the documented implementation, experiments, screenshots, and findings.

## Disclaimer

This project was developed for educational purposes in a controlled home lab environment.
