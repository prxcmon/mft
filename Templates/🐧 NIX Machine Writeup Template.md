---
tags: 
difficulty:
  - Very Easy
  - Easy
  - Medium
  - Hard
  - Insane
status:
  - Not Started
  - In-Progress
  - Done
description: Add machine description here
date:
---
# Nmap reconnaissance

```
$ sudo nmap -sCV -A -Pn <target-ip> -oN machine-name.txt
- paste the nmap results here
- nmap commands are complementary; you can customize it as you desired
```

## Open ports to analyze

- 21/TCP: FTP
	- Anonymous login allowed
- 22/TCP: SSH
	- Potential SSH login
- 80/TCP: HTTP
	- Runs Apache/IIS/Nginx
- 139, 445/TCP: SMB
	- SMB version name
- 3389/TCP: RDP
- 5985/TCP: WinRM

# Enumeration

## FTP

FTP anonymous login allowed
- Obtained secret file
- No backup file

## HTTP

Web UI
- Wappalyzer

Version check
- Obtained vulnerable template

Nikto scan
- Found vulnerable technology

## Potential Exploits

CVE-2025-32433
- Description

# Initial Foothold

## Exploiting CVE-2025-32433

Gather information of exploits
- Steps to perform exploitation
- Obtain the user shell

## Other exploits

Gather information of exploits
- Steps to perform exploitation
- Obtain the user shell

# Privilege escalation

## Enumerating OS services

Running PEASS-ng to obtain misconfigured credentials, vulnerable services, SUIDs, and more.
- Found the SUID is exploitable

## Exploiting SUID

Exploiting SUID from GTFObins

# Appendix

## Found credentials

[Machine] --> `username`:`password`
[Machine] --> `username`:`NTLM_hash`