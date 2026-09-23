Linux Security Lab
A practical Linux security lab built using Ubuntu to practice essential system administration and security concepts.
Objectives
Manage users and administrative privileges
Configure Linux file permissions
Set up and verify SSH
Configure the UFW firewall
Monitor and analyze system logs
1. User & Privilege Management
Created two users with different roles:
securityadmin: Administrative user with sudo privileges.
testuser: Standard user. This demonstrates basic account and privilege management in Linux.
2. File Permissions
Created a protected file and restricted its permissions using: chmod 600 secret.txt The file is accessible only by its owner for reading and writing.
3. SSH Configuration
Installed and enabled the OpenSSH server and verified that the service was running successfully.
sudo apt install openssh-server -y
sudo systemctl enable --now ssh
sudo systemctl status ssh SSH was configured to listen on port 22.
4. Firewall Configuration
Configured UFW (Uncomplicated Firewall) and allowed SSH connections.
sudo ufw allow ssh
sudo ufw enable
sudo ufw status verbose The firewall was configured with a default policy of denying incoming connections and allowing outgoing connections.
5. Log Monitoring
Reviewed SSH service logs and system warnings using journalctl.
sudo journalctl -u ssh --no-pager -n 20
sudo journalctl -p warning..alert --no-pager -n 20 This helped practice basic Linux log monitoring and troubleshooting.
Tools & Technologies: Ubuntu Linux • VirtualBox • OpenSSH • UFW Firewall • Linux Terminal • systemd / journalctl
Project Skills: Linux User Management • Privilege Management • File Permissions • SSH Configuration • Firewall Configuration • Log Monitoring • Basic Linux Security
