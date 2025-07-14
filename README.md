# Linux Backup Automation Script

This project is part of the **IBM Data Engineer Certification** and demonstrates the use of Linux shell scripting, file permissions, cron jobs, and basic automation to back up encrypted password files updated.

In this project scenario, I am a lead Linux developer at the top-tech company ABC International Inc. As one of ABC Inc.'s most trusted Linux developers, I have been tasked with creating a script called backup.sh which runs every day and automatically backs up any encrypted password files that have been updated in the past 24 hours.

## 📂 Project Overview

The main script `backup.sh` is designed to:

- Accept two arguments: a target directory and a destination directory
- Find files updated in the past 24 hours in the target directory
- Archive and compress those files into a `.tar.gz` backup
- Move the backup archive to the destination directory
- Automate this process using a cron job (every 24 hours)

## 🔧 Usage

```bash
./backup.sh /path/to/target /path/to/destination
```

## ✏️Example :
```bash
./backup.sh /home/project/important-documents /home/project
```
## 🕑 Cron Job Setup
To schedule the script to run every day at midnight:
```bash
crontab -e
```
Add the following line:
```cron
0 0 * * * /usr/local/bin/backup.sh /home/project/important-documents /home/project
```
Start and stop the cron service manually (for Theia virtual lab):
```
sudo service cron start
sudo service cron stop
```

## 📁 File Structure
```
linux-backup-automation/
├── backup.sh
├── README.md
├── screenshots/
│   ├── 01-Set_Variables.jpg
│   ├── 02-Display_Values.jpg
│   └── ... other screenshots
```
## ✅ Requirements
- Linux shell environment
- Bash (v4+)
- cron service
- Permissions to access and move files
