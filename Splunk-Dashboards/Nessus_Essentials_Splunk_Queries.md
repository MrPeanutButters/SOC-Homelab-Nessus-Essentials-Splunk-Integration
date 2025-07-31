# Example Queries

## Critical Vulnerabilities
index=nessus severity=critical 
| stats count by host, pluginName, cve

## Vulnerable Hosts With Brute-Force Activity
(index=nessus severity=critical) OR (index=wineventlog EventCode=4625)
| stats values(pluginName) values(EventCode) by host
