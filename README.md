Project described in https://github.com/01-edu/public/tree/master/subjects/devops/deep-in-system

Lessons from the project:

Partitions, name and hostname are configured during setup

static ip settings are handled in netplan config

ssh settings like port and remote root login disable are handled in sudo nano /etc/ssh/sshd_config

ufw is a good firewall

new users can be added with adduser command

sudo usermod -aG sudo newuser gives superpowers

su - newuser changes user

For SSH with key:

ssh-keygen -t rsa -b 4096 -C "new@yourdomain.com"

touch ~/.ssh/authorized_keys

chmod 600 ~/.ssh/authorized_keys

cat /path/to/jormakey.pub >> ~/.ssh/authorized_keys


copy key

and do chmod 600 /path/to/private/key

ssh -i /path/to/private/key user@server_ip_address -p 2222



To set up nami with readonly ftp and no ssh change user to /usr/sbin/nologin. 

For wordpress LEMP stack is good (linux ngnix php mysql)