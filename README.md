# ssh-auto-ban-mail-reporter
Automatically ban failed SSH attackers and send a daily email report of banned IPs using Fail2Ban, msmtp, and cron.

# SSH Brute-Force Protection with Auto Ban and Daily Email Report

This project sets up a Linux-based automation system to:
- Automatically ban IP addresses that fail SSH login attempts
- Log banned IPs into a text file
- Email the log file daily using Gmail SMTP
- All using only configuration files and cron — no custom scripts required

---

## Features

- Auto-ban IPs after 3 failed SSH login attempts
- Log banned IPs to `/var/log/banned_ips.txt`
- Send daily email reports via Gmail SMTP
- Lightweight setup using Fail2Ban, msmtp, and cron
- No custom scripts — everything configured with built-in tools
- Easily enable or disable cron jobs

---

## Tools Used

| Tool      | Purpose                                      |
|-----------|----------------------------------------------|
| Fail2Ban  | Detects and bans brute-force IPs             |
| msmtp     | Sends email via Gmail SMTP                   |
| cron      | Automates the daily task                     |
| uuencode  | Attaches the log file to emails              |

---

## Setup Instructions

### 1. Install dependencies
```bash
sudo apt update
sudo apt install fail2ban msmtp mailutils sharutils
