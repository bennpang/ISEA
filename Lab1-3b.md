This lab trains students in using command-line tools to locate, inspect, and search through text files, especially within large archives. It builds essential skills in system administration and file forensics using Linux.

Enable FileShare
---
Firstly, in order to access file easily betweeen my Host and Virtual Machine I decided to Enable Filesharing.

We will first have to change the settings to enable fileshare "Right-CLick under settings"

<img width="281" height="350" alt="image" src="https://github.com/user-attachments/assets/5777b653-ecb2-4a44-8656-64f7405d66f5" />

Under Virtual Machine Settings Options I will nagavitage to share folders and always enable folder sharing in this instance i have a path "\Desktop\student_ISEA"

<img width="561" height="335" alt="image" src="https://github.com/user-attachments/assets/40ca9c36-6312-4cad-b0e8-cd3fd4aaa19c" />

Since Filesharing has been enable in the VMware Workstation I will have to mount it onto my Ubuntu system. "ls /mnt/hgfs"
From here, my file is accessible. However, nagivitating to this directory can be a hassle and I would like to move it somewhere for convienent like my Desktop. "ln -s/mnt/hfgs/student_ISEA ~/Desktop/student_ISEA" 

<img width="811" height="121" alt="image" src="https://github.com/user-attachments/assets/c2cada8f-412f-4a81-8ded-96bef0ae05dc" />

After restarting my Virtual Machine my shortcut to my shared folder has some issues. This was because it wasnt mounted permanently.

<img width="1033" height="657" alt="image" src="https://github.com/user-attachments/assets/48fa98be-de30-43d5-8697-1fba6ac1e5b3" />

<img width="1111" height="673" alt="image" src="https://github.com/user-attachments/assets/d3ac437e-e421-48f1-9c69-94edf5822f0a" />
