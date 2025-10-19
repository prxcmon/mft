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
- Found DLL injection vulnerability on `notsomalicious.exe`

## Exploiting DLL Injection

- Identifying `notsomalicious.exe` on Process Monitor
- Found `blank.dll` is not found
- Crafting malicious `blank.dll` with MSFVenom
- Exporting `blank.dll` in the directory target
- Set up listener on the attacking machine, then run the `notsomalicious.exe` again

# Lateral movement

## MS01 to MS02

### Proxying MS01 to MS02

- Use ligolo-ng/chisel guides

### 

## MS02 to DC01

### BloodHound enumeration

- Found MS02 to DC01 has DCSync vulnerability

### Obtaining Domain Admin hash by exploiting DCSync

- Run impacket on Linux
- Run rubeus on Windows

# Appendix

## References and sources

- Other write-ups -- https://example.com
- More write-ups

## Found credentials

[Machine] --> `username`:`password`
[Machine] --> `username`:`NTLM_hash`
