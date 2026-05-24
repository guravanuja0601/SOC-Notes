# Splunk Queries

## Failed Login Detection

```spl
index=windows EventCode=4625
| stats count by Account_Name, Source_Network_Address
```

### Purpose
Detect repeated failed login attempts.

### SOC Use Case
Used for brute force detection and suspicious login monitoring.
