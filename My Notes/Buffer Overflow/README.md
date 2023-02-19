1. **Env setup**
		1. Mona working directory
		2. Run the binary/service
		3. Start immunity debugger as admin
		4. Attach the process
	
2. **Fuzzing**
	1. Identify crashing point
	2. Msf pattern create -l crashpoint

3. **Control EIP**
	1. Msf pattern offset -q EIP value
	2. Exploit code set offset and observe EIP value

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
