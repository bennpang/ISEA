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

I had to locate the directory of the file sharing in "/mnt/hgfs" and make some configurations. 
<img width="1111" height="673" alt="image" src="https://github.com/user-attachments/assets/d3ac437e-e421-48f1-9c69-94edf5822f0a" />

adding "user_allow_other" inside the "/etc/fuse.conf"

<img width="1546" height="696" alt="image" src="https://github.com/user-attachments/assets/8e78f8ad-a4a3-494f-a35c-20ded99102c6" />

I also had to configure the "/etc/fstab" which will automatically boot once the Virtual Machine start  
<img width="1440" height="691" alt="image" src="https://github.com/user-attachments/assets/687edc19-f476-4ea8-97bd-75094be53f23" />

After configurating and much troubleshooting with online resources, I was able to use my filesharing folder from my host to share with my VM

<img width="972" height="660" alt="image" src="https://github.com/user-attachments/assets/1e93c01b-d668-4eb9-ba84-948d2ce855d4" />

Archive Extracted Successfully
---
To extract the files, I used "bunzip2" and "tar -xvf" to extract the files 

<img width="406" height="203" alt="image" src="https://github.com/user-attachments/assets/57c0f738-8e0f-4547-b55b-7046455ebf22" />

File Listing of Extracted Directory
---
**Tree**

I had to first install tree using "apt install tree"

<img width="361" height="167" alt="image" src="https://github.com/user-attachments/assets/0c9819e0-855a-480b-8e62-39c43976a0ff" />

This allowed me to have the chance to explore tree command that shows me the directory hierachy

<img width="302" height="229" alt="image" src="https://github.com/user-attachments/assets/8de41e9e-3da2-48ca-a446-4f00859af7d3" />


**less**
I tried the less command 
<img width="404" height="342" alt="image" src="https://github.com/user-attachments/assets/743b18b5-73b9-480d-a08b-7eaa46167380" />
