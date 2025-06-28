# cyber-task-4
Windows Firewall Configuration
Cyber Security Internship

##  Objective
To understand and configure basic firewall rules on a Windows system — including blocking and allowing specific ports — and observe how firewall rules filter traffic.

---

##  Tool Used
- **Windows Defender Firewall with Advanced Security** (`wf.msc`)
- **Command Prompt** (to test port status using `telnet`)

---

##  Steps Performed

### 1. Opened Firewall Settings
Accessed the Windows Defender Firewall Advanced panel using `wf.msc`.

### 2. Listed Inbound Rules
Viewed existing inbound rules to understand current network traffic permissions.  

### 3. Blocked Port 23 (Telnet)
- Created a new **inbound rule** to block **TCP port 23**
- Applied the rule to all profiles: Domain, Private, and Public

### 4. Tested Block Rule
- Used the command: `telnet 127.0.0.1 23`
- Result: **Connection failed**, proving port was successfully blocked

### 5. Allowed Port 22 (SSH)
- Added an inbound rule to allow **TCP port 22**
- Useful in real-world Linux systems for SSH access
- Included for demonstration purposes on Windows

### 6. Removed Test Rules
- Deleted the custom Telnet and SSH rules after testing
- Restored original firewall state

---

##  Screenshots

| Step                          | File Name                          |
|-------------------------------|------------------------------------|
| Opened Firewall               | `1_firewall_opened.png`            |
| Block Port 23 - Rule Added    | `2_block_port_23_1.png`            |
| Block Port 23 - Rule Confirmed| `3_block_port_23_2.png`            |
| Telnet Test (Blocked)         | `4_telnet_test_blocked.png`        |
| Allow Port 22 - Rule Added    | `6_allow_port_22_1.png`            |
| Allow Port 22 - Rule Confirmed| `7_allow_port_22_2.png`            |
| Rule Removed                  | `8_rule_removed.png`               |

---

##  What I Learned

- How to use Windows Firewall Advanced Settings to create and remove rules
- How to block unused or insecure ports (e.g., Telnet on port 23)
- How to allow secure traffic (e.g., SSH on port 22)
- How to test firewall behavior using basic networking tools like `telnet`

---

## Notes

- Port 22 (SSH) is typically used on Linux systems. It was included here only for demonstration.
- Testing via `telnet` helps verify firewall behavior locally without external tools.
