# 🧾 Commands Used

This file documents important commands used during the networking and cybersecurity labs in this repository.

All commands were used inside controlled virtual lab environments for educational and defensive learning purposes.

---

## 📞 FreeBSD + Asterisk VoIP Lab

### FreeBSD System Verification

```bash
uname -a
ifconfig
pkg update
pkg search asterisk
```

### Asterisk Installation and Service Commands

```bash
pkg install asterisk
service asterisk start
service asterisk status
service asterisk restart
```

### Asterisk CLI Access

```bash
asterisk -rvvv
```

### Asterisk CLI Verification Commands

```bash
pjsip show endpoints
pjsip show contacts
pjsip show aors
dialplan show
confbridge list
```

### PF Firewall Commands

```bash
pfctl -e
pfctl -sr
pfctl -f /etc/pf.conf
pfctl -s info
```

### Network Testing

```bash
ping 192.168.43.87
netstat -an
sockstat -4
```

---

## 🔥 pfSense Firewall and Network Security Lab

### Basic Connectivity Testing

```bash
ping 10.1.10.1
ping 8.8.8.8
nslookup facebook.com
nslookup pfsense.org
```

### DVWA and NAT Testing

```bash
docker ps
docker start dvwa
curl http://10.1.10.103:4280
```

### Nmap Port Scan Testing

```bash
nmap 10.1.10.103
nmap -p 1-1000 10.1.10.103
```

### SYN Flood Detection Test

```bash
sudo hping3 -S --flood -p 80 10.1.10.103
```

> This command was used only inside an isolated virtual lab to test Snort IDS/IPS detection.

### Tailscale Subnet Router Commands

```bash
sudo sysctl -w net.ipv4.ip_forward=1
sudo tailscale up --advertise-routes=10.1.10.0/24
tailscale status
```

---

## ⚠️ Ethical Note

These commands are documented only for educational, defensive, and lab-based cybersecurity learning.

No external systems, public targets, or unauthorized networks were tested.
