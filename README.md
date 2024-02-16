# CybersecurityAnalystPro
A collection of personal projects and hands-on labs performed during my certification.

## Table of Contents

Securing Linux
<br> Docker </br>

### Securing Linux
<br> This is where I learned Role Based Access Control to add users, groups, and secure my Linux terminal's vulnerabilities. </br>

### 1.) adduser
![linuxadduser](https://github.com/millywithnobrim/CybersecurityAnalystPro/assets/82410132/9731ad39-d69a-4a9c-85e2-bc92f1342a78)

The command 'sudo adduser test' adds a new user to the system with the name "test". It also created a new group with the same name as the user, adds the user to the group, and automatically request a new password for the user. Alternatively, you would have to use the 'sudo passwd [user's name]' command to set a password for the user.

![linuxadduser2](https://github.com/millywithnobrim/CybersecurityAnalystPro/assets/82410132/5021d254-796a-44ec-b17b-0da2c1196fe9)

Enter a new password and retype the password when prompted.

![linuxadduser3](https://github.com/millywithnobrim/CybersecurityAnalystPro/assets/82410132/47edc0a0-f5ba-4cbf-85ff-8329e123691e)

Add additional information and confirm with 'y'. Otherwise 'n' to edit the entered information.

### 2.) Manage user groups with groupadd
![usergroup](https://github.com/millywithnobrim/CybersecurityAnalystPro/assets/82410132/0f512787-2a41-4489-a752-815928cac9ff)

Added a new group to the system with the command 'sudo groupadd testusers'. "testusers" is the name of the group.

![usergroup2](https://github.com/millywithnobrim/CybersecurityAnalystPro/assets/82410132/af234d47-19d0-4eec-a550-b9188da2e46d)

The 'sudo usermod -a -G testusers test' command modifies the user "test" and adds them to the "testusers" group. The '-a' flag adds a user to a group without removing the user from other groups. The '-G' flag indicates you will be moving a user to a group which is then followed by the group name the user is being moved to.

![usergroup3](https://github.com/millywithnobrim/CybersecurityAnalystPro/assets/82410132/9940f023-314b-4e31-8d52-ce430f6be290)

The 'getent group' command lists all of the groups from databases stored in the system's text file. As you can see testusers group is displayed on the list.

### 3.) firewall
![fw](https://github.com/millywithnobrim/CybersecurityAnalystPro/assets/82410132/93f06c31-1969-48e7-8eb7-be28507f92fc)

Used the 'sudo ufw status' command to check if the firewall is active and the 'ufw enable' command to turn on the firewall. Then rechecked if the firewall is on.

![fw2](https://github.com/millywithnobrim/CybersecurityAnalystPro/assets/82410132/0343dbc1-d946-49df-95bf-740e7cb348ae)

The 'sudo ufw verbose' command outputs the default firewal rules. It is currently blocking all incoming traffic so nothing can connect to my device but it allows all outgoing traffic so I can connect to any external device. Also routed traffic is disabled so I cant use my device as a router.

![fw3](https://github.com/millywithnobrim/CybersecurityAnalystPro/assets/82410132/075dbff3-71fe-4c50-9e50-ac5342b5a923)

Finally, I used 'sudo ufw allow 22/tcp' and 'sudo ufw allow 80/tcp' to open and allow traffic to TCP ports 22 and 80 on my device. Port 22 allows remote devices to securely login to and communicate with a server via Secure Shell Protocol(ssh). Port 80 allows web browsing to work. Then I used 'sudo ufw deny 23' to close port 23 because although it allows remote login and communication with the server it doesnt encrypt data therefore it is best closed to keep my device more secure. I used 'verbose' again to ensure the new rules are active.

Follow me on LinkedIn:
<br><a href="https://www.linkedin.com/in/jamile2"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></img></a></br>
