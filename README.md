# windows-firewall-configuration
# Windows Firewall Configuration and Testing

## About the Project

This project demonstrates the configuration and testing of basic firewall rules using Windows Defender Firewall on Windows 11.

The practical exercise focuses on creating an inbound rule to block TCP port 23 (Telnet), verifying the configuration, and removing the temporary rule after testing.

## Objectives

- Understand the basic working of a firewall.
- Explore Windows Defender Firewall.
- View and manage inbound firewall rules.
- Create a rule to block incoming traffic on a specific port.
- Verify firewall rule configuration.
- Understand how firewalls help prevent unauthorized access.

## Tools and Technologies

- Windows 11
- Windows Defender Firewall with Advanced Security
- Windows PowerShell

## Project Structure

```text
Windows-Firewall-Configuration/
│
├── README.md
│
└── report/
    └── firewall_configuration_report.txt
```

## Practical Implementation

### 1. Firewall Access

Opened Windows Defender Firewall with Advanced Security using:

`wf.msc`

### 2. Firewall Rule Creation

Created an inbound firewall rule with the following configuration:

| Setting | Value |
|---|---|
| Rule Name | Task4-Block-Telnet |
| Direction | Inbound |
| Protocol | TCP |
| Local Port | 23 |
| Action | Block |
| Profiles | Domain, Private, Public |

### 3. Rule Verification

Verified that the firewall rule was enabled and configured to block inbound TCP traffic on port 23.

### 4. Port Listening Check

Used the following PowerShell command:

`Get-NetTCPConnection -State Listen -LocalPort 23 -ErrorAction SilentlyContinue`

No output was returned, indicating that no service was listening on port 23.

### 5. Cleanup

Deleted the temporary firewall rule after verification to restore the previous configuration.

## Key Learnings

- Understanding inbound and outbound firewall rules.
- Configuring TCP port-based filtering.
- Blocking unwanted incoming network traffic.
- Managing firewall rules using Windows Defender Firewall.
- Verifying and removing temporary security rules.

## Results

Successfully created and verified an inbound firewall rule to block TCP port 23 using Windows Defender Firewall.

An actual connection-blocking test was not demonstrated because no service was listening on the tested port.

## Disclaimer

This project was performed on a personal Windows 10 computer for educational and cybersecurity learning purposes.

## Author

**Hetansh Patel**

Cyber Security Student | Cybersecurity Intern
