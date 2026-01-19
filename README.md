# Operating-System-Security-Fundamentals

🛡️ Operating System Hardening Report
1. Environment Setup
- Linux VM (Ubuntu via VirtualBox):
- Installed Ubuntu 22.04 LTS in VirtualBox with 2GB RAM and 20GB disk.
- Created a safe, isolated environment for testing security configurations.
- Windows 11 Security Settings:
- Verified Windows Defender and Firewall are enabled.
- Accessed Local Security Policy for account and permission management.

2. User Accounts & Access Control
- Linux:
- Created new user: sudo adduser testuser.
- Verified groups: groups testuser.
- Default role: Standard User.
- Windows:
- Added new account via Settings → Accounts → Family & other users.
- Assigned roles:
- Administrator: Full system privileges.
- Standard User: Restricted privileges for safer daily use.

3. File Permissions
- Linux:
- Checked permissions: ls -l file.txt.
- Modified permissions: chmod 755 script.sh.
- Changed ownership: sudo chown testuser:testuser file.txt.
- Windows:
- Adjusted file permissions via Properties → Security tab.
- Configured Read/Write/Execute access for specific users.

4. Administrator vs Standard User Privileges
- Administrator (root/sudo in Linux, Admin in Windows):
- Can install software, modify system files, manage accounts.
- Standard User:
- Limited access, safer against malware or accidental system changes.
- Best Practice: Use standard accounts for daily work; elevate only when necessary.

5. Firewall Configuration
- Linux (UFW):
- Enabled firewall: sudo ufw enable.
- Allowed SSH: sudo ufw allow 22/tcp.
- Verified status: sudo ufw status.
- Windows Firewall:
- Confirmed firewall is ON for all network profiles.
- Configured inbound/outbound rules for specific applications.

6. Processes & Services
- Linux:
- Listed processes: ps aux, top.
- Listed services: systemctl list-units --type=service.
- Windows:
- Checked processes via Task Manager.
- Reviewed services via services.msc.

7. Disabling Unnecessary Services
- Linux:
- Stopped unused service: sudo systemctl stop apache2.
- Disabled at boot: sudo systemctl disable apache2.
- Windows:
- Disabled unused services in Services Manager (e.g., Remote Registry).
- Reduced attack surface by limiting active background services.

8. Best Practices for OS Hardening
- Apply Principle of Least Privilege.
- Keep OS and applications patched and updated.
- Enable firewall and antivirus at all times.
- Disable unused accounts and services.
- Enforce strong passwords + MFA.
- Enable logging and auditing to monitor system activity.
- Regularly review running processes for anomalies.

✅ Conclusion
This lab demonstrated the fundamentals of OS hardening:
- Controlled user privileges.
- Secured files and directories.
- Enabled firewalls.
- Monitored and minimized active services.
- Documented best practices.
Together, these measures significantly reduce the attack surface and improve the overall security posture of both Linux and Windows systems.
