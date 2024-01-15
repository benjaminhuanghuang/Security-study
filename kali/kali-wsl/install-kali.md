

1. Turn on WSL

    Search for "Turn Windows features on or off"
    Enable:
    - Virtual Machine Platform
    - Windows Subsystem for Linux

2. Update WSL

    Open terminal as administrator
    ```bash
        wsl --update

        wsl --status

        wsl --set-default-version 2    # Set WSL2 as default on Win10
    ```

3. Install Kali Linux from Microsoft Store
Click open, input user name and password

4. Install tools in Kali
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
