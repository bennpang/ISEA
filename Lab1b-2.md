This lab focuses on secure file permission and user group management in Linux. Students will create users, assign group permissions, and test access control settings for different user scenarios. This is a foundational skill for managing secure multi-user systems.

Creating Users
---
Created Alice, Bob and Mallory using "sudo adduser alice"

Sample output of the user creation process

<img width="165" height="65" alt="image" src="https://github.com/user-attachments/assets/a7616460-77e4-45d8-bd61-20bcd5069360" />

Verifying Creation with "cat /etc/passwd"

<img width="290" height="71" alt="image" src="https://github.com/user-attachments/assets/41d0ec21-06f1-41a0-8f1f-c7681a206e2a" />

Next creating a group with the command "sudo groupadd sharedgroup"

To check if the group is successfully created we can used the "getent group sharedgroup" to verify

Create a directory: "sudo mkdir/home/shared" 

<img width="341" height="121" alt="image" src="https://github.com/user-attachments/assets/1205bb47-c66b-4cb0-83bd-1651fa91ad93" />

Create ten files inside the directory file1 to file10 with the "sudo touch file1" command 

<img width="335" height="163" alt="image" src="https://github.com/user-attachments/assets/27868bf8-d139-4515-bf6b-1f86af5d7c83" />


Adding alice and bob into the group "sudo usermod -aG sharedgroup alice"

Changing the group ownership with "sudo chgrp -R sharedgroup/ home/shared". The sudo chgrp -R sharedgroup /home/shared command changes the group ownership of the /home/shared directory—and everything inside it—to the sharedgroup group.

<img width="401" height="193" alt="image" src="https://github.com/user-attachments/assets/553a2fb4-1522-4c9c-bac3-c5c1d4d78c43" />

<img width="362" height="156" alt="image" src="https://github.com/user-attachments/assets/7e8959ec-32e4-4c8b-beb2-b2b40ce47c87" />

<img width="350" height="157" alt="image" src="https://github.com/user-attachments/assets/868269ed-256d-4ad7-8fb1-f96e98a62c23" />

