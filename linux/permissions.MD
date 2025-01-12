# Groups
C | A
-|-
groups | Groups of current user
groups \<user\> | Groups of the user
cat /etc/group | Show all groups
sudo adduser \<user\> dialout | Add \<user\> to dialout group (to access serial ports) (need to log out & log back to take effect)

# Users
C | A
-|-
sudo adduser \<username\> | Create new user (should be lowercase)
sudo usermod -aG sudo \<username\> | Give superpowers
sudo deluser --remove-home \<username\> | Delete user (with home directory)
sudo --list | Show which commands user can run (sudoers?)
sudo adduser \<user\> sudo | Add user to sudoer list
sudo delluser <user> sudo | Remove user from sudoers
 
# User passwords
C | A
-|-
sudo passwd \<usr\> | Set password
sudo passwd -S \<usr\> | View password
sudo passwd -l \<usr\> | Lock user
sudo passwd -u \<usr\> | Unlock user

