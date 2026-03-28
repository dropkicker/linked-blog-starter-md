
### Rust scan and nmap 
`rustscan -a <IP> --ulimit 5000 -- -sC -sV -vv -O -oA rust_nmap <IP>`


### Full Nmap Port Scan -> Nmap 
`sudo nmap -p- -Pn --open -vvv -T4 --min-rate 1000 -oG openPorts.txt <TARGET_IP>`
`ports=$(grep -oP '\d+(?=/open/tcp)' openPorts.txt | tr '\n' ',' | sed 's/,$//')`
`nmap -sC -sV -vv -O -p $ports -oA detailed_scan <TARGET_IP>`
