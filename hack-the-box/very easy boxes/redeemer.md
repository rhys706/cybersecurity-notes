# Redeemer

1. Run [nmap](https://app.gitbook.com/s/DfkKonzwaN3qZbJhj85Q/enumeration#nmap "mention") to look for services: `nmap -T4 -sV <target_IP>`

{% hint style="warning" %}
By default `nmap` only checks the top 1000 ports! Sometimes this isn't enough and `-p-` needs to be used!
{% endhint %}

2. Run [nmap](https://app.gitbook.com/s/DfkKonzwaN3qZbJhj85Q/enumeration#nmap "mention") to look for services on all ports: `nmap -T4 -p- -sV <target_IP>`
3. Port 6379 is open and running a redis database

{% hint style="info" %}
If you know what port is open you can use `nmap` to scan a single port and provide all the associated data with `nmap -A -p <port> <target_IP>`
{% endhint %}

4. Connect to the redis database with `redis-cli -h <target_IP> -p <port>`
5. Use the `info` command to see more. You can see `db0` exists and has 4 keys at the bottom of the info returned
6. Select `db0` with `select 0`
7. Print the keys with `KEYS *`
8. Access the flag with `GET flag`
