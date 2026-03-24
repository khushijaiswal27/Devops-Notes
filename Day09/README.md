### Day 9: Linux User Management & File Linking

## 👤 User & Group Administration
* **`sudo useradd [username]`**: Used to create a new user in the system.
* **`sudo groupadd [groupname]`**: Used to create a new group.
* **`cat /etc/passwd`**: Used to view the list of all users and their configuration.
* **`cat /etc/group`**: Used to view the list of all existing groups.
* **`sudo gpasswd -a [user] [group]`**: Used to add an existing user to a specific group.

## 🔗 Linking in Linux:-

### 1. Soft Link (Symbolic Link)
Acts as a shortcut to the original file. If the original file is deleted, the link becomes broken.
* **Command:** `ln -s [source_file] [link_name]`
### 2. Hard Link
Acts as a mirror of the file data. Even if the original file is deleted, the data remains accessible.
* **Command:** `ln [source_file] [link_name]`

## 📦 Archiving & Downloading
* **`tar -cvf`**: Used to bundle multiple files into a single "tarball" archive.
* **`gzip`**: Used to compress files to reduce their storage size.
* **`wget [URL]`**: A utility to download files directly from the internet via the command line.

  
# Day 9  Notes:
![Lecture-09-Notes-pg1 jpg](https://github.com/user-attachments/assets/ff1ea050-51cf-43e1-95d9-dcfd84abe68a)
![Lecture-09-Notes-pg2 jpg](https://github.com/user-attachments/assets/8004c1d9-b38c-4985-b402-b7c85c2d5088)
