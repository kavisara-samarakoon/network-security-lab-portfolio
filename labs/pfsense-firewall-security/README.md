# 🔥 pfSense Firewall and Network Security Lab

This lab documents a pfSense-based network security environment built using virtual machines, firewall rules, IDS/IPS monitoring, NAT, VPN preparation, and controlled security testing.

The lab focuses on practical firewall configuration, network segmentation, traffic filtering, intrusion detection, secure remote access concepts, and defensive cybersecurity testing inside an isolated virtual lab environment.

---

## 📌 Lab Overview

The lab was built using **pfSense in UTM** as a virtual firewall.  
The pfSense firewall was configured to separate an upstream network from an isolated LAN environment used for client connectivity and controlled security testing.

The lab included:

- pfSense firewall installation
- WAN, LAN, and OPT interface configuration
- DHCP and DNS configuration
- Firewall rule creation and testing
- NAT port forwarding
- Website blocking test
- DVWA controlled testing
- Snort IDS/IPS monitoring
- SYN flood detection
- Nmap port scan detection
- OpenVPN remote access preparation
- Tailscale subnet router remote access testing

---

## 🧰 Tools and Technologies

| Category | Tools / Technologies |
|---|---|
| Virtualization | UTM |
| Firewall Platform | pfSense |
| Client Systems | Windows VM, Ubuntu VM |
| Security Testing | DVWA, Nmap, hping3 |
| IDS/IPS | Snort |
| Remote Access | OpenVPN, Tailscale |
| Networking | DHCP, DNS, NAT, WAN, LAN, OPT, Firewall Rules |
| Documentation | Screenshots, lab summaries, sanitized report |

---

## 🎯 Purpose

The purpose of this lab is to understand practical firewall configuration, network segmentation, IDS/IPS alert monitoring, NAT, VPN concepts, and defensive security testing in an isolated virtual lab environment.

This lab helped me practice:

- pfSense firewall setup
- Interface configuration
- LAN/WAN network separation
- DHCP and DNS services
- Firewall rule design
- NAT port forwarding
- IDS/IPS alert analysis
- Controlled vulnerability testing
- VPN and secure remote access concepts
- Troubleshooting and documentation

---

## ✅ Key Areas Covered

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

---

## 🔐 Security Features

This lab included several network security-focused configurations:

- Firewall rule-based traffic control
- LAN-side client isolation
- NAT forwarding for controlled testing
- Snort IDS/IPS alert monitoring
- Detection of controlled suspicious traffic
- SYN flood detection
- Nmap port scan detection
- VPN preparation using OpenVPN
- Secure remote access testing using Tailscale subnet routing

---

## 📸 Screenshot Evidence

Selected sanitized screenshots are available in the screenshots folder.

The screenshots demonstrate:

- LAN interface configuration
- DHCP server configuration
- Firewall blocking rule
- DVWA access testing
- Snort IDS alert logging
- SYN flood detection
- Nmap port scan detection

View screenshot documentation here:

[pfSense Lab Screenshots](./screenshots/README.md)

---

## 📄 Documentation

Additional documentation is available in the docs folder.

- [Lab Summary](./docs/lab-summary.md)
- [Sanitized pfSense Lab Report](./docs/pfsense-network-security-lab-report-sanitized.pdf)

The uploaded report is a sanitized version prepared for public GitHub documentation. Sensitive academic and personal details were removed before upload.

---

## 🧪 Testing Performed

The lab was tested using:

- pfSense dashboard verification
- WAN, LAN, and OPT interface checks
- LAN gateway connectivity testing
- DHCP lease testing
- DNS resolution testing
- Internet access testing
- Firewall blocking rule testing
- NAT port forwarding verification
- DVWA controlled testing
- Snort IDS/IPS alert review
- Controlled SYN flood detection
- Controlled Nmap port scan detection
- OpenVPN preparation verification
- Tailscale subnet router remote access testing

---

## 🧠 Skills Demonstrated

This lab demonstrates practical skills in:

- Firewall configuration
- Network segmentation
- DHCP and DNS configuration
- NAT and port forwarding
- IDS/IPS monitoring
- Controlled security testing
- VPN preparation
- Remote access concepts
- Network troubleshooting
- Technical documentation
- Defensive cybersecurity lab design

---

## ⚠️ Ethical and Safety Note

This lab was completed only inside a controlled virtual lab environment for educational and defensive cybersecurity learning.

The security testing activities were performed only against private lab systems.  
No external systems, public targets, or unauthorized networks were tested.

---

## 🚀 Future Improvements

Possible future improvements include:

- Add a clean network topology diagram
- Add more structured setup steps
- Add sanitized configuration examples
- Add troubleshooting notes specific to pfSense and Snort
- Add comparison between firewall, IDS, and IPS behavior
- Add more defensive monitoring examples
- Add more remote access security notes

---

## 📌 Status

✅ Lab documentation added  
✅ Sanitized screenshots added  
✅ Sanitized lab report added  
✅ GitHub-ready structure created
