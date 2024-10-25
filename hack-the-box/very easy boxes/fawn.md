# Fawn

1. Run nmap to look for services:

* `nmap -T4 -Pn -sV <target_IP>`

2. FTP is open on port 21. We can connect without a password with:

> FTP username: anonymous

3. Log in with some poor credentials

* `ftp -p <IP_address> <port>`

4. List files with `ls`
5. Download the flag to your current directory with `get <filename>`

> Flag: 035db21c881520061c53e0536e44f815
