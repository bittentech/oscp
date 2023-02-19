
### **Dirsearch:**
- *dirsearch -u URL -l WORDLIST -x EXCLUDE_STATUES -I INCLUDE_STATUSES -e EXTENSION -t THREADS*

### **Hydra:**
- *hydra -L USER_FILE -P PASS_FILE -t THREADS -e nsr -s PORT protocol://IP:PORT*

### **SSH:**
- *ssh -o "ServerAliveInterval 60" server_address -I priv_key*

### **nc Port scan:**
- *nc -z -w 1 -v IP PORTRANGE (start-end) 2>&1 | grep -I succeeded*

### **Curl:**
- *curl -A/-H [header] [url]*

### **Crackmapexec:**
- *crackmapexec type (winrm/smb) -u user/userfile -p pass/passfile IP*

### **SNMPwalk:**
- *snmpwalk -v 2c -c public [IP] [OID/MIB]*

### **Wfuzz:**
1. **Subdomain enum:**
	1. *wfuzz -u main_host -w wordlist -H FUZZ.host.com --sc 200 --hc 302*

### Dirbuster:
1. **Common extensions** php/asp/do/html/txt/
18. Scan **subdirectories** for services under a directory
19. Also use dirb/**big.txt** or multiple wordlists
20. Scan for **all http ports**

### **GetNPUsers**
1. **AS-REP roasting**
a. *GETNPUsers.py -no-pass -dc-ip IP domain/user or --users-list list*

### **Wmic:**
1. **Weak service permissions**
	1. *wmic service list brief*
2. **Unquoted service paths**
	1. *wmic service get name,pathname,startmode | findstr /I "auto"*

### **SC**
1. **Unquoted service paths**
	1. *sc query*
	2. *sc qc service name*

### **Evil-winrm:**
1. **Pass-The-Hash**
	1. *evil-winrm -I host-ip -u user -H nthash*
2. **Download files:**
	1. *evil-winrm download file_name*

### **Impacket-psexec**
1. **Pass the hash**
	1. *impacket-psexec -hashes lm:nt username@ip*
