🧪 Enterprise Security LAB – Active Directory, Web Security & AI-Assisted Log Analysis
📌 Project Overview

This project documents a fully virtualized enterprise-style LAB environment built to practice:

Windows Server administration

Active Directory design

Group Policy enforcement

Linux server management

Web application deployment & hardening

Offensive security testing

Log analysis & detection engineering

AI-assisted security triage

The LAB simulates a small corporate infrastructure with domain management, user restrictions, web services, and a dedicated attacker machine.

All activities were performed in an isolated local environment for educational purposes.

🧱 Infrastructure Architecture
🌐 Network Configuration

Subnet: 10.0.0.0/24
Netmask: 255.255.255.0

Machine Role IP Address
Windows Server 2016 Domain Controller (soc.corp) 10.0.0.1
Windows 11 Pro Domain Client 10.0.0.2
Ubuntu Server Web / Linux Server 10.0.0.3
Kali Linux Attacker Machine 10.0.0.4
🏢 Active Directory – soc.corp
Domain Structure
soc.corp
│
├── OU_Admin
├── OU_Users
└── OU_Guests

Implemented Controls

Custom Organizational Units

Role-based user separation

Logon hour restrictions (09:00–17:00 for standard users)

Peripheral access restrictions:

USB storage blocked

Printer access restricted

Group Policy Objects (GPO) configuration

Account permission segmentation

Security Monitoring

Event ID 4624 – Successful logon

Event ID 4625 – Failed logon

Logon time enforcement validation

Policy enforcement testing

🖥️ Linux Server (Ubuntu)
Services Deployed

Apache2

PHP

MySQL

WordPress

URL (LAB only):

http://10.0.0.3/wordpress

Web Stack Integration

PHP ↔ MySQL configuration

WordPress database isolation

Service verification via Nmap

🔐 Remote Access Configuration
RDP

Windows 11 ↔ Windows Server 2016

SSH

Administrative access to Ubuntu

Log monitoring via /var/log/auth.log

🧪 Offensive Security Testing

A dedicated Kali Linux VM simulates attacker behavior.

Tools Used

Nmap

WPScan

Nikto

Burp Suite

Reconnaissance Techniques

TCP SYN scan (-sS)

UDP scan (-sU)

Service detection (-sV)

OS detection (-O)

Full subnet scan (10.0.0.0/24)

🛡️ Attack Simulation Scenarios
1️⃣ WordPress Brute Force Simulation

Controlled login attempts were performed to:

Generate Apache access log events

Analyze server behavior under authentication attacks

Monitor response codes and IP patterns

Logs Analyzed

/var/log/apache2/access.log

/var/log/apache2/error.log

/var/log/auth.log

2️⃣ Domain Policy Enforcement Testing

Attempted logins outside permitted hours

Tested restricted user permissions

Validated USB blocking policies

Observed related Windows Security Events

🤖 AI-Assisted Log Analysis (Linux Terminal Integration)

A custom AI assistant was integrated into the Linux terminal using OpenAI API.

Purpose

To assist in:

Summarizing authentication logs

Identifying brute-force patterns

Highlighting suspicious IP addresses

Extracting repeated failed login attempts

Accelerating security log triage

Workflow Concept

Logs are filtered locally using Linux tools (grep, awk, sort).

Structured data is passed to the AI API.

AI generates summarized security insight.

Results are reviewed and correlated with system behavior.

⚠️ In production environments, log data should be sanitized before external API transmission.

🔎 Security Engineering Mindset

This LAB focuses not only on attack execution, but on:

Attack surface identification

Log correlation

Policy validation

Detection and mitigation awareness

Infrastructure segmentation

Identity-based security controls

🎯 Learning Objectives

Build and manage an AD domain environment

Apply GPO-based security controls

Deploy and secure a Linux web server

Perform controlled penetration testing

Analyze authentication logs and web logs

Integrate AI-assisted triage into security workflows

Understand attack → detection → mitigation cycles

📊 Key Skills Demonstrated

Windows Server Administration

Active Directory Design

Group Policy Configuration

Linux Server Management

Network Scanning & Enumeration

Web Application Security Testing

Log Analysis & Event Investigation

API Integration (OpenAI)

Security Lab Architecture Design

🚧 Future Improvements

Centralized log aggregation

Fail2ban integration

Web application hardening

Firewall rule optimization

Automated detection scripting

SIEM-style log visualization

⚠️ Disclaimer

This project is strictly educational.
All security testing was conducted in an isolated local lab environment owned and controlled by the author.
