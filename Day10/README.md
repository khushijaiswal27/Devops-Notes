### Day 10: Master Linux Permissions & Ownership 

## Task 12 :
Learn LVM to manage storage flexibly – create, extend, and mount volumes.

**Watch First:** [Linux LVM Tutorial](https://youtu.be/Evnf2AAt7FQ?si=ncnfQYySYtK_2K3c)

---

## Expected Output
- A markdown file: `day-13-lvm.md`
- Screenshots of command outputs

---

## Before You Start

Switch to root user:
```bash
sudo -i
```
or
```bash
sudo su
```
No spare disk? Create a virtual one (watch the tutorial):
```bash
dd if=/dev/zero of=/tmp/disk1.img bs=1M count=1024
losetup -fP /tmp/disk1.img
losetup -a   # Note the device name (e.g., /dev/loop0)
```

---

## Challenge Tasks

### Task 1: Check Current Storage
Run: `lsblk`, `pvs`, `vgs`, `lvs`, `df -h`

### Task 2: Create Physical Volume
```bash
pvcreate /dev/sdb   # or your loop device
pvs
```

### Task 3: Create Volume Group
```bash
vgcreate devops-vg /dev/sdb
vgs
```

### Task 4: Create Logical Volume
```bash
lvcreate -L 500M -n app-data devops-vg
lvs
```

### Task 5: Format and Mount
```bash
mkfs.ext4 /dev/devops-vg/app-data
mkdir -p /mnt/app-data
mount /dev/devops-vg/app-data /mnt/app-data
df -h /mnt/app-data
```

### Task 6: Extend the Volume
```bash
lvextend -L +200M /dev/devops-vg/app-data
resize2fs /dev/devops-vg/app-data
df -h /mnt/app-data
```

---

## Documentation

Create `day-13-lvm.md` with:
- Commands used
- Screenshots of outputs
- What you learned (3 points)

---

## Task 13 :
Get comfortable with core networking concepts and the commands you’ll actually run during troubleshooting.

You will:
- Map the **OSI vs TCP/IP models** in your own words
- Run essential connectivity commands
- Capture a mini network check for a target host/service

Keep it short, real, and repeatable.

---

## Expected Output
- A markdown file: `day-14-networking.md`
- Screenshots (optional) of key command outputs

---

## Quick Concepts (write 1–2 bullets each)
- OSI layers (L1–L7) vs TCP/IP stack (Link, Internet, Transport, Application)
- Where **IP**, **TCP/UDP**, **HTTP/HTTPS**, **DNS** sit in the stack
- One real example: “`curl https://example.com` = App layer over TCP over IP”

---

## Hands-on Checklist (run these; add 1–2 line observations)
- **Identity:** `hostname -I` (or `ip addr show`) — note your IP.
- **Reachability:** `ping <target>` — mention latency and packet loss.
- **Path:** `traceroute <target>` (or `tracepath`) — note any long hops/timeouts.
- **Ports:** `ss -tulpn` (or `netstat -tulpn`) — list one listening service and its port.
- **Name resolution:** `dig <domain>` or `nslookup <domain>` — record the resolved IP.
- **HTTP check:** `curl -I <http/https-url>` — note the HTTP status code.
- **Connections snapshot:** `netstat -an | head` — count ESTABLISHED vs LISTEN (rough).

Pick one target service/host (e.g., `google.com`, your lab server, or a local service) and stick to it for ping/traceroute/curl where possible.

---

## Mini Task: Port Probe & Interpret
1) Identify one listening port from `ss -tulpn` (e.g., SSH on 22 or a local web app).  
2) From the same machine, test it: `nc -zv localhost <port>` (or `curl -I http://localhost:<port>`).  
3) Write one line: is it reachable? If not, what’s the next check? (e.g., service status, firewall).

---

## Reflection (add to your markdown)
- Which command gives you the fastest signal when something is broken?
- What layer (OSI/TCP-IP) would you inspect next if DNS fails? If HTTP 500 shows up?
- Two follow-up checks you’d run in a real incident.

---

## Task 14:
Build on Day 14 by understanding the building blocks of networking every DevOps engineer must know.

You will:
- Understand how **DNS** resolves names to IPs
- Learn **IP addressing** (IPv4, public vs private)
- Break down **CIDR notation** and **subnetting** basics
- Know common **ports** and why they matter

This is concept-focused — research, understand, and document in your own words.

---

## Expected Output
- A markdown file: `day-15-networking-concepts.md`

---

## Challenge Tasks

### Task 1: DNS – How Names Become IPs
1. Explain in 3–4 lines: what happens when you type `google.com` in a browser?
2. What are these record types? Write one line each:
   - `A`, `AAAA`, `CNAME`, `MX`, `NS`
