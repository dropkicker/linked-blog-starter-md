──(bozo㉿kali)-[~/Downloads]
└─$ rustscan -a 10.129.49.208 --ulimit 5000  
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: http://discord.skerritt.blog         :
: https://github.com/RustScan/RustScan :
 --------------------------------------
Breaking and entering... into the world of open ports.

[~] The config file is expected to be at "/home/bozo/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 10.129.49.208:80
[~] Starting Script(s)
[~] Starting Nmap 7.98 ( https://nmap.org ) at 2026-01-25 01:04 -0500
Initiating Ping Scan at 01:04
Scanning 10.129.49.208 [4 ports]
Completed Ping Scan at 01:04, 0.05s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 01:04
Completed Parallel DNS resolution of 1 host. at 01:04, 0.50s elapsed
DNS resolution of 1 IPs took 0.50s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating SYN Stealth Scan at 01:04
Scanning 10.129.49.208 [1 port]
Discovered open port 80/tcp on 10.129.

![[remote-blog/publish/02-Targets/Bashed/01-Enumeration/Screenshots/Rust screenshotagain.png]]

#####Nmap

```
┌──(bozo㉿kali)-[~/Documents/bashed]
└─$ sudo nmap -sC -sV -oA nmap/bashed 10.129.49.208
Starting Nmap 7.98 ( https://nmap.org ) at 2026-01-25 01:14 -0500
Nmap scan report for 10.129.49.208
Host is up (0.093s latency).
Not shown: 999 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
80/tcp open  http    Apache httpd 2.4.18 ((Ubuntu))
|_http-server-header: Apache/2.4.18 (Ubuntu)
|_http-title: Arrexel's Development Site

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 13.11 seconds
```


###### Gobuster
![[remote-blog/publish/02-Targets/Bashed/01-Enumeration/Screenshots/Gobuster_recon.png]]


