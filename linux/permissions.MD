# Groups
C | A
-|-
groups | Groups of current user
groups \<user\> | Groups of the user
cat /etc/group | Show all groups
sudo groupadd \<group\> | Add a new group
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

# Add common shared folder fro users
C | A
-|-
sudo groupadd sharedgroup | Create a group that all users will belong to
sudo usermod -aG sharedgroup A | Add user A to this group
sudo usermod -aG sharedgroup B | Add user B to this group
sudo usermod -aG sharedgroup C | Add user C to this group
sudo mkdir -p /srv/shared | Create shared folde
sudo chown root:sharedgroup /srv/shared | Make the group the owner of the directory
sudo chmod 2770 /srv/shared | Full access for owner and group, none for others. setgid 2 - new files and subfolders inherit permissions
