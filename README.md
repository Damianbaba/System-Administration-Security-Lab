# System-Administration-Security-Lab

🧪 LAB: System Administration & Security Fundamentals

Project description

This project presents a complete LAB environment built for learning and practicing Windows and Linux system administration as well as cybersecurity fundamentals.
The LAB was created locally in a virtualized environment and includes network configuration, remote access, service analysis, and web application security testing.

This is an educational and demonstrational project.

🎯 Project goals

-build a client–server environment (Windows + Linux)

-configure remote access (RDP, SSH)

-analyze network services using Nmap

-deploy a web application (WordPress)

-perform controlled brute force tests

-analyze logs and system behavior

🧱 Environment architecture

Network
Subnet: 10.0.0.0/24
Netmask: 255.255.255.0

LAB machines

System Role IP Address
Windows Server 2016 Administration server 10.0.0.1
Windows 11 Pro Client workstation 10.0.0.2
Ubuntu Linux Linux / Security server 10.0.0.3

🔐 Remote access

-RDP

-Windows 11 → Windows Server 2016

-Windows Server → Windows 11

-SSH

-Administrative access to Ubuntu Linux

🌐 Network analysis (Nmap)

From the Ubuntu Linux machine, network scans were performed to identify active hosts, open ports, and services.

Techniques used:

-TCP SYN Scan (-sS)

-UDP Scan (-sU)

-Service & Version Detection (-sV)

-OS Detection (-O)

-No DNS resolution scans (-n)

Scope:

10.0.0.0/24

🖥️ Web server (Linux)

-Apache2

-PHP

-MySQL

-PHP ↔ SQL integration

📰 WordPress

-WordPress installed on Ubuntu Linux

-Database configured

-Fully functional web application

URL:

http://10.0.0.3/wordpress

🛡️ Security testing – Brute Force

In the LAB environment, controlled multiple login attempts were performed against the WordPress admin panel to:

-simulate brute force attacks

-generate security events

-analyze server behavior

Monitored elements:

-Apache logs

-application behavior

-server response under increased load

⚠️ All tests were performed only on a self-hosted LAB application.

📌 Conclusions

This project allowed:

-practical integration of Windows and Linux administration

-understanding of local network architecture

-analysis of real security logs

-increased awareness of web application threats

📄 Disclaimer

This project was created for educational purposes only and conducted exclusively in a controlled LAB environment.
