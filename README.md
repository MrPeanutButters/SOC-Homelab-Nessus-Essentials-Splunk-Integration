# SOC Homelab – Integrating Nessus Essentials with Splunk

## Overview
This project expands my existing SOC Analyst Homelab by integrating **Nessus Essentials (the free version of Tenable Nessus)** with **Splunk Enterprise**. The goal is to simulate how a Security Operations Center (SOC) identifies and prioritizes vulnerabilities across endpoints while correlating this data with security events for incident response.

## Why This Matters
In real-world SOC operations, vulnerability management and threat detection go hand in hand. By feeding Nessus Essentials scan data into Splunk, I can:
- Visualize vulnerability exposure across Windows and Linux systems
- Correlate vulnerability data with real-time events (e.g., brute-force attacks)
- Trigger alerts when high-risk vulnerabilities are being actively exploited

## Architecture
![Architecture Diagram](Architecture-Diagram.png)

**Key Components:**
- **Ubuntu Server (SIEM/Scanner):** Hosts Splunk Enterprise and Nessus Essentials  
- **Windows 10 (Victim Endpoint):** Target of vulnerability scans and simulated attacks  
- **Ubuntu Client (Attacker VM):** Uses Hydra and other red-team tools  
- **Splunk Dashboards:** Centralized visualization of Nessus Essentials vulnerability data and Windows Event logs  

## Project Steps
1. **Install and configure Nessus Essentials** for authenticated scanning on Windows and Ubuntu targets  
2. **Run vulnerability scans** and export findings via the Splunk Add-on for Tenable  
3. **Ingest Nessus Essentials data into Splunk** using syslog/API inputs  
4. **Create dashboards and correlation searches** to prioritize vulnerabilities and detect potential exploitation  
5. **Map vulnerabilities to MITRE ATT&CK** techniques for deeper analysis  

## Skills Demonstrated
- Vulnerability scanning with **Nessus Essentials (free version of Tenable Nessus)**  
- SIEM integration and custom dashboards in **Splunk**  
- Threat correlation and alert creation  
- CVE remediation prioritization  
- MITRE ATT&CK mapping  
