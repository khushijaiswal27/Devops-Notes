### Day 13: Git Installation & GitHub Setup
In this session, I learned how to establish coordination between a Central Repository (GitHub) and Local Repositories (AWS EC2 Instances).

🛠️ Key Learnings & Tasks Performed:

1. EC2 Instance Configuration:-
   
- Launched two Linux EC2 instances in different regions (Mumbai and Singapore) to simulate a global development environment.
- Configured Security Groups to allow inbound traffic for SSH (Port 22) and HTTP (Port 80).

2. Git Installation on Amazon Linux:-
   
Updated the system packages using:
- sudo yum update -y

Installed Git on the AWS machine:
- sudo yum install git -y

Verified the installation and checked the version:
- git --version (Result: Version 2.23.3)

3. Git Global Configuration:-
   
* Configured global identity settings to track commits accurately:
- git config --global user.name "Your Name"
- git config --global user.email "your-email@example.com"

* Verified the settings using::-
- git config --list

4. GitHub Professional Setup:-
Created and verified a new GitHub account.
Explored the GitHub UI and understood the workflow of a Central Repository.

- 📸 Lab Proof (Screenshot):-
- <img width="1036" height="164" alt="Screenshot 2026-03-01 145053" src="https://github.com/user-attachments/assets/e83c569b-5605-4ecf-b328-58ab0531aa2a" />

  # Day13 notes-
![WhatsApp Image 2026-03-01 at 2 45 17 PM](https://github.com/user-attachments/assets/ef53d76b-8069-40d7-8829-4d1335f834fc)
