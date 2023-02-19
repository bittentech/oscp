
### **LFI:**
1. cat /etc/passwd
2. cat **service config** files
3. **Upload** a reverse shell and **locate** it
4. **Chain** with **file upload** (FTP/Redis/Web console)
5. Check /etc/**knockd**
6. **/proc/self/environ** (shell in user-agent)
7. **Apache log poisoning** (shell in **user-agent**)

### **CSRF**
1. Try to test **POST to GET** conversion and vice versa
9. **Send GET link** for sensitive action in any form that goes to another user
10. Generate **CSRF PoC** and **upload**

### **SQLi:**
1. **Pentestmonkey** cheatsheet
12. Try *admin'#* (**valid username**, see netsparker sqli cheatsheet)
13. Try *abcd' or 1=1;-*-
14. Use *UNION SELECT null,null*,.. instead of 1,2,.. to **avoid type conversion**
errors
15. For **mssql**,
	1. **xp_cmdshell**
	2. Use **concat** for listing 2 or more column data in one
16. For **mysql**,
	1. **udf**
	2. See banzai for UDF exploit issues
	3. try *a' or 1='1 -- -*
	4. A' union select *"<?php system($_GET['cmd']); ?>" into* **outfile**
	*"C:\xampp\htdocs\run.php" -- -'*
	

### **SSRF:**
1. Try to open **other subdomains**
22. Bypass restrictions with **case switching**
23. Use **other protocols**, file://, ftp (single line http like auth and access,
ftp://user:pass@server/path
24. Try **inline meta chars** $(),\`

### **Creds:**
1. **Default** username/passwords
26. Username as default **password as service name**
27. Default username and password **bruteforce**
28. Password **reuse**
29. **Null** password
30. Check **config files**
31. Generate custom wordlist with **cewl** (--with-numbers)
32. Use **hashcat rules** if hints point to it, (-r rule_path, **best64** should work)

### **File Upload:**
1. **Change mime** type
34. Add **image headers**
35. Add payload in **exiftool** **comment** and name file as file.php.png
 
### **SSTI:**
1. Identify with **tplmap.py**
38. Use SSTI -> RCE
39. Use SSTI **chart** to identify template engine
