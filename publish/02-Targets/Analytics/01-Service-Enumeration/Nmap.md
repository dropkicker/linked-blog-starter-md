##Initial Rust Scan

```
┌──(bozo㉿kali)-[~/Downloads]
└─$ rustscan -a 10.129.60.215 --ulimit 5000
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: http://discord.skerritt.blog         :
: https://github.com/RustScan/RustScan :
 --------------------------------------
Nmap? More like slowmap.🐢

[~] The config file is expected to be at "/home/bozo/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 10.129.60.215:80
Open 10.129.60.215:22
[~] Starting Script(s)
[~] Starting Nmap 7.98 ( https://nmap.org ) at 2026-01-12 20:52 -0500
Initiating Ping Scan at 20:52
Scanning 10.129.60.215 [4 ports]
Completed Ping Scan at 20:52, 0.04s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 20:52
Completed Parallel DNS resolution of 1 host. at 20:52, 0.50s elapsed
DNS resolution of 1 IPs took 0.50s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating SYN Stealth Scan at 20:52
Scanning 10.129.60.215 [2 ports]
Discovered open port 80/tcp on 10.129.60.215
Discovered open port 22/tcp on 10.129.60.215
Completed SYN Stealth Scan at 20:52, 0.12s elapsed (2 total ports)
Nmap scan report for 10.129.60.215
Host is up, received echo-reply ttl 63 (0.044s latency).
Scanned at 2026-01-12 20:52:11 EST for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack ttl 63
80/tcp open  http    syn-ack ttl 63

Read data files from: /usr/share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.76 seconds
           Raw packets sent: 6 (240B) | Rcvd: 3 (116B)

```

##Initial Nmap #ippsec-nmap
```
┌──(bozo㉿kali)-[~/Downloads]
└─$ sudo nmap -sC -sV -oA nmap/analytics 10.129.60.215
Starting Nmap 7.98 ( https://nmap.org ) at 2026-01-12 21:44 -0500
Nmap scan report for 10.129.60.215
Host is up (0.047s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 8.9p1 Ubuntu 3ubuntu0.4 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 3e:ea:45:4b:c5:d1:6d:6f:e2:d4:d1:3b:0a:3d:a9:4f (ECDSA)
|_  256 64:cc:75:de:4a:e6:a5:b4:73:eb:3f:1b:cf:b4:e3:94 (ED25519)
80/tcp open  http    nginx 1.18.0 (Ubuntu)
|_http-title: Did not follow redirect to http://analytical.htb/
|_http-server-header: nginx/1.18.0 (Ubuntu)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 10.05 seconds

```

