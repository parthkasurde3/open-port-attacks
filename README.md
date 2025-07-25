
# Open Port Scanning & Brute-Force Attack Project

This project demonstrates advanced network reconnaissance, service enumeration, and brute-force login attacks using **Kali Linux**, **Nmap**, and **Wireshark** in a controlled lab environment.

## 📌 Project Structure

```
open-port-attacks/
├── README.md
├── docs/
│   └── project_report.pdf
├── logs/
│   └── command_log.txt
├── scripts/
│   └── script_list.txt
├── captures/
│   └── wireshark_eth0_sample.pcapng
```

## 🔧 Tools & Environment

- **OS**: Kali Linux on VMware Workstation 16
- **Scanning Tool**: Nmap 7.91
- **Packet Analysis**: Wireshark
- **Target**: AltoroMutual (testfire.net), Kali.org, local subnet `192.168.35.0/24`

## 🧪 Commands Executed

```bash
# Basic host discovery on subnet
nmap -sn 192.168.35.128/22

# Stealth SYN scan
nmap -sS 192.168.114.130
nmap -sS 192.168.35.128/22

# Aggressive scan with OS detection
nmap -v -A kali.org
nmap -v -A testfire.net

# Directory navigation for NSE scripts
cd /usr/share/nmap/scripts
ls
ls -l | grep ssh

# SSH brute-force attack
nmap --script ssh-brute.nse -p 22 192.168.35.129
```

## 🧾 Results Summary

- **Open Ports Found**: 22 (SSH), 80 (HTTP), 443 (HTTPS)
- **Hosts Online**: Over 770 detected in 192.168.35.0/24
- **SSH Brute Attempts**: Admin/root/guest accounts tried
- **SSL Certificate Info**: Extracted from `testfire.net`
- **Packet Captures**: TCP SYN, ACK, RST flags analyzed with Wireshark

## 🛡️ Disclaimer

This project is conducted in a controlled lab setting for **educational and ethical hacking practice**. Never use these techniques on networks you don't own or have permission to test.
