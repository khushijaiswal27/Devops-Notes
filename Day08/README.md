
### Day 8: Package Management & System Utilities🚀
## Task 8
Today's goal is to **deploy a real web server on the cloud** and learn practical server management.

You will:
- Launch a cloud instance (AWS EC2 or Utho)
- Connect via SSH
- Install Nginx
- Configure security groups for web access (port 80 by default for nginx)
- Extract and save logs to a file
- Verify your webpage is accessible from the internet

This is real DevOps work - exactly what you'll do in production.

---

## Expected Output
By the end of today, you should have:

1. A markdown file named: `day-08-cloud-deployment.md`
2. Screenshots showing:
   - SSH connection to your server
   - Nginx welcome page accessible from browser
   - Log file contents
3. The log file: `nginx-logs.txt`

---

## Prerequisites
- AWS account (Free Tier) OR Utho account
- Basic understanding of Linux commands (Days 1-7)
- SSH client (Terminal on Mac/Linux, PuTTY on Windows)

---

## Guidelines

### Part 1: Launch Cloud Instance & SSH Access (15 minutes)

**Step 1: Create a Cloud Instance**


**Step 2: Connect via SSH**


---

### Part 2: Install Docker & Nginx (20 minutes)

**Step 1: Update System**


**Step 3: Install Nginx**

**Verify Nginx is running:**

---

### Part 3: Security Group Configuration (10 minutes)

**Test Web Access:**
Open browser and visit: `http://<your-instance-ip>`

You should see the **Nginx welcome page**!

📸 **Screenshot this page** - you'll need it for submission

---

### Part 4: Extract Nginx Logs (15 minutes)

**Step 1: View Nginx Logs**

**Step 2: Save Logs to File**

**Step 3: Download Log File to Your Local Machine**
```bash
# On your local machine (new terminal window)
# For AWS:
scp -i your-key.pem ubuntu@<your-instance-ip>:~/nginx-logs.txt .

# For Utho:
scp root@<your-instance-ip>:~/nginx-logs.txt .
```

---


## Documentation Template

Create your `day-08-cloud-deployment.md` with this structure:

## Commands Used
[List the key commands you used]

## Challenges Faced
[Describe any issues and how you solved them]

## What I Learned
[3-5 bullet points of key learnings]

---


## Why This Matters for DevOps

This exercise teaches you:
- **Cloud infrastructure provisioning** - launching and configuring servers
- **Remote server management** - SSH, security, access control
- **Service deployment** - installing and running applications
- **Log management** - accessing and analyzing logs
- **Security** - configuring firewalls and security groups

These are core skills for any DevOps engineer working in production.

---


🚀 Topics Covered:

1. **Network & Host Info:**
   - `hostname`: To check the system name.
   - `ifconfig` or `hostname -i`: To find the IP address of the instance.
2. **Package Management (YUM):**
   - `sudo yum install httpd -y`: To install Apache Web Server.
   - `sudo yum update -y`: To update all packages.
   - `sudo yum remove httpd`: To uninstall a package.
3. **Service Management:**
   - `sudo systemctl start httpd`: To start the web server.
   - `sudo systemctl status httpd`: To check if the server is active (running).
   - `sudo chkconfig httpd on`: To enable the service on boot.
4. **Advanced File Operations:**
   - `grep "text" filename`: To search for a specific word in a file.
   - `sort filename`: To sort the file content alphabetically.
   - `tree`: To view the directory structure in a visual format.
  
   - 📸 Lab Proof (Screenshot):-
   - 
<img width="833" height="436" alt="Screenshot 2026-02-20 220724" src="https://github.com/user-attachments/assets/8e4b89be-8988-4b91-8b87-531a34a7acb1" />

<img width="684" height="160" alt="Screenshot 2026-02-20 221036" src="https://github.com/user-attachments/assets/f76dfcef-4020-42a2-84c5-e0440398c6d8" />

<img width="946" height="1011" alt="Screenshot 2026-02-20 221116" src="https://github.com/user-attachments/assets/db25139c-3ecd-4c79-936e-d3b9595a7034" />

<img width="768" height="921" alt="Screenshot 2026-02-20 221137" src="https://github.com/user-attachments/assets/77726ebb-9f1e-4cea-a2d7-f4d5968db2a2" />

# Day 8 Notes:
![Lecture-08-Notes-pg1 jpg](https://github.com/user-attachments/assets/f5c443c4-1631-4879-b8f8-7869fd940b00)
![Lecture-08-Notes-pg2 jpg](https://github.com/user-attachments/assets/206229d3-37fe-4d09-bfca-8b69b3811583)
![Lecture-08-Notes-pg3 jpg](https://github.com/user-attachments/assets/5d7949a1-96d6-4136-925f-7d4097b1a2ad)
