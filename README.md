# Defending the Digital Fortress: A pfSense Firewall & Snort IDS Lab

## Overview
This hands-on cybersecurity project simulates a real-world network defense scenario using a three-node virtual lab environment:  
- **pfSense** as a firewall and IDS/IPS  
- **Kali Linux** as the attacker/analyst machine  
- **Metasploitable2** as the vulnerable target

The lab demonstrates the deployment and tuning of intrusion detection rules, packet filtering, and proactive threat mitigation using pfSense and Snort.

## 🖥️ Network Topology

![Network Topology](https://github.com/ldodson10/cybersecurity-phase1-lab-final/blob/main/screenshots/topology.png?raw=true)

*Figure 1: Virtual network architecture showing pfSense (em0 – WAN via NAT, em1

- **WAN (NAT):** pfSense connects to the internet (DHCP)
- **LAN (Internal):** 192.168.10.0/24 subnet for intra-network traffic

| Device           | Interface | IP Address       | Role                    |
|------------------|-----------|------------------|-------------------------|
| pfSense WAN      | em0       | DHCP via NAT     | Internet gateway        |
| pfSense LAN      | em1       | 192.168.10.1     | Firewall & Snort engine |
| Kali Linux       | eth0      | 192.168.10.100   | Attacker/analyst VM     |
| Metasploitable2  | eth0      | 192.168.10.101   | Vulnerable target       |

## Key Lab Steps

- Configured pfSense interfaces via console
- Assigned static LAN IP and enabled DHCP on pfSense
- Verified connectivity using `ping` and `ip a`
- Installed Snort via pfSense GUI and applied custom rules
- Simulated network scans and HTTP traffic from Kali
- Monitored alerts and enforced a firewall rule to block Kali’s IP

## Tools Used

- **pfSense 2.7.2**
- **Snort IDS (Legacy Mode)**
- **Kali Linux 2025.1**
- **Metasploitable2**
- **Oracle VirtualBox**
- **Nmap**, `curl`, `dig`

## Skills Demonstrated

- LAN/WAN segmentation and static IP configuration  
- Deployment of IDS with Snort and alert tuning  
- Testing detection via simulated scanning and probing  
- Creating firewall rules to block attacker traffic  
- Navigating virtual networking challenges in VirtualBox  
- Documentation of technical configuration and results

## Screenshots Included

- pfSense interface setup (https://github.com/ldodson10/cybersecurity-phase1-lab-final/blob/main/screenshots/PFSENSE_final_console.png)
- WebConfigurator access and Snort configuration (https://github.com/ldodson10/cybersecurity-phase1-lab-final/blob/main/screenshots/ping_success.png)
- Alert logs triggered by Nmap scans (https://github.com/ldodson10/cybersecurity-phase1-lab-final/blob/main/screenshots/nmap_%20scan_run_view_results.png)
- Firewall rule blocking Kali's IP (https://github.com/ldodson10/cybersecurity-phase1-lab-final/blob/main/screenshots/Kali_connection_timed_out.png
- Network map (from Packet Tracer or equivalent) (https://github.com/ldodson10/cybersecurity-phase1-lab-final/blob/main/screenshots/nmap_%20scan_run_view_results.png)

## References

- [pfSense Documentation – Netgate](https://docs.netgate.com/pfsense/en/latest/)
- [Snort User Manual – Cisco Talos](https://docs.snort.org/)
- [Kali Linux Documentation](https://www.kali.org/docs/)

---

> This lab showcases practical network defense skills and demonstrates readiness for SOC or Blue Team roles.

