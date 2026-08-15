
# 🛠️ Troubleshooting Notes

This document summarizes common issues, causes, and solutions identified during the networking and cybersecurity labs in this repository.

The purpose of this file is to document practical troubleshooting experience from the lab work and show how problems were analyzed and solved step by step.

---

## 📞 FreeBSD + Asterisk VoIP Lab

### 1. FreeBSD VM Network Connectivity Issue

**Issue:**  
The FreeBSD virtual machine needed to communicate with the Mac and iPhone softphone clients on the same local network.

**Possible Cause:**  
The virtual machine network adapter must be configured correctly. If NAT mode is used instead of bridged mode, other LAN devices may not directly reach the FreeBSD server.

**Solution:**  
The UTM network adapter was configured in bridged mode so the FreeBSD VM could join the same LAN as the client devices.

**Result:**  
The FreeBSD server became reachable from the local network and Linphone clients could connect to the Asterisk PBX.

---

### 2. SIP Registration Problems

**Issue:**  
Softphone clients may fail to register with the Asterisk PBX.

**Possible Causes:**

- Incorrect server IP address
- Wrong SIP username or password
- PJSIP endpoint configuration errors
- Firewall blocking SIP traffic
- Asterisk service not running

**Solution Steps:**

- Verify the FreeBSD server IP address using `ifconfig`
- Confirm Asterisk service is running
- Check PJSIP endpoint, authentication, and AOR configuration
- Verify registration status from the Asterisk CLI
- Confirm SIP port access through the firewall

**Result:**  
Linphone softphones were able to register with the Asterisk PBX using configured extensions.

---

### 3. Voice or Video Call Media Issue

**Issue:**  
SIP registration may work, but voice or video media may fail.

**Possible Causes:**

- RTP media ports are blocked
- Codec mismatch between Asterisk and Linphone
- NAT traversal settings are missing or incorrect
- Firewall rules allow SIP but not RTP traffic

**Solution:**  

- Allow RTP media range through the firewall
- Confirm codec configuration in Asterisk
- Check Linphone audio/video codec settings
- Verify NAT traversal settings such as symmetric RTP and contact rewriting

**Result:**  
Voice and video calling worked successfully between registered softphone clients.

---

### 4. PF Firewall Blocking VoIP Traffic

**Issue:**  
After enabling PF firewall, SIP registration or media traffic may stop working.

**Possible Cause:**  
The firewall may be blocking SIP, SIP-TLS, or RTP ports.

**Solution:**  
PF rules should allow only required VoIP and management traffic, such as:

- SSH for administration
- SIP traffic
- SIP-TLS traffic
- RTP media ports
- ICMP for testing

**Result:**  
The firewall protected the FreeBSD server while still allowing required VoIP communication.

---

### 5. SIP-TLS or Secure Communication Issue

**Issue:**  
SIP-TLS registration may fail or the softphone may not connect using secure signalling.

**Possible Causes:**

- TLS transport not configured correctly
- Certificate issue
- SIP-TLS port blocked by firewall
- Softphone transport setting not changed to TLS

**Solution:**  

- Verify TLS transport configuration in Asterisk
- Confirm the TLS port is listening
- Allow SIP-TLS traffic through the firewall
- Configure the softphone account to use TLS transport

**Result:**  
Secure SIP signalling was enabled and tested through the VoIP lab.

---

## 🔥 pfSense Firewall and Network Security Lab

### 1. WAN Address Did Not Match the Lab Sheet

**Issue:**  
The WAN IP address did not match the address expected in the lab sheet.

**Cause:**  
The lab sheet used a different network range, but UTM shared networking assigned its own private IP range.

**Solution:**  
The WAN interface was changed to DHCP under the UTM shared network environment.

**Result:**  
pfSense received a working WAN address and Internet connectivity worked through UTM.

---

### 2. Mac Host Could Not Directly Reach pfSense LAN

**Issue:**  
The Mac host could not directly access the pfSense LAN gateway.

**Cause:**  
The pfSense LAN was configured as a host-only/internal virtual network used by the virtual machines.

**Solution:**  
pfSense was managed from a Windows or Ubuntu VM connected to the LAN network.

