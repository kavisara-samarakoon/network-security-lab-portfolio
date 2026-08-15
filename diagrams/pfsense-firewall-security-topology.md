# 🔥 pfSense Firewall and Network Security Lab Topology

This diagram shows the network topology used in the pfSense Firewall and Network Security lab.

```mermaid
flowchart LR
    A[UTM Shared Network<br>WAN: 192.168.64.0/24] --> B[pfSense Firewall<br>WAN: 192.168.64.5<br>LAN: 10.1.10.1<br>OPT1: 10.1.20.1]

    B --> C[Isolated LAN<br>10.1.10.0/24]
    B --> D[OPT1 Network<br>10.1.20.0/24<br>Future Expansion]

    C --> E[Windows Client<br>10.1.10.101]
    C --> F[DVWA Server<br>10.1.10.103:4280]
    C --> G[Ubuntu Test VM<br>LAN Adapter]

    H[Attacker/Test VM<br>192.168.64.10 / 10.1.10.10] --> B

    B --> I[pfSense Services<br>DHCP<br>DNS Resolver<br>Firewall Rules<br>NAT]
    B --> J[Snort IDS/IPS<br>ICMP Alerts<br>SYN Flood Detection<br>Nmap Portscan Detection]

    F -. NAT Port Forward<br>WAN TCP 4280 .-> B
    G -. Tailscale Subnet Router<br>Advertises 10.1.10.0/24 .-> K[iPhone Remote Access Test]
```

---

## 🔍 Topology Explanation

The lab used pfSense as a virtual firewall inside UTM.  
pfSense separated the upstream WAN network from the isolated internal LAN used for client connectivity and controlled security testing.

The Windows client was used for normal LAN testing.  
The DVWA server was used for controlled web security testing.  
Snort IDS/IPS was configured on pfSense to detect suspicious traffic such as SYN flood attempts and Nmap port scans.

---

## 🔐 Security Components

- Firewall rules controlled LAN traffic.
- NAT port forwarding was used for controlled DVWA testing.
- Snort IDS/IPS monitored suspicious traffic.
- OpenVPN remote access was prepared.
- Tailscale subnet routing was tested for secure remote access without exposing the pfSense dashboard publicly.

---

## 📌 Key Network Details

| Component | Details |
|---|---|
| Firewall | pfSense |
| Virtualization | UTM |
| WAN | 192.168.64.5/24 |
| LAN Gateway | 10.1.10.1/24 |
| OPT1 | 10.1.20.1/24 |
| Windows Client | 10.1.10.101 |
| DVWA Server | 10.1.10.103:4280 |
| Attacker/Test VM | 192.168.64.10 / 10.1.10.10 |
| IDS/IPS | Snort |
| Remote Access | OpenVPN preparation + Tailscale subnet routing |
