
### **Exam Network**
1. Enter all individual IPs
2. Enter all AD IPs (3 machines)
3. Enter private interface Ips for AD if applicable

###  **Service Enumeration**
1. Port scan results in tabular format in single record (TCP/UDP)
2. Heading for particular service enumeration, from where we found a
potential target software

### **Initial Access**
1. Heading for which attack is exploited
2. Vuln explanation
3. Vuln Fix
4. Severity
5. Steps to Reproduce
	1. Nmap command and output (screenshots)
	2. Searchsploit for exploit (ss)
	3. Exploit URL and modification (modified code)
	4. Payload generation
	5. File transfer commands and ss
	6. Shell reception
	7. PoC Code

### **Priv Esc**
1. Heading for issue exploited
2. Explanation
3. Fix
4. Severity
5. Steps to Reproduce
6. Commands and output with ss

### **Post Exploitation**
1. Proof files screenshots
2. If Windows, use PsExec to get SYSTEM
3. Proof screenshot format:
	1. Type proof.txt && whoami && ipconfig
4. If AD,
	1. Mimikatz enum
	2. Groups Enum
	3. RDP screenshots
	4. Pivoting tools and commands

Exam Guide: https://help.offensive-security.com/hc/enus/articles/360040165632-OSCP-Exam-Guide
