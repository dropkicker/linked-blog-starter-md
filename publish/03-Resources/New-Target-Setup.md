<%*
// 1. Ask for the Machine Name
let title = await tp.system.prompt("Enter Machine Name (e.g. Arctic)");
if (!title) return;

// 2. Define the paths
const baseFolder = `02-Targets/${title}`;
const subFolders = [
  "01-Enumeration",
  "02-Initial-Access",
  "03-Privilege-Escalation",
  "04-Post-Exploitation",
  "05-House-Cleaning",
  "Screenshots"
];

// 3. Create the Folders (with existence check)
if (!app.vault.getAbstractFileByPath(baseFolder)) {
    await app.vault.createFolder(baseFolder);
}

for (const sub of subFolders) {
    const path = `${baseFolder}/${sub}`;
    if (!app.vault.getAbstractFileByPath(path)) {
        await app.vault.createFolder(path);
    }
}

// 4. Create the Summary Page
const summaryPath = `${baseFolder}/_Summary-&-${title}.md`;
if (!app.vault.getAbstractFileByPath(summaryPath)) {
    const summaryContent = `---
os: 
ip: 
hostname: 
status: In-Progress
difficulty: 
tags: [target]
---
# 🏠 Summary: ${title}

## 🎯 Machine Info
- **IP:** - **Hostname:** - **OS:** ## 📝 Searchable Keywords
> 

## 🚩 Flags
- [ ] **User:** - [ ] **Root:** ---
## 📓 Quick Log
- ${tp.date.now("YYYY-MM-DD")}: Started box.`;

    await app.vault.create(summaryPath, summaryContent);
}

// 5. Create the Screenshot Checklist Note
const screenshotNotePath = `${baseFolder}/Screenshots/_Screenshot-Checklist.md`;
if (!app.vault.getAbstractFileByPath(screenshotNotePath)) {
    const screenshotContent = `## 🏆 1. The "Golden Proof" Screenshot
> [!CAUTION] The Requirement
> OffSec graders must see your identity, your IP address, and the flag hash all in the same image to verify the work was done on the correct target.

### 💻 The Multi-Command One-Liners
**Linux:**
\`\`\`bash
whoami && id && ip addr && cat /root/proof.txt
\`\`\`

**Windows:**
\`\`\`powershell
whoami && ipconfig && type C:\\Users\\Administrator\\Desktop\\proof.txt
\`\`\`

---

## 📸 2. Evidence Checklist
You need enough evidence so a "technically competent reader" can replicate your attack.

- [ ] **Nmap Scan:** The specific port/service you targeted.
- [ ] **The Vulnerability:** The web page, version banner, or config file that proved the machine was vulnerable.
- [ ] **The Exploit:** The terminal command you ran to trigger the exploit.
- [ ] **The Shell:** The moment your listener (Netcat) catches the connection.
- [ ] **Modifications:** Screenshots of code diffs or script changes (Python/Exploit-DB).`;

    await app.vault.create(screenshotNotePath, screenshotContent);
}

// 6. Open the Summary Page automatically
const newFile = app.vault.getAbstractFileByPath(summaryPath);
if (newFile) {
    await app.workspace.getLeaf().openFile(newFile);
}
%>