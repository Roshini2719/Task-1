# Task-1
1.Open Kali Linux tool and find the local IP range using command:ip a
2.Run the nmap scan using the command:nmap -sS 10.0.2.0/24
-sS: Performs a TCP SYN (Stealth) scan
/24: Scans 256 IP addresses (10.0.2.0 to 10.0.2.255)

Scan Summary
Total Hosts Scanned: 256
Live Hosts Detected: 3

Host: 10.0.2.2
MAC Address: 52:55:04:00:02:02 
Open Ports: None visible
Port States:
All 1000 scanned TCP ports are filtered (state: net-unreach)
Interpretation:
The host is blocking port scans or behind a firewall.
Possibly a hardened or inactive system.

Host: 10.0.2.3
MAC Address: 52:55:04:00:02:03
Open Ports:
53/tcp → Open
Service: domain (DNS)
Other Ports: 999 filtered ports (state: net-unreach)

DNS (Port 53):
Handles domain name lookups.
Could indicate the presence of a DNS server.

Potential Risks:
DNS Amplification Attacks
Zone Transfers could leak internal information.
DNS Tunneling for data exfiltration if misconfigured.
Host: 10.0.2.15
Open Ports: None
Port States:
All 1000 scanned TCP ports are closed (state: reset)
Interpretation:
Host is accessible but not running any TCP services on standard ports.
Could be an endpoint with all ports closed or firewalled.
