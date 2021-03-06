# BruteSpray

Created by: Shane Young/@x90skysn3k && Jacob Robles/@shellfail 

Inspired by: Leon Johnson/@sho-luv

#### Version - 1.3

# Demo

https://youtu.be/C-CVLbSEe_g

# Description
BruteSpray takes nmap GNMAP output and automatically brute-forces services with default credentials using Medusa. BruteSpray can even find non-standard ports by using the -sV inside Nmap.  

<img src="http://i.imgur.com/k9BDB5R.png" width="500">



# Usage
First do an nmap scan with '-oA nmap.gnmap'.

Command: ```python brutespray.py -h```

Command: ```python brutespray.py --file nmap.gnmap```

<img src="http://i.imgur.com/jDzT0sT.png" width="450">

## Examples

#### Using Custom Wordlists:

```python brutespray.py --file nmap.gnmap -U /usr/share/wordlist/user.txt -P /usr/share/wordlist/pass.txt --threads 5 --hosts 5```

#### Brute-Forcing Specific Services:

```python brutespray.py --file nmap.gnmap --service ftp,ssh,telnet --threads 5 --hosts 5```

#### Specific Credentials:
   
```python brutespray.py --file nmap.gnmap -u admin -p password --threads 5 --hosts 5```

#### Continue After Success:

```python brutespray.py --file nmap.gnmap --threads 5 --hosts 5 -c```

# Supported Services

* ssh
* ftp
* telnet
* vnc
* mssql
* mysql
* postgresql
* rsh
* imap
* nntp
* pcanywhere
* pop3
* rexec
* rlogin
* smbnt
* smtp
* snmp
* svn
* vmauthd

# Changelog
* v1.3
    * added the ability to stop on success
    * added the ability to reference custom userlists and passlists
    * added the ability to specify specific users & passwords
