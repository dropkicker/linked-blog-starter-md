## 🏆 1. The "Golden Proof" Screenshot
> [!CAUTION] The Requirement
> OffSec graders must see your identity, your IP address, and the flag hash all in the same image to verify the work was done on the correct target.

### 💻 The Multi-Command One-Liners
**Linux:**
```bash
whoami && id && ip addr && cat /root/proof.txt
```

**Windows:**
```powershell
whoami && ipconfig && type C:\Users\Administrator\Desktop\proof.txt
```

---

## 📸 2. Evidence Checklist
You need enough evidence so a "technically competent reader" can replicate your attack.

- [ ] **Nmap Scan:** The specific port/service you targeted.
- [ ] **The Vulnerability:** The web page, version banner, or config file that proved the machine was vulnerable.
- [ ] **The Exploit:** The terminal command you ran to trigger the exploit.
- [ ] **The Shell:** The moment your listener (Netcat) catches the connection.
- [ ] **Modifications:** Screenshots of code diffs or script changes (Python/Exploit-DB).