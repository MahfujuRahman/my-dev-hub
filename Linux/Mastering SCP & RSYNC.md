# 🧠 Mastering SCP & RSYNC: From Beginner to Pro

This guide will help you **master `scp`, `rsync`, and related tools** to transfer files and directories between **Linux↔Linux** and **Linux↔Windows**. Each section includes clear examples and command explanations.

---

## 📘 PART 1: Basics of File Transfer

### 1.1 What is `scp`?

* `scp` = **secure copy**
* Uses **SSH** to securely transfer files between machines.
* Works for both files and folders (with `-r` flag).

### 1.2 SCP Basic Syntax

```bash
scp [options] source destination
```

### 1.3 Examples: Linux ↔ Linux

#### 🔹 Local to Remote

```bash
scp file.txt user@192.168.1.100:/home/user/
```

* `file.txt`: The file to send.
* `user@192.168.1.100`: The username and IP of the remote Linux system.
* `/home/user/`: Destination folder on the remote server.

#### 🔹 Remote to Local

```bash
scp user@192.168.1.100:/home/user/file.txt /home/localuser/
```

#### 🔹 Copy Folder Recursively

```bash
scp -r my_folder user@192.168.1.100:/home/user/
```

* `-r`: Recursive, used for copying directories.

---

## 📘 PART 2: Advanced SCP Usage

### 2.1 Use a Custom SSH Port

```bash
scp -P 2222 file.txt user@host:/path/
```

* `-P 2222`: Use port 2222 instead of the default SSH port (22).

### 2.2 Copy Multiple Files

```bash
scp file1.txt file2.txt user@host:/destination/
```

### 2.3 Copy with Wildcards

```bash
scp *.txt user@host:/destination/
```

> ❗ SCP is fast and simple, but **rsync** is more efficient for backups and syncing.

---

## 📗 PART 3: What is `rsync`?

* `rsync` = **Remote Synchronization**
* Only transfers changed files → **efficient for backups**.
* Supports local and SSH-based remote transfer.

### 3.1 Basic Syntax

```bash
rsync [options] source destination
```

### 3.2 Examples: Linux ↔ Linux

#### 🔹 Local to Remote

```bash
rsync -avz my_folder/ user@192.168.1.100:/home/user/
```

* `-a`: Archive (preserve permissions, timestamps, links, etc.)
* `-v`: Verbose
* `-z`: Compress data during transfer

#### 🔹 Remote to Local

```bash
rsync -avz user@192.168.1.100:/home/user/remote_folder/ /home/localuser/
```

#### 🔹 Transfer Single File

```bash
rsync -avz file.txt user@host:/destination/
```

---

## 📙 PART 4: Intermediate Rsync Usage

### 4.1 Use SSH with Custom Port

```bash
rsync -avz -e "ssh -p 2222" my_folder/ user@host:/path/
```

### 4.2 Exclude Files or Folders

```bash
rsync -av --exclude="*.log" my_folder/ user@host:/path/
```

### 4.3 Delete Remote Files No Longer Present Locally

```bash
rsync -av --delete my_folder/ user@host:/path/
```

### 4.4 Dry Run (Preview changes)

```bash
rsync -av --dry-run my_folder/ user@host:/path/
```

---

## 📘 PART 5: Transferring Files Linux ↔ Windows

### 5.1 Option 1: Windows Has OpenSSH Server

Use normal `scp` or `rsync`:

```bash
scp file.txt user@windows_ip:/c/Users/yourname/Desktop/
```

```bash
rsync -avz file.txt user@windows_ip:/c/Users/yourname/Desktop/
```

> Windows path becomes `/c/Users/yourname/...`

### 5.2 Option 2: Use Samba or SMB

1. Create shared folder in Windows
2. Mount in Linux:

```bash
sudo mount -t cifs //windows_ip/shared /mnt/windows -o username=winuser
```

3. Copy files:

```bash
cp file.txt /mnt/windows/
```

### 5.3 Option 3: Windows with WSL (Windows Subsystem for Linux)

From Linux:

```bash
rsync -avz file.txt user@windows_ip:/mnt/c/Users/yourname/Desktop/
```

---

## 📗 PART 6: Automation & Scheduling

### 6.1 Backup Script Example

```bash
#!/bin/bash
rsync -avz /home/user/my_project/ user@remote:/backups/my_project/
```

### 6.2 Add to Crontab

```bash
crontab -e
```

Add:

```bash
0 * * * * /home/user/backup.sh
```

> Runs every hour

---

## 📙 PART 7: Related Tools

### 🔸 `sftp`: Secure File Transfer Protocol

```bash
sftp user@host
sftp> put file.txt
sftp> get file.txt
```

### 🔸 `sshfs`: Mount Remote Directory via SSH

```bash
sshfs user@host:/remote/dir /mnt/remote
```

Then you can use regular file commands:

```bash
cp file.txt /mnt/remote/
```

### 🔸 GUI Tools

* **FileZilla**: Easy drag-n-drop interface
* **WinSCP**: Windows file transfer tool

---

## ✅ Summary Table

| Level        | Topic                             | Tools & Commands                              |
| ------------ | --------------------------------- | --------------------------------------------- |
| Beginner     | Securely copy files/folders       | `scp`, `rsync -avz`                           |
| Intermediate | Exclusions, custom ports, syncing | `--exclude`, `--delete`, `--dry-run`          |
| Advanced     | Automate, cross-OS, remote mounts | `cron`, `sshfs`, `samba`, `sftp`, `GUI tools` |

---

Would you like a practice challenge set or example projects next?