**Result:**  
Web and SSH management were available from inside the lab network.

---

### 3. Facebook Wildcard Blocking Issue

**Issue:**  
A wildcard entry such as `*.facebook.com` was not accepted in the pfSense host alias.

**Cause:**  
The host alias did not support that wildcard format.

**Solution:**  
Separate entries were used instead, such as:

- `facebook.com`
- `www.facebook.com`
- `m.facebook.com`

**Result:**  
The firewall rule successfully blocked the tested Facebook connection.

---

### 4. DVWA Access Blocked by Snort

**Issue:**  
DVWA became unreachable through the NAT rule during testing.

**Cause:**  
Snort detected the attacker/test machine traffic and added the source address to the blocked-host list.

**Solution:**  
The blocked host entry was cleared, or Snort was temporarily adjusted to alert-only mode while collecting lab evidence.

**Result:**  
DVWA became reachable again for controlled testing.

---

### 5. Nmap Scan Did Not Trigger Port Scan Alert

**Issue:**  
The Nmap scan did not generate a port scan alert at first.

**Cause:**  
The Snort portscan preprocessor was not enabled.

**Solution:**  
Port scan detection was enabled for all protocols and scan types with higher sensitivity.

**Result:**  
Snort detected the scan and reported it as a TCP filtered port scan.

---

### 6. DVWA Service Needed Restart After Shutdown

**Issue:**  
DVWA was not reachable after the lab virtual machines were shut down and restarted.

**Cause:**  
The required virtual machines and Docker service were not running after shutdown.

**Solution:**  

- Start pfSense first
- Start the DVWA server
- Start the attacker/testing VM
- Verify Docker container status
- Recheck NAT and firewall rules

**Result:**  
DVWA and Snort monitoring worked correctly after restarting the lab environment.

---

### 7. SYN Flood Test Received No Replies

**Issue:**  
The controlled SYN test did not receive normal replies.

**Cause:**  
The firewall and IDS/IPS were dropping or blocking the traffic.

**Solution:**  
Instead of depending only on client-side replies, the Snort alert page and blocked-host list were checked.

**Result:**  
The detection and blocking evidence was confirmed from the firewall and IDS/IPS logs.

---

### 8. OpenVPN Could Not Be Reached Directly from Mobile Data

**Issue:**  
The OpenVPN server could not be reached directly from mobile data.

**Cause:**  
The pfSense VM was behind UTM private networking and did not have a directly reachable public endpoint.

**Solution:**  
An Ubuntu VM was configured as a Tailscale subnet router and the lab subnet route was approved.

**Result:**  
The pfSense Web UI became reachable from the iPhone over 4G through the private Tailscale route without exposing the firewall directly to the public Internet.

---

## 🧠 General Troubleshooting Approach

When a lab issue happens, the following troubleshooting flow can be used:

1. **Check basic connectivity**
   - Ping gateway
   - Check IP address
   - Confirm subnet and interface settings

2. **Check service status**
   - Confirm the required service is running
   - Restart the service if needed
   - Check service logs

3. **Check firewall rules**
   - Confirm required ports are allowed
   - Check rule order
   - Check firewall logs

4. **Check NAT and routing**
   - Verify gateway settings
   - Verify NAT rules
   - Confirm internal and external interface placement

5. **Check security tools**
   - Review IDS/IPS alerts
   - Check blocked-host lists
   - Confirm rules are enabled correctly

6. **Document the fix**
   - Record the issue
   - Record the cause
   - Record the solution
   - Record the final result

---

## 🎯 Key Troubleshooting Lessons

Through these labs, I learned that many network and security issues are caused by:

- Incorrect virtual network mode
- Wrong interface assignment
- Firewall rule order problems
- Blocked ports
- NAT misconfiguration
- IDS/IPS blocking expected lab traffic
- Services not running after VM restart
- Missing detection options in security tools
- Private virtual networks not being directly reachable from outside

---

## ⚠️ Ethical Note

All troubleshooting and testing activities were performed only inside controlled virtual lab environments.

No public systems, external targets, or unauthorized networks were tested.
