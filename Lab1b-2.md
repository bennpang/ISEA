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

The File Ownership (root root). The first root is the User Owner. The second root is the Group Owner.Because the system administrator account (root) owns all 10 files (file1 through file10), your normal user account cannot modify, overwrite, or delete any of them right now

<img width="335" height="163" alt="image" src="https://github.com/user-attachments/assets/27868bf8-d139-4515-bf6b-1f86af5d7c83" />


Adding alice and bob into the group "sudo usermod -aG sharedgroup alice"

Changing the group ownership with "sudo chgrp -R sharedgroup/ home/shared". The sudo chgrp -R sharedgroup /home/shared command changes the group ownership of the /home/shared directory—and everything inside it—to the sharedgroup group.

<img width="401" height="193" alt="image" src="https://github.com/user-attachments/assets/553a2fb4-1522-4c9c-bac3-c5c1d4d78c43" />

The File Ownership (root sharedgroup )Every line has two side-by-side columns reading root sharedgroup. The first root is the User Owner.The second is the Group Owner. Therfore, root has full read and write power while sharedgroup and others have read-only access

<img width="362" height="156" alt="image" src="https://github.com/user-attachments/assets/7e8959ec-32e4-4c8b-beb2-b2b40ce47c87" />

After changing the directory permissions "sudo chmod 770 /home/shared" now both root and sharedgroup have full access while others are unable to have any access to the files.

<img width="355" height="169" alt="image" src="https://github.com/user-attachments/assets/67ef23a1-4954-48c4-8d35-dbe72b70bef0" />

During my troubleshoot and understanding of this command. I initally thought that it was because of the wrong command was given used and wrong user previliege. The "No such file or directory" error happens because the wildcard asterisk (*) is looking for individual files inside /home/shared, but that folder is completely empty right now. However there were files inside of the directory which got me thinking that I was using the wrong user. So i switched to bob and tried using sudo however bob was unable to use sudo command.  In Linux, if a folder contains no files, the shell cannot expand the * symbol, causing the command to fail. The Solution Instead of targeting the files inside the folder using the asterisk, target the directory itself and tell it to apply the rules recursively (-R). The reason the command failed even though files exist is due to how Linux permission restrictions interact with shell wildcards (*).When you typed sudo chmod 750 /home/shared/*, your shell tried to expand the * into a list of files before running sudo. Because your normal user account (ben) did not have read permissions on the folder at that exact millisecond, the shell was blocked from seeing inside to expand the asterisk, resulting in the "No such file or directory" error.
<img width="357" height="287" alt="image" src="https://github.com/user-attachments/assets/33064060-d512-4966-9050-2393d4a3e426" />


