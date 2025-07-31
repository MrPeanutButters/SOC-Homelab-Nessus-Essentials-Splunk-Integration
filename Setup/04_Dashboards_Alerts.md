# Create Splunk Dashboards and Alerts

## 1. Dashboards
- Vulnerability counts by severity
- Top 10 vulnerable hosts
- Vulnerabilities mapped to CVEs

## 2. Alerts
- Trigger alert if a **Critical vulnerability** is found on a host with active attack activity
```spl
index=nessus severity=critical | stats count by host
```

## 3. Correlation Searches
- Cross-reference Nessus vulnerabilities with Windows Event Logs (e.g., brute-force EventID 4625)
