# fail2ban_pterodactyl
A fail2ban filter for wings daemon, the service of pterodactyl panel, to secure the SFTP bruteforcing

## Installation

Copy the code below to your jail configuration file.

```bash
[pterodactyl-sftp]
enabled = true
maxretry = 3
findtime = 3600
bantime = -1
```
