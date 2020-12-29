
## Kali 
- Download Kali Virtual Box image
https://www.kali.org/downloads/


- Import image

File -> Import Appliance

Login : kali/kali or root/toor


## Metasploitable
Metasploitable is an intentionally vulnerable Linux virtual machine


## Virtual Box Network settings
- NAT: vm can access internet and be accessed from internet

- NAT Network: can not be accessed from internet


## update
```
  su

  apt-get update && apt-get upgrade -y && apt-get dist-upgrade -y
```

## Check version
```
  cat /etc/*{release,version}
```