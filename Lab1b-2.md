This lab focuses on secure file permission and user group management in Linux. Students will create users, assign group permissions, and test access control settings for different user scenarios. This is a foundational skill for managing secure multi-user systems.

Creating Users
---
Created Alice, Bob and Mallory using "sudo adduser alice"
Verifying Creation with "cat /etc/passwd"

<img width="290" height="71" alt="image" src="https://github.com/user-attachments/assets/41d0ec21-06f1-41a0-8f1f-c7681a206e2a" />

Next creating a group with the command "sudo groupadd sharedgroup"

To check if the group is successfully created we can used the "getent group sharedgroup" to verify

Create a directory: "sudo mkdir/home/shared" 

<img width="341" height="121" alt="image" src="https://github.com/user-attachments/assets/1205bb47-c66b-4cb0-83bd-1651fa91ad93" />

<img width="1246" height="1134" alt="image" src="https://github.com/user-attachments/assets/b5258966-23de-4630-9c5d-4cedbc323798" />

