This lab introduces Bash scripting for creating file backups, scheduling them using cron jobs, and exporting them to the cloud. Students will use scripting logic to automate folder archiving, apply timestamps to filenames, and securely upload backups to remote servers.

Created a Files and Directory inside of Documents

<img width="266" height="88" alt="image" src="https://github.com/user-attachments/assets/7b7a4924-c958-4534-8137-014a3d927cec" />


Made a script to move Documents to backup and zip then instead my home directory

<img width="301" height="266" alt="Screenshot 2026-07-13 230422" src="https://github.com/user-attachments/assets/64295e00-512d-4d10-b53d-069b459647ea" />


Move script to usr/bin

<img width="400" height="13" alt="image" src="https://github.com/user-attachments/assets/71257ec8-08fa-4811-81b1-91649c8ddd6a" />

Cronjob

I have editted the crontab file to allow it to run

<img width="455" height="301" alt="image" src="https://github.com/user-attachments/assets/d43b6735-4d3d-40d7-9e45-b540230bdfa8" />

Proof that cronjob was active and running 

<img width="452" height="215" alt="image" src="https://github.com/user-attachments/assets/e135d7ae-d65f-4907-8b6e-21635f9f3ead" />

Managed to scp

<img width="467" height="69" alt="image" src="https://github.com/user-attachments/assets/445c897e-2850-4f16-9897-f2257c883024" />


Proof that the file was received by Cloud instance

<img width="173" height="67" alt="image" src="https://github.com/user-attachments/assets/7944f7ab-2c6d-45ec-a5bb-2ba82aabcb7a" />


Challenge1
---
I configured it! 

<img width="466" height="371" alt="image" src="https://github.com/user-attachments/assets/ccc119f6-0d39-4320-bd65-66b7663b5dbb" />


Challenge 2
---
Created a script

<img width="380" height="146" alt="image" src="https://github.com/user-attachments/assets/23ea5b90-976f-4410-a377-ec2152facd51" />


Set it for all users

<img width="358" height="32" alt="image" src="https://github.com/user-attachments/assets/68a62807-70a3-45e2-a258-fecbf6796a5a" />

It Works!

<img width="327" height="158" alt="image" src="https://github.com/user-attachments/assets/dd05b72d-2b4b-4033-bda1-ba0b39ad6c53" />


Reflection Question:
---
Why is using absolute paths important in scripts run by cron?
This is because since cron jobs are automated, they execute jobs within a highly restricted and minimal enviroment that lacks configuration therefore stating the absolute paths is important so that it there is a protection against security vulnerabilites.

•	- What are the benefits of cloud exporting for backups?
Disaster Recovery Security Cost Effictivenes and Accessibility

•	- How does cron differ from manual execution?
Cron automates and makes it simpler compared to multiple manual executions.

•	- What happens if SSH keys are not accepted ahead of time?
Based on my experience during the lab exercise the prompt will usually hang and not display anything. However i would have to manually type the key to enable the ssh connection.

•	- How can login messages help improve user/system engagement?
It give the user a more unique and much not so boring interface as well as to give the user customization in my example i was able to give a login welcome to the user and specify the account when logging into the terminal


