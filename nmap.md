
# 🔍 Nmap Basic Commands Cheat Sheet

## 🛠️ Host Discovery
```
nmap -sn 192.168.1.0/24          # Ping scan to find live hosts
nmap -PR 192.168.1.1             # ARP ping scan
nmap -PE 192.168.1.1             # ICMP Echo ping
nmap -PU 192.168.1.1             # UDP ping
```

## 🔓 Port Scanning
```
nmap 192.168.1.1                 # Default scan (top 1000 ports)
nmap -p 22,80,443 192.168.1.1    # Scan specific ports
nmap -F 192.168.1.1              # Fast scan (fewer ports)
nmap --top-ports 10 192.168.1.1  # Scan top 10 most common ports
```

## 🎯 Scan Types
```
nmap -sS 192.168.1.1             # SYN (stealth) scan
nmap -sT 192.168.1.1             # TCP connect scan
nmap -sU 192.168.1.1             # UDP scan
nmap -sX 192.168.1.1             # Xmas scan
nmap -sA 192.168.1.1             # ACK scan
```

## 🧠 Service and OS Detection
```
nmap -sV 192.168.1.1             # Version detection
nmap -O 192.168.1.1              # OS detection
nmap -A 192.168.1.1              # Aggressive scan (OS, version, scripts)
```

## 🧪 Script Scanning
```
nmap --script default 192.168.1.1
nmap --script vuln 192.168.1.1
nmap --script smb-os-discovery.nse 192.168.91.131

```

## 💾 Output
```
nmap -oN scan.txt 192.168.1.1    # Normal output
nmap -oG scan.gnmap 192.168.1.1  # Grepable output
nmap -oX scan.xml 192.168.1.1    # XML output
```

