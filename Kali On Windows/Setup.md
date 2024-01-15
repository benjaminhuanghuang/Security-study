

1. Turn WSL
Search for "Turn Windows features on or off"
Enable:
- Virtual Machine Platform
- Windows Subsystem for Linux

2. Open terminal as administrator
```bash
    wsl --update

    wsl --status

    wsl --set-default-version 2    # Set WSL2 as default on Win10
```

3. Install Kali Linux from Microsoft Store
Click open, input user name and password

4. Install tools
https://www.kait.org/tools/kali-meta
```bash
    sudo apt update
    sudo apt upgrade
    sudo apt install kali-linux-default
```
Change MAC automatically : No
Install Kismet "setuid root" : Yes, User: ben
Should non-superusers be able to capture packets? : Yes
sslh: standalone

Use Tasksel to install some metapackages
```bash
    sudo apt install tasksel
    sudo tasksel
```

## Setup SSH
Turn on SSH server in Kali VM
```bash
sudo service ssh start
```

Send the traffic to the host:2222 to port Kali VM:22 and allow the traffic through the Windows firewall
```bash
netsh interface portproxy add v4tov4 listenport=2222 listenaddress=0.0.0.0 connectport=22 connectaddress=localhost

netsh advfirewall firewall add rule name="WSL SSH" dir=in action=allow protocol=TCP localport=2222
```

Connect from Windows to Kali VM
```bash
ssh ben@172.24.80.1 -oPort=2222
```
