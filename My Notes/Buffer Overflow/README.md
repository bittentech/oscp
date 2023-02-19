1. **Env setup**
		a. Mona working directory
		b. Run the binary/service
		c. Start immunity debugger as admin
	d. Attach the process
	
2. **Fuzzing**
a. Identify crashing point
b. Msf pattern create -l crashpoint

3. **Control EIP**
a. Msf pattern offset -q EIP value
b. Exploit code set offset and observe EIP value

4. **Finding bad chars**
a. Generate all bad chars with python
b. Generate bad chars with mona bytearray
c. Mona compare with esp address (or follow esp dump manually)
d. Remove next bad char from payload, fire
e. Generate new mona bytechar with excluded bad char
f. Repeat steps e and f for all bad chars until unmodified

5. **Find jump esp**
a. Find with mona
b. Select address with no money protections (jmp esp)

6. **Generate shellcode**
a. Msfvenom -f py EXITFUNC=thread
b. Exclude all bad chars with -b
c. -v exploit script payload variable name

7. **Grand Finale!**
a. Prepend NOPS! (4/8/16)
b. Buffer = prefix + overflow + retn + padding + payload + postfix

https://github.com/Tib3rius/Pentest-Cheatsheets/blob/master/exploits/bufferoverflows.rst
