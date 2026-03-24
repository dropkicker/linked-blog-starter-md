##Rustscan

┌──(bozo㉿kali)-[~/Documents/boardlight]
└─$ rustscan -a 10.129.6.190 --ulimit 5000
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
Open 10.129.6.190:22
Open 10.129.6.190:80
[~] Starting Script(s)
[~] Starting Nmap 7.98 ( https://nmap.org ) at 2026-01-31 18:09 -0500
Initiating Ping Scan at 18:09
Scanning 10.129.6.190 [4 ports]
Completed Ping Scan at 18:09, 0.04s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 18:09
Completed Parallel DNS resolution of 1 host. at 18:09, 0.50s elapsed
DNS resolution of 1 IPs took 0.50s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating SYN Stealth Scan at 18:09
Scanning 10.129.6.190 [2 ports]
Discovered open port 80/tcp on 10.129.6.190
Discovered open port 22/tcp on 10.129.6.190
Completed SYN Stealth Scan at 18:09, 0.07s elapsed (2 total ports)
Nmap scan report for 10.129.6.190
Host is up, received echo-reply ttl 63 (0.021s latency).
Scanned at 2026-01-31 18:09:53 EST for 0s

PORT   STATE SERVICE REASON
22/tcp open  ssh     syn-ack ttl 63
80/tcp open  http    syn-ack ttl 63

Read data files from: /usr/share/nmap
Nmap done: 1 IP address (1 host up) scanned in 0.74 seconds
           Raw packets sent: 6 (240B) | Rcvd: 3 (116B)

##nmap
└─$ sudo nmap -sC -sV -oA nmap/boardlight 10.129.6.190
Starting Nmap 7.98 ( https://nmap.org ) at 2026-01-31 18:09 -0
Nmap scan report for 10.129.6.190
Host is up (0.057s latency).
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 8.2p1 Ubuntu 4ubuntu0.11 (Ubuntu 
| ssh-hostkey: 
|   3072 06:2d:3b:85:10:59:ff:73:66:27:7f:0e:ae:03:ea:f4 (RSA)
|   256 59:03:dc:52:87:3a:35:99:34:44:74:33:78:31:35:fb (ECDSA
|_  256 ab:13:38:e4:3e:e0:24:b4:69:38:a9:63:82:38:dd:f4 (ED255
80/tcp open  http    Apache httpd 2.4.41 ((Ubuntu))
|_http-server-header: Apache/2.4.41 (Ubuntu)
|_http-title: Site doesn't have a title (text/html; charset=UT
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect resul
Nmap done: 1 IP address (1 host up) scanned in 10.07 seconds
                                                              
┌──(bozo㉿kali)-[~/Documents/boardlight]
└─$ 
