# Integrate Nessus Essentials with Splunk

## 1. Install Splunk Add-on for Tenable

## 2. Configure Inputs
- Choose Nessus as the data source
- Use Nessus API or parse exported JSON reports

## 3. Verify Data Flow
- Check Splunk indexes for Nessus data
```bash
index=nessus*
```
- Ensure vulnerabilities and host data are visible
