
┌──(bozo㉿kali)-[~/Documents/broker]
└─$ sudo nmap -sC -sV -vv -O -oA nmap/broker 10.129.230.87
Starting Nmap 7.98 ( https://nmap.org ) at 2026-03-03 12:29 -0500
NSE: Loaded 158 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 12:29
Completed NSE at 12:29, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 12:29
Completed NSE at 12:29, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 12:29
Completed NSE at 12:29, 0.00s elapsed
Initiating Ping Scan at 12:29
Scanning 10.129.230.87 [4 ports]
Completed Ping Scan at 12:29, 0.04s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 12:29
Completed Parallel DNS resolution of 1 host. at 12:29, 0.50s elapsed
Initiating SYN Stealth Scan at 12:29
Scanning 10.129.230.87 [1000 ports]
Discovered open port 80/tcp on 10.129.230.87
Discovered open port 22/tcp on 10.129.230.87
Completed SYN Stealth Scan at 12:29, 0.43s elapsed (1000 total ports)
Initiating Service scan at 12:29
Scanning 2 services on 10.129.230.87
Completed Service scan at 12:29, 6.09s elapsed (2 services on 1 host)
Initiating OS detection (try #1) against 10.129.230.87
NSE: Script scanning 10.129.230.87.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 12:29
Completed NSE at 12:29, 1.38s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 12:29
Completed NSE at 12:29, 0.23s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 12:29
Completed NSE at 12:29, 0.00s elapsed
Nmap scan report for 10.129.230.87
Host is up, received echo-reply ttl 63 (0.024s latency).
Scanned at 2026-03-03 12:29:36 EST for 9s
Not shown: 998 closed tcp ports (reset)
PORT   STATE SERVICE REASON         VERSION
22/tcp open  ssh     syn-ack ttl 63 OpenSSH 8.9p1 Ubuntu 3ubuntu0.4 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 3e:ea:45:4b:c5:d1:6d:6f:e2:d4:d1:3b:0a:3d:a9:4f (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBJ+m7rYl1vRtnm789pH3IRhxI4CNCANVj+N5kovboNzcw9vHsBwvPX3KYA3cxGbKiA0VqbKRpOHnpsMuHEXEVJc=
|   256 64:cc:75:de:4a:e6:a5:b4:73:eb:3f:1b:cf:b4:e3:94 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIOtuEdoYxTohG80Bo6YCqSzUY9+qbnAFnhsk4yAZNqhM
80/tcp open  http    syn-ack ttl 63 nginx 1.18.0 (Ubuntu)
| http-auth: 
| HTTP/1.1 401 Unauthorized\x0D
|_  basic realm=ActiveMQRealm
|_http-title: Error 401 Unauthorized
|_http-server-header: nginx/1.18.0 (Ubuntu)
Device type: general purpose
Running: Linux 4.X|5.X
OS CPE: cpe:/o:linux:linux_kernel:4 cpe:/o:linux:linux_kernel:5
OS details: Linux 4.15 - 5.19
TCP/IP fingerprint:
OS:SCAN(V=7.98%E=4%D=3/3%OT=22%CT=1%CU=35573%PV=Y%DS=2%DC=I%G=Y%TM=69A71A89
OS:%P=aarch64-unknown-linux-gnu)SEQ(SP=109%GCD=1%ISR=10B%TI=Z%CI=Z%II=I%TS=
OS:A)OPS(O1=M542ST11NW7%O2=M542ST11NW7%O3=M542NNT11NW7%O4=M542ST11NW7%O5=M5
OS:42ST11NW7%O6=M542ST11)WIN(W1=FE88%W2=FE88%W3=FE88%W4=FE88%W5=FE88%W6=FE8
OS:8)ECN(R=Y%DF=Y%T=40%W=FAF0%O=M542NNSNW7%CC=Y%Q=)T1(R=Y%DF=Y%T=40%S=O%A=S
OS:+%F=AS%RD=0%Q=)T2(R=N)T3(R=N)T4(R=Y%DF=Y%T=40%W=0%S=A%A=Z%F=R%O=%RD=0%Q=
OS:)T5(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=Y%DF=Y%T=40%W=0%S=A%
OS:A=Z%F=R%O=%RD=0%Q=)T7(R=Y%DF=Y%T=40%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U1(R=Y%
OS:DF=N%T=40%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=G%RUD=G)IE(R=Y%DFI=N%T=
OS:40%CD=S)

Uptime guess: 16.304 days (since Sun Feb 15 05:11:28 2026)
Network Distance: 2 hops
TCP Sequence Prediction: Difficulty=265 (Good luck!)
IP ID Sequence Generation: All zeros
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 12:29
Completed NSE at 12:29, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 12:29
Completed NSE at 12:29, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 12:29
Completed NSE at 12:29, 0.00s elapsed
Read data files from: /usr/share/nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 10.28 seconds
           Raw packets sent: 1026 (45.930KB) | Rcvd: 1016 (41.338KB)
                                                                      
┌──(bozo㉿kali)-[~/Documents/broker]
└─$ 



                                                                      
┌──(bozo㉿kali)-[~/Downloads]
└─$ rustscan -a 10.129.230.87 --ulimit 5000
.----. .-. .-. .----..---.  .----. .---.   .--.  .-. .-.
| {}  }| { } |{ {__ {_   _}{ {__  /  ___} / {} \ |  `| |
| .-. \| {_} |.-._} } | |  .-._} }\     }/  /\  \| |\  |
`-' `-'`-----'`----'  `-'  `----'  `---' `-'  `-'`-' `-'
The Modern Day Port Scanner.
________________________________________
: http://discord.skerritt.blog         :
: https://github.com/RustScan/RustScan :
 --------------------------------------
TreadStone was here 🚀

[~] The config file is expected to be at "/home/bozo/.rustscan.toml"
[~] Automatically increasing ulimit value to 5000.
Open 10.129.230.87:22
Open 10.129.230.87:80
Open 10.129.230.87:1883
Open 10.129.230.87:5672
Open 10.129.230.87:8161
Open 10.129.230.87:61613
Open 10.129.230.87:61614
Open 10.129.230.87:61616
[~] Starting Script(s)
[~] Starting Nmap 7.98 ( https://nmap.org ) at 2026-03-03 12:25 -0500
Initiating Ping Scan at 12:25
Scanning 10.129.230.87 [4 ports]
Completed Ping Scan at 12:25, 0.12s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 12:25
Completed Parallel DNS resolution of 1 host. at 12:25, 0.50s elapsed
DNS resolution of 1 IPs took 0.50s. Mode: Async [#: 1, OK: 0, NX: 1, DR: 0, SF: 0, TR: 1, CN: 0]
Initiating SYN Stealth Scan at 12:25
Scanning 10.129.230.87 [8 ports]
Discovered open port 1883/tcp on 10.129.230.87
Discovered open port 61613/tcp on 10.129.230.87
Discovered open port 8161/tcp on 10.129.230.87
Discovered open port 5672/tcp on 10.129.230.87
Discovered open port 61614/tcp on 10.129.230.87
Discovered open port 61616/tcp on 10.129.230.87
Discovered open port 80/tcp on 10.129.230.87
Discovered open port 22/tcp on 10.129.230.87
Completed SYN Stealth Scan at 12:25, 0.99s elapsed (8 total ports)
Nmap scan report for 10.129.230.87
Host is up, received reset ttl 63 (0.67s latency).
Scanned at 2026-03-03 12:25:48 EST for 1s

PORT      STATE SERVICE     REASON
22/tcp    open  ssh         syn-ack ttl 63
80/tcp    open  http        syn-ack ttl 63
1883/tcp  open  mqtt        syn-ack ttl 63
5672/tcp  open  amqp        syn-ack ttl 63
8161/tcp  open  patrol-snmp syn-ack ttl 63
61613/tcp open  unknown     syn-ack ttl 63
61614/tcp open  unknown     syn-ack ttl 63
61616/tcp open  unknown     syn-ack ttl 63

Read data files from: /usr/share/nmap
Nmap done: 1 IP address (1 host up) scanned in 1.71 seconds
           Raw packets sent: 12 (504B) | Rcvd: 1964 (78.612KB)

                                                                      
┌──(bozo㉿kali)-[~/Downloads]
└─$ 


