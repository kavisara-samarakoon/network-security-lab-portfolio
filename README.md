# 🛡️ Network Security Lab Portfolio

This repository contains my hands-on networking and cybersecurity lab work, focused on practical system configuration, firewalling, VoIP communication, intrusion detection, VPN preparation, and controlled security testing.

The purpose of this repository is to document my learning and practical experience in **Computer Networks, Network Security, VoIP systems, Firewalls, IDS/IPS, NAT, VPN, and Secure Remote Access**.

---

## 📌 Labs Included

### 1. 📞 FreeBSD + Asterisk VoIP Configuration Lab

A practical VoIP lab built using **FreeBSD**, **Asterisk PBX**, and **Linphone softphones**.

#### Key Areas Covered

- FreeBSD installation in UTM
- Asterisk PBX installation and configuration
- SIP/PJSIP extension setup
- Linphone softphone registration
- Voice and video calling
- Internal extension-to-extension calling
- Conference calling using ConfBridge
- PF firewall rules for VoIP traffic
- SIP-TLS signalling
- ZRTP media encryption
- Voicemail configuration
- IVR menu configuration
- Custom IVR voice prompt testing

#### Skills Demonstrated

- VoIP system configuration
- SIP/PJSIP concepts
- FreeBSD administration
- Firewall rule configuration
- Secure communication setup
- Network troubleshooting
- Practical documentation

#### Evidence

- [Lab README](./labs/freebsd-asterisk-voip/README.md)
- [Lab Summary](./labs/freebsd-asterisk-voip/docs/lab-summary.md)
- [Network Topology Diagram](./diagrams/freebsd-asterisk-voip-topology.md)
- [Screenshot Evidence](./labs/freebsd-asterisk-voip/screenshots/README.md)
- [Sanitized Lab Report](./labs/freebsd-asterisk-voip/docs/freebsd-asterisk-voip-lab-report-sanitized.pdf)

---

### 2. 🔥 pfSense Firewall and Network Security Lab

A network security lab built using **pfSense**, virtual machines, firewall rules, IDS/IPS monitoring, NAT, VPN preparation, and controlled security testing.

#### Key Areas Covered

- pfSense installation in UTM
- WAN, LAN, and OPT interface configuration
- DHCP and DNS setup
- Firewall rule creation and testing
- NAT port forwarding
- Website blocking rule testing
- DVWA setup for controlled security testing
- Snort IDS/IPS configuration
- SYN flood detection
- Nmap port scan detection
- OpenVPN remote access preparation
- Tailscale subnet router remote access testing

#### Skills Demonstrated

- Firewall configuration
- Network segmentation
- DHCP and DNS configuration
- NAT and routing
- IDS/IPS monitoring
- Security testing in an isolated lab
- VPN preparation
- Remote access concepts
- Troubleshooting and documentation

#### Evidence

- [Lab README](./labs/pfsense-firewall-security/README.md)
- [Lab Summary](./labs/pfsense-firewall-security/docs/lab-summary.md)
- [Network Topology Diagram](./diagrams/pfsense-firewall-security-topology.md)
- [Screenshot Evidence](./labs/pfsense-firewall-security/screenshots/README.md)
- [Sanitized Lab Report](./labs/pfsense-firewall-security/docs/pfsense-network-security-lab-report-sanitized.pdf)

---

## 🧰 Tools and Technologies

| Category | Tools / Technologies |
|---|---|
| Virtualization | UTM |
| Operating Systems | FreeBSD, pfSense, Ubuntu, Windows |
| VoIP | Asterisk PBX, Linphone, SIP/PJSIP, RTP, SIP-TLS, ZRTP |
| Security | PF Firewall, pfSense Firewall, Snort IDS/IPS |
| Testing | DVWA, Nmap, hping3 |
| Remote Access | OpenVPN, Tailscale |
| Networking | DHCP, DNS, NAT, Firewall Rules, WAN, LAN, OPT |
| Documentation | Technical reports, screenshots, lab summaries, topology diagrams |

---

## 🗂️ Repository Structure

```text
network-security-lab-portfolio/
├── README.md
├── diagrams/
│   ├── freebsd-asterisk-voip-topology.md
│   └── pfsense-firewall-security-topology.md
│
├── labs/
│   ├── freebsd-asterisk-voip/
│   │   ├── README.md
│   │   ├── docs/
│   │   │   ├── lab-summary.md
│   │   │   └── freebsd-asterisk-voip-lab-report-sanitized.pdf
│   │   └── screenshots/
│   │       ├── README.md
│   │       └── selected-screenshot-files
│   │
│   └── pfsense-firewall-security/
│       ├── README.md
│       ├── docs/
│       │   ├── lab-summary.md
│       │   └── pfsense-network-security-lab-report-sanitized.pdf
│       └── screenshots/
│           ├── README.md
│           └── selected-screenshot-files
│
├── notes/
│   ├── commands-used.md
│   ├── lessons-learned.md
│   └── troubleshooting.md
│
└── LICENSE- WAN, LAN, and OPT interface configuration
- DHCP and DNS setup
- Firewall rule creation and testing
- NAT port forwarding
- Website blocking rule testing
- DVWA setup for controlled security testing
- Snort IDS/IPS configuration
- SYN flood detection
- Nmap port scan detection
- OpenVPN remote access preparation
- Tailscale subnet router remote access testing

#### Skills Demonstrated

- Firewall configuration
- Network segmentation
- NAT and routing
- IDS/IPS monitoring
- Security testing in an isolated lab
- VPN preparation
- Remote access concepts
- Troubleshooting and documentation

---

## 🧰 Tools and Technologies

| Category | Tools / Technologies |
|---|---|
| Virtualization | UTM |
| Operating Systems | FreeBSD, pfSense, Ubuntu, Windows |
| VoIP | Asterisk PBX, Linphone, SIP/PJSIP, RTP |
| Security | PF Firewall, pfSense Firewall, Snort IDS/IPS |
| Testing | DVWA, Nmap, hping3 |
| Remote Access | OpenVPN, Tailscale |
| Networking | DHCP, DNS, NAT, Firewall Rules, LAN/WAN |
| Documentation | Technical reports, screenshots, lab evidence |

---

## 🗂️ Repository Structure

```text
network-security-lab-portfolio/
├── README.md
├── labs/
│   ├── freebsd-asterisk-voip/
│   │   ├── README.md
│   │   ├── screenshots/
│   │   └── docs/
│   │
│   └── pfsense-firewall-security/
│       ├── README.md
│       ├── screenshots/
│       └── docs/
│
├── diagrams/
├── notes/
└── LICENSE
