
1. Use **seclists/Names/names.txt** for finding names/user enum
2. Password **spraying** (crackmapexec, smb winrm, rdp)

**Tools:**
1. **John**
a. --format for hash format
b. --wordlist for pass list
2. **Hashcat**
a. -a 0 **(brute force)**
b. -m **attack_mode** (hashcat --help)
c. --force (for **non native GPU** support)
d. --rule (**mangling** rules)
