# Task-4-Firewall-UFW
This repository contains Task 4 of my Cyber Security Internship, which demonstrates basic firewall configuration using UFW on Kali Linux. The task involves allowing and denying specific ports, testing firewall behavior, and restoring system settings. Screenshots and a detailed README are included.

# Task 4 - Configure and Use Firewall on Linux (UFW)

## 👨‍💻 Performed by: Naman Patil

## 🎯 Objective:
Configure and test basic firewall rules using UFW on Kali Linux to allow/block specific ports (22, 23) and verify the changes.

---

## 🛠️ Tools Used:
- Kali Linux
- UFW (Uncomplicated Firewall)
- Terminal Commands

---

## 🧪 Steps Performed:

### 1. Install UFW:
```bash
sudo apt install ufw
```

### 2. Enable UFW:
```bash
sudo ufw enable
sudo ufw status
sudo ufw status verbose
```

### 3. Allow SSH (Port 22):
```bash
ufw allow 22
```

### 4. Deny Telnet (Port 23):
```bash
ufw deny 23
```

### 5. Verify Rules with Numbers:
```bash
ufw status numbered
```

### 6. Test Telnet Access:
```bash
telnet localhost 23
```
✅ Output: `Connection refused` — means port is blocked.

### 7. Delete the Rule (Restore State):
```bash
ufw delete deny 23
```

---

## 📷 Screenshots Included:
- `enable-ufw.png` – UFW installed and enabled
- `allow-22.png` – Rule to allow port 22
- `deny-23.png` – Rule to deny port 23
- `final-status.png` – Status showing applied rules
- `restore-original-state.png` – Telnet test + rule deleted

---

## ✅ Outcome:
- Understood how to manage basic firewall rules on Linux.
- Practically tested rules for both allowing and denying traffic.
- Restored system to original state after testing.

---

## 📘 Learnings:
- UFW simplifies iptables rule management.
- Telnet is insecure and should be blocked.
- Port-based access control is essential in cyber security.
