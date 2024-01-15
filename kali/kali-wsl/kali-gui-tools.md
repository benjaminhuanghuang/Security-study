
Using Kali GUI tools in a WSL session is using the WSLg feature of Windows 11. 
Which can launch individual Linux GUI applications without a Linux desktop environment.

1. Make sure WSL is updated
    ```bash
    wsl --update
    ```
2. Enter the Kali WSL session
    ```bash
    kali
    ```
3. Setup wireshark in Kali
    ```bash
    # Add user to wireshark group
    sudo usermod -aG wireshark ben

    exit
    ```
4. Run wireshark in windows host
    ```bash
    wslg wireshark
    ```
5. Or run wireshark GUI in Kali
    ```bash
    wireshark
    ```

## References
Scott Simpson, Apr 2022
https://www.linkedin.com/learning/introduction-to-kali-linux-and-windows-subsystem-for-linux
