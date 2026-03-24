---
os: Linux
ip: empty
hostname: bashed
status: Complete
difficulty: easy
tags: []
---
e# 🏠 Summary: Bashed

## 🎯 Machine Info
- **IP:** - **Hostname:** - **OS:** ## 📝 Searchable Keywords

 nmap the server, 1 port open just a webserver.
 gobuster and find a dev directory php with a webshell in there
 in the webshell upload Linenum.sh to /dev/shm a temporary storage area using a simplehttpserver and wget. run it and see that a user scriptmanager can run any command.

get a reverseshell by uploading a shell into uploads folder and executing to a netcat listener

sudo into that user. its got a scripts folder that has a script that runs on a cron as root. edit that file for a reverseshell and run a netcat listener to get a root shell back






## 🚩 Flags
- [ ] **User:** - [ ] **Root:** ---
## 📓 Quick Log
- 2026-01-22: Started box.