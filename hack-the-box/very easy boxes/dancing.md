# Dancing

1. Run [nmap](https://app.gitbook.com/s/DfkKonzwaN3qZbJhj85Q/enumeration#nmap "mention") to look for services: `nmap -T4 -sV <target_IP>`
2. Port 445 is open and typically runs SMB.&#x20;
3. We can list SMB shares with `smbclient -L <target_IP>` (have to enter your kali password)
4. You can see the `WorkShares` share is not password protected because it does not have a `$`&#x20;
5. Open it with `smbclient \\\\<target_IP>\\WorkShares`
6. Read directory contents with `ls` and move around with `cd` (use `cd ..` to go up a level)
7. Use `get` to download the flag once you find it
8. Use `quit` to exit the smbclient
9. Use `nano` to read the downloaded file
