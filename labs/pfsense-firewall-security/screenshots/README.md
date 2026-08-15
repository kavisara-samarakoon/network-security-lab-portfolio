# pfSense Firewall and Network Security Lab Evidence

These screenshots provide a concise, public-facing record of the pfSense lab. They contain no student identifiers, lecturer details, credentials, keys, tokens, certificate details, email addresses, personal device names, or public IP addresses.

| Screenshot filename | Description | Evidence shown |
|---|---|---|
| `02-interface-configuration.png` | pfSense LAN interface configuration | Shows the LAN interface enabled with static IPv4 configuration and the lab subnet gateway address. |
| `03-dhcp-dns-configuration.png` | DHCP server configuration | Shows DHCP enabled on LAN and the configured private-lab address pool. |
| `04-firewall-block-rule.png` | Website-blocking firewall rule | Shows an enabled LAN TCP/UDP block rule targeting the `Blocked_Facebook` alias. |
| `05-dvwa-nat-testing.png` | DVWA access test through the mapped lab port | Shows the DVWA login page reachable at the private lab host and port, with both credential fields empty. |
| `06-snort-ids-alerts.png` | Snort IDS alert log | Shows active Snort alert logging for controlled ICMP and DVWA traffic tests. |
| `07-syn-flood-detection.png` | Controlled SYN-flood detection | Shows Snort raising `Possible DoS Attack: SYN Flood Detected` alerts during the lab test. |
| `08-nmap-portscan-detection.png` | Nmap port-scan detection and blocking | Shows the Snort blocked-host record containing a `TCP Filtered Portscan` event. |

Only the PNG files in this directory and this README are intended for public GitHub documentation.
