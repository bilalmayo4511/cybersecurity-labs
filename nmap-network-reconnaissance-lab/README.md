# Nmap Network Reconnaissance Lab

A hands-on cybersecurity lab focused on basic network reconnaissance and service identification using Kali Linux and Nmap in a controlled local environment.

## Objective

The objective of this lab was to practice basic Nmap reconnaissance techniques, identify an active host, discover an open TCP port, and perform service/version detection against a locally hosted HTTP service.

## Lab Environment

- Operating System: Kali Linux
- Target: Localhost (127.0.0.1)
- Network Interface: wlan0
- Local IP: 192.168.0.117
- Tool: Nmap
- Test Service: Python HTTP Server
- Test Port: 8000

## Tools Used

- Kali Linux
- Nmap
- Python 3

## Lab Tasks

 ### 1. IP Configuration

Checked the local network configuration using:

```bash
ip addr
The active wireless interface was wlan0 with local IP address 192.168.0.117.

2. Host Discovery

Performed host discovery against the local Kali machine:
nmap -sn 192.168.0.117

Result:

Host was identified as up.
1 IP address was scanned.

Local HTTP Service

A Python HTTP server was started on localhost port 8000:

python3 -m http.server 8000 --bind 127.0.0.1

Result:

8000/tcp open http-alt

5. Service and Version Detection

Performed service/version detection using:

nmap -sV -p 8000 127.0.0.1

Nmap identified:

8000/tcp open http SimpleHTTPServer 0.6 (Python 3.14.6)

| Scan              | Result               |
| ----------------- | -------------------- |
| Host Discovery    | Host is up           |
| Port Scanning     | TCP/8000 open        |
| Service Detection | HTTP                 |
| Detected Service  | SimpleHTTPServer 0.6 |
| Python Version    | 3.14.6               |

Key Learnings
Understanding basic network reconnaissance
Using Nmap for host discovery
Identifying open TCP ports
Performing service and version detection
Understanding the relationship between ports and network services
Documenting cybersecurity lab results
Ethical Use

This lab was performed against a locally controlled system and test service for educational purposes. Network scanning should only be performed on systems and networks where you have explicit authorization.

Future Improvements

Future versions of this lab may include:

Scanning multiple authorized hosts in a controlled lab
Comparing different Nmap scan techniques
Network traffic analysis with Wireshark
Web security testing with Burp Suite
Additional vulnerability assessment exercises
