
1. **Exam Network**
a. Enter all individual IPs
b. Enter all AD IPs (3 machines)
c. Enter private interface Ips for AD if applicable

2. **Service Enumeration**
a. Port scan results in tabular format in single record (TCP/UDP)
b. Heading for particular service enumeration, from where we found a
potential target software

3. **Initial Access**
a. Heading for which attack is exploited
b. Vuln explanation
c. Vuln Fix
d. Severity
e. Steps to Reproduce
i. Nmap command and output (screenshots)
ii. Searchsploit for exploit (ss)
iii. Exploit URL and modification (modified code)
iv. Payload generation
v. File transfer commands and ss
vi. Shell reception
vii. PoC Code

4. **Priv Esc**
a. Heading for issue exploited
b. Explanation
c. Fix
d. Severity
e. Steps to Reproduce
i. Commands and output with ss

5. **Post Exploitation**
a. Proof files screenshots
b. If Windows, use PsExec to get SYSTEM
c. Proof screenshot format:
i. Type proof.txt && whoami && ipconfig
d. If AD,
i. Mimikatz enum
ii. Groups Enum
iii. RDP screenshots
iv. Pivoting tools and commands

Exam Guide: https://help.offensive-security.com/hc/enus/articles/360040165632-OSCP-Exam-Guide
