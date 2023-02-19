
1. Check **source code**
2. Service **default creds**
3. Don't forget to **enum** **domain names** (box.htb) and add to /etc/hosts
4. Apply **wildcard service** **nse** scripts at all discovered ports
5. Bust **subdirs** as well!
6. Check **Server: header**, might have exploit for server technology

### **Active Directory:**

1. If a user is found as hope sharp, try to create user list as:
	1. Hope
	10. Sharp
	11. H.sharp
	12. Hope.s
	13. Hopesharp
2. Use impacket GetADUsers to enum all users with valid creds

### **DNS:**
1. Use **nameserver** (hostname of the target) to enumerate subdomains (add entry to
/etc/hosts)
4. **host** -l nameserver IP
5. **Zone transfer** with dig
6. Check **https versions** of subdomain web pages

### **SMB:**
1. Try to **change client_min/client_max protocols** if disconnect error (-m/--option, NT1)
8. Try to run **NSE** scripts
9. Enumerate **version**

## **RPCCLient:**
1. **rpcclient** -U'user%pass' (or null) host
12. In prompt,
13. **Enumdomusers**
14. **Enumprinters**
15. **Enum***

### **Shellshock:**
1. Search for **executable extensions** (py,php,pl,sh,cgi,rb) inside **/cgi-bin/**
