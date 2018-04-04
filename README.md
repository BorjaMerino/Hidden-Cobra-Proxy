# Hidden-Cobra-Proxy NSE Script
Nmap NSE script to detect the proxy component of the Hidden Cobra APT attributed to North Korean government.

The script attempts to identify the bidirectional proxy component used by this APT by sending an innocuous TCP packet with certain control code.

```
root@kali:~# nmap -n --script hidden-cobra-proxy --script-args='timeout=500' -p 443 192.168.1.44

Starting Nmap 7.60 ( https://nmap.org ) at 2018-04-04 11:48 EDT
Nmap scan report for 192.168.1.44
Host is up (0.00068s latency).

PORT    STATE SERVICE
443/tcp open  https
|_hidden-cobra-proxy: Hidden Cobra Proxy found!
MAC Address: 08:00:27:AB:CD:EF (Oracle VirtualBox virtual NIC)

Nmap done: 1 IP address (1 host up) scanned in 0.90 seconds
```
Reference: https://www.us-cert.gov/HIDDEN-COBRA-North-Korean-Malicious-Cyber-Activity
