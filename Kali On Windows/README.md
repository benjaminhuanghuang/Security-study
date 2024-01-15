# Introduction to Kali Linux and Windows Subsystem for Linux 
Scott Simpson, Apr 2022
https://www.linkedin.com/learning/introduction-to-kali-linux-and-windows-subsystem-for-linux


## WSL
- WSL1
Emulates a Linux kernel
Doesn't use virtualization
Fairly slow
Files on Windows filesystem

- WSL2
Uses a real Linux kernel
Uses virtualization
Faster than WSL1
Files in a virtual hard disk file
Default for Windows 11
WSL2 provides a system-managed virtual machine with connections to the host's filesystem and network. This Hyper-V virtual machine is managed by the system and tuned for use with Linux.


WSL provides command line tool wsl.exe to interact with the Linux subsystem.


## File
Linux home directory: /home/username (or ~)
Windows home directory: /mnt/c/Users/Username


Ignore files in Windows filesystem
```bash
find / -name ".profile" -print -o -path "/mnt/c" -prune 2>/dev/null
```
## Network
WSL visual machine is a client of a virtual network
• This network provides a private, dynamic IP address
• The WSL client can access the host's network and the internet
• Only the WSL client and Windows host can access the client

The host acts as the virtual network's router and DNS server

Ports opened by the WSL client are available on the host
• Port 8081 in WSL is localhost:8081 to the Windows host
• Access the service running on the Kali VM:3306 from the Windows host:
localhost:3306


The Kali VM doesn't have a firewall blocking access to ports


Find the IP address of the Windows host
```bash
cat /etc/resolv.conf
```

## Tools
What is Metasploit?
It is a tool that can run known exploits against remote hosts.
Metasploit's library of exploits can be useful for analyzing your own systems' vulnerabilities.


WSLg
Allows you rto run individual Linux GUI applications without a Linux desktop environment.

Kex
Launch a Win-Kex desktop
