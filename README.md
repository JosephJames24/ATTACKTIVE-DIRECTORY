🔐 Attacktive Directory - TryHackMe Writeup

A comprehensive walkthrough of the "Attacktive Directory" TryHackMe room, demonstrating complete Active Directory penetration testing from initial enumeration to full domain compromise.
📋 Overview

This repository contains detailed documentation of my penetration testing methodology for exploiting a vulnerable Windows Active Directory environment. The writeup covers the entire attack chain used to gain domain administrator privileges through common AD misconfigurations and vulnerabilities.
🎯 Learning Objectives

    Active Directory Fundamentals - Understanding AD components and services

    Enumeration Techniques - Network, service, and user enumeration

    Kerberos Exploitation - AS-REP Roasting and user enumeration

    SMB Share Analysis - Network share enumeration and credential harvesting

    Privilege Escalation - DCSync attacks and credential dumping

    Lateral Movement - Pass-the-Hash attacks and domain persistence

🛠️ Tools Used

    Nmap - Network enumeration

    enum4linux - SMB enumeration

    Kerbrute - Kerberos user enumeration

    Impacket Suite - GetNPUsers, secretsdump

    John the Ripper - Password cracking

    Evil-WinRM - Post-exploitation

    smbclient - SMB share access

⚡ Attack Flow

    Initial Reconnaissance - Port scanning and service enumeration

    User Discovery - Kerberos-based user enumeration with Kerbrute

    AS-REP Roasting - Exploiting misconfigured pre-authentication

    SMB Enumeration - Share discovery and credential harvesting

    DCSync Attack - Domain credential dumping with backup account

    Pass-the-Hash - Lateral movement to domain administrator

    Flag Collection - Proof of compromise from user desktops

📁 Repository Structure
text

├── README.md          # Main writeup documentation
├── images/            # Screenshots and diagrams
├── commands/          # Useful command references
└── resources/         # Additional learning materials

🚀 Key Techniques Demonstrated

    Kerberos AS-REP Roasting - Compromising accounts without pre-authentication

    DCSync Attacks - Extracting NTDS.dit hashes with replication privileges

    Pass-the-Hash - Authenticating with NTLM hashes instead of passwords

    SMB Share Enumeration - Identifying and accessing network shares

    Credential Cracking - Offline password cracking with John the Ripper

📖 Lessons Learned

    The importance of proper service account configuration

    Dangers of excessive backup account permissions

    How Kerberos misconfigurations can lead to domain compromise

    Criticality of monitoring for DCSync and replication privileges
