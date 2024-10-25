# Fawn

1. Run [nmap](https://app.gitbook.com/s/DfkKonzwaN3qZbJhj85Q/enumeration#nmap "mention") to look for services: `nmap -T4 -sV <target_IP>`
2. FTP is running on port 21. Connect with `ftp -p <target_IP> <port>`
3. You can login with username = `anonymous` and no password (weak credentials)
4. Use `ls` to see the files on the server
5. Download `flag.txt` with get `flag.txt`
6. Exit the server using `quit`
7. Read the file using [nano](https://app.gitbook.com/s/DfkKonzwaN3qZbJhj85Q/#nano "mention") with `nano flag.txt`
