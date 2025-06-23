# Task1
# Nmap Local Network Scan and Analysis

This project documents a basic network scan using **Nmap** and optional analysis using **Wireshark** on an Ubuntu system.

## 🔧 Steps Performed

1. **Installed Nmap**:
   ```bash
   sudo apt update
   sudo apt install nmap
Identified Local IP Range:

Interface: wlp4s0

IP: 192.168.76.174

Subnet: 192.168.76.0/24

Performed SYN Scan:

bash
Copy
Edit
sudo nmap -sS 192.168.76.0/24
Noted Open Ports:

192.168.76.51: Port 53/tcp open (DNS)

192.168.76.174: No open ports

Optional Packet Analysis with Wireshark:

Captured traffic during scan

Applied filter: tcp.flags.syn == 1

Researched Port 53 Services:

Found to be DNS (Domain Name System)

Identified Risks:

Possible DNS poisoning, tunneling, amplification attacks

Saved Results:

bash
Copy
Edit
sudo nmap -sS 192.168.76.0/24 -oN scan_results.txt
sudo nmap -sS 192.168.76.0/24 -oX scan_results.xml
xsltproc scan_results.xml -o scan_results.html
📂 Files Generated
scan_results.txt

scan_results.xml

scan_results.html (optional)

📌 Tools Used
Nmap

Wireshark (optional)

xsltproc (for HTML conversion)
