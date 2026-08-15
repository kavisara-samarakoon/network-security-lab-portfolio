# 📞 FreeBSD + Asterisk VoIP Configuration Lab

This lab documents a FreeBSD-based VoIP environment using **Asterisk PBX** and **Linphone softphones**.

The lab focuses on practical VoIP system configuration, SIP/PJSIP communication, secure signalling, encrypted media, firewall protection, voicemail, IVR, and call testing inside a controlled virtual lab environment.

---

## 📌 Lab Overview

The VoIP server was built using a **FreeBSD virtual machine in UTM**.  
Asterisk PBX was configured as the central call-control server, while Linphone softphones were used as client endpoints.

The lab included:

- SIP/PJSIP extension registration
- Voice and video calling
- Conference calling
- PF firewall protection
- SIP-TLS signalling
- ZRTP media encryption
- Voicemail
- IVR menu
- Custom IVR prompt testing

---

## 🧰 Tools and Technologies

| Category | Tools / Technologies |
|---|---|
| Virtualization | UTM |
| Operating System | FreeBSD |
| VoIP Server | Asterisk PBX |
| Softphone Client | Linphone |
| Protocols | SIP, PJSIP, RTP, SIP-TLS, ZRTP |
| Firewall | PF Firewall |
| Features | Voice Calls, Video Calls, Conference Calls, Voicemail, IVR |

---

## 🎯 Purpose

The purpose of this lab is to understand practical VoIP system configuration, SIP communication, firewall protection, and secure voice communication concepts.

This lab helped me practice:

- FreeBSD server setup
- Asterisk PBX configuration
- SIP/PJSIP endpoint setup
- VoIP call routing
- Firewall rule configuration
- Secure VoIP communication
- Voicemail and IVR feature configuration
- Technical troubleshooting and documentation

---

## ✅ Key Areas Covered

- FreeBSD installation in UTM
- Asterisk PBX setup
- SIP/PJSIP extension configuration
- Linphone softphone registration
- Voice and video calling
- Internal extension-to-extension calling
- Conference calling using ConfBridge
- PF firewall rules
- SIP-TLS signalling
- ZRTP media encryption
- Voicemail configuration
- IVR menu configuration
- Custom IVR voice prompt testing

---

## 🔐 Security Features

This lab included several VoIP security-focused configurations:

- PF firewall rules to allow only required VoIP and management traffic
- SIP-TLS for secure SIP signalling
- ZRTP for end-to-end encrypted media
- Controlled RTP media port range
- Voicemail access testing
- IVR call routing in a controlled lab environment

---

## 📸 Screenshot Evidence

Selected sanitized screenshots are available in the screenshots folder.

The screenshots demonstrate:

- ZRTP encrypted voice call testing
- Encrypted desktop call testing
- IVR menu call testing
- Custom IVR prompt testing
- DTMF input testing
- Voicemail access testing

View screenshot documentation here:

[VoIP Lab Screenshots](./screenshots/README.md)

---

## 📄 Documentation

Additional documentation is available in the docs folder.

- [Lab Summary](./docs/lab-summary.md)
- [Sanitized VoIP Lab Report](./docs/freebsd-asterisk-voip-lab-report-sanitized.pdf)

The uploaded report is a sanitized version prepared for public GitHub documentation. Sensitive academic and personal details were removed before upload.

---

## 🧪 Testing Performed

The lab was tested using:

- Asterisk CLI verification
- SIP/PJSIP endpoint registration checks
- Linphone softphone call testing
- Voice call testing
- Video call testing
- Conference call testing
- SIP-TLS transport verification
- ZRTP encrypted call verification
- Voicemail access testing
- IVR menu testing
- PF firewall rule verification

---

## 🧠 Skills Demonstrated

This lab demonstrates practical skills in:

- VoIP system configuration
- SIP/PJSIP communication
- FreeBSD administration
- Asterisk PBX management
- Firewall rule configuration
- Secure communication setup
- Network troubleshooting
- Technical documentation
- Defensive network service configuration

---

## ⚠️ Ethical and Safety Note

This lab was completed only inside a controlled virtual lab environment for educational and defensive learning purposes.

No external systems, public targets, or unauthorized networks were tested.

---

## 🚀 Future Improvements

Possible future improvements include:

- Add a clean topology diagram
- Add more structured setup steps
- Add configuration file examples with sensitive values removed
- Add troubleshooting notes specific to VoIP errors
- Add a comparison between SIP, SIP-TLS, RTP, and ZRTP
- Expand the lab with monitoring and logging improvements

---

## 📌 Status

✅ Lab documentation added  
✅ Sanitized screenshots added  
✅ Sanitized lab report added  
✅ GitHub-ready structure created
