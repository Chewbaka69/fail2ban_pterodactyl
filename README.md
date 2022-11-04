# fail2ban_pterodactyl
A fail2ban filter for wings daemon, the service of pterodactyl panel, to secure the SFTP bruteforcing

## Installation

First of all you need to have install the systemd python extension.
```bash
apt install python-systemd
```
or
```bash
apt install python3-systemd
```

And after you need to copy the file `pterodactyl-sftp.conf` to `/etc/fail2ban/filter.d/`

And after copy the code below to your jail configuration file.
For debian ex: `/etc/fail2ban/jail.d/defaults-debian.conf`

```bash
[pterodactyl-sftp]
enabled = true
maxretry = 3
findtime = 3600
bantime = -1
backend  = systemd
```
