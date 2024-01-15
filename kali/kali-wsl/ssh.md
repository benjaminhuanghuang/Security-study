# Access Kali from Windows via SSH


## Turn on SSH server in Kali VM
```bash
sudo service ssh start
```

## Send the traffic to the host:2222 to port Kali VM:22 
In windows host, run as administrator
```bash
netsh interface portproxy add v4tov4 listenport=2222 listenaddress=0.0.0.0 connectport=22 connectaddress=localhost
```
## allow the traffic through the Windows firewall
In windows host, run as administrator
```bash
netsh advfirewall firewall add rule name="WSL SSH" dir=in action=allow protocol=TCP localport=2222
```

## Connect Kali VM
```bash
ssh ben@172.24.80.1 -oPort=2222
```


## References
Scott Simpson, Apr 2022
https://www.linkedin.com/learning/introduction-to-kali-linux-and-windows-subsystem-for-linux
