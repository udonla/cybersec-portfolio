Linux User & Process Management
/etc/passwd

This file stores information about every user account.

Example:

student:x:1000:1000:Student:/home/student:/bin/bash

Fields:

Username
Password placeholder (x)
User ID (UID)
Group ID (GID)
User information
Home directory
Default shell

Important:

It does NOT store the actual password.
Everyone can usually read this file.

Check it:

cat /etc/passwd
/etc/shadow

This file stores the encrypted (hashed) passwords.

Example:

student:$6$...

Important:

Only root can read it.
Passwords are stored as hashes, not plain text.
It also stores password expiration information.

Check it:

sudo cat /etc/shadow
Useful User Commands
sudo adduser alice
sudo passwd alice
sudo usermod -aG sudo alice
id alice
whoami
Process Management

View processes:

ps aux

Live process monitor:

top

Kill by PID:

kill 1234

Kill by name:

killall firefox
Package Management

Install:

sudo apt install nginx

Update package list:

sudo apt update

Upgrade packages:

sudo apt upgrade

Remove:

sudo apt remove nginx
Services

Start:

sudo systemctl start apache2

Stop:

sudo systemctl stop apache2

Status:

systemctl status apache2