3. Run: `dig google.com` — identify the A record and TTL from the output

---

### Task 2: IP Addressing
1. What is an IPv4 address? How is it structured? (e.g., `192.168.1.10`)
2. Difference between **public** and **private** IPs — give one example of each
3. What are the private IP ranges?
   - `10.x.x.x`, `172.16.x.x – 172.31.x.x`, `192.168.x.x`
4. Run: `ip addr show` — identify which of your IPs are private

---

### Task 3: CIDR & Subnetting
1. What does `/24` mean in `192.168.1.0/24`?
2. How many usable hosts in a `/24`? A `/16`? A `/28`?
3. Explain in your own words: why do we subnet?
4. Quick exercise — fill in:

| CIDR | Subnet Mask   | Total IPs | Usable Hosts |
|------|-------------  |-----------|--------------|
| /24  | 255.255.255.0 | 256       | 254          |
| /16  | 255.255.0.0   | 65,536    | 65,534       |
| /28  |255.255.255.240| 16        | 14           |

---

### Task 4: Ports – The Doors to Services
1. What is a port? Why do we need them?
2. Document these common ports:

| Port | Service  |
|------|----------|
| 22   | SSH      |
| 80   | HTTP     |
| 443  | HTTPS    |
| 53   | DNS      |
| 3306 | MYSQL(DB)|
| 6379 | Redis    |
| 27017| MongoDB  |

3. Run `ss -tulpn` — match at least 2 listening ports to their services

---

### Task 5: Putting It Together
Answer in 2–3 lines each:
- You run `curl http://myapp.com:8080` — what networking concepts from today are involved?
- Your app can't reach a database at `10.0.1.50:3306` — what would you check first?

---

## Documentation

Create `day-15-networking-concepts.md` with:
- Your answers to each task
- Command outputs from `dig` and `ss`
- The filled CIDR table
- What you learned (3 key points)

---




*(Inspired by TechGuftgu DevOps Series)*

Today's learning was focused on the security layer of Linux. In DevOps, managing access is crucial for protecting servers and automation scripts.

---

## 🔍 Understanding the Permission String
When you run `ls -l`, you see something like:  
`drwxr-xr--`

| Position | Meaning | Examples |
| :--- | :--- | :--- |
| **1st Char** | File Type | `-` (File), `d` (Directory), `l` (Link) |
| **2-4 Char** | **Owner** Permissions | `rwx` (Read, Write, Execute) |
| **5-7 Char** | **Group** Permissions | `r-x` (Read, Execute only) |
| **8-10 Char** | **Others** Permissions | `r--` (Read only) |

---

## 🔢 The Numeric Method (The 4-2-1 Rule)
Linux assigns a number to each permission type. To set permissions, we just sum them up!

- **4** = Read (r)
- **2** = Write (w)
- **1** = Execute (x)
- **0** = No Permission

### **Common Permission Combinations:**
- **777** : `rwxrwxrwx` (Full access for everyone - *Risky!*)
- **755** : `rwxr-xr-x` (Owner can do everything, others can only Read/Execute)
- **644** : `rw-r--r--` (Standard file: Owner can Edit, others can only Read)
- **400** : `r--------` (Read-only for Owner - *Used for .pem keys*)

---

## 🛠️ Essential Commands

### 1. Changing Permissions (`chmod`)
- **Numeric:** `chmod 700 secret.txt`
- **Symbolic:** `chmod u+x script.sh` (Give execute power to User)

### 2. Changing Ownership (`chown`)
To change who "owns" the file:
- `sudo chown khushi:devops group_file.txt`  
*(Changes Owner to 'khushi' and Group to 'devops')*

### 3. Changing Group (`chgrp`)
To change only the group:
- `sudo chgrp developers project_folder`

---

## 💡 Key Takeaway from TechGuftgu
> "Permissions are the first line of defense in DevOps. Never give '777' permissions unless absolutely necessary for debugging, as it opens your system to everyone!"

- 📸 Lab Proof (Screenshot):
<img width="686" height="785" alt="Screenshot 2026-02-25 140510" src="https://github.com/user-attachments/assets/d6f7f410-7268-4f29-9231-7ce7e3fb40ed" />
<img width="701" height="813" alt="Screenshot 2026-02-25 140547" src="https://github.com/user-attachments/assets/c5d0ada6-b37f-4d82-8eb2-d41cb747db58" />

# Day 10  Notes:

![Lecture-10-Notes-pg1 jpg](https://github.com/user-attachments/assets/602c84d6-ddbc-41f2-b2bf-d77d8aad8be1)
![Lecture-10-Notes-pg2 jpg](https://github.com/user-attachments/assets/d2111cfd-49af-4839-82ab-9a420edb20bb)
