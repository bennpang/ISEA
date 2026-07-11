This lab expands students’ understanding of Linux as a service host. Students will configure Apache, SSH, network settings, firewall rules, user accounts, and use compression tools for transferring files. The activities are collaborative and test basic system administration capabilities

**Apache**
---
Initially, I had to use "sudo apt install apeche2" to get Apeche before testing it on my browser at http://127.0.0.1.

Here are pictures of me testing and downloading it. Everything was operating smoothly!

<img width="479" height="230" alt="Screenshot 2026-07-11 082829" src="https://github.com/user-attachments/assets/a6602541-c275-41db-a49f-bfba35b7c841" />

Default webpage of Apache WebServer

<img width="431" height="356" alt="image" src="https://github.com/user-attachments/assets/a732305e-12e9-4589-93ae-23606d829e78" />

**Modified index.html page**

I personalising my webserver with a code that i found online by editing the file with "nano /var/www/html/index.html"


<img width="450" height="377" alt="image" src="https://github.com/user-attachments/assets/4fb75266-a910-4085-bd68-380da24058c1" />

<img width="452" height="409" alt="image" src="https://github.com/user-attachments/assets/8bdc9cf8-cbc3-4d52-88df-9ede6571967d" />

<img width="458" height="341" alt="image" src="https://github.com/user-attachments/assets/6262d51c-c8ba-424c-b463-a463799111b9" />

**NMAP**
---
Running the command "sudo apt install nmap" to install nmap onto ubuntu

<img width="434" height="150" alt="image" src="https://github.com/user-attachments/assets/4d813a83-e202-498a-a754-cd8c79e2ebf6" />

Doing an nmap scan to check for open ports on my Ubuntu Virtual Machine with the command "nmap 192.168.1.242"

Showing the Local IP address & Loopback address with the command "ip a"

<img width="416" height="256" alt="image" src="https://github.com/user-attachments/assets/87e4fbfc-cd22-4e4c-b4ef-58784329bff7" />

After removing apache2, port 80 was occupied by nginx. Hence, I had to stop nginx from listening to port 80

<img width="566" height="163" alt="image" src="https://github.com/user-attachments/assets/abf8fbdc-7546-4c4d-9781-7cff1b7bac4e" />

Firewall
---
I have enable and configured the firewall "sudo ufw status verbose" "sudo ufw enable" "sudo ufw allow port 80" 

<img width="302" height="157" alt="image" src="https://github.com/user-attachments/assets/dee7718b-05cd-4a3c-b1c5-e1fc54158442" />


SSH Enabled
---
I enabled Port 22 on the firewall which allows me to SSH into my Ubuntu with my Host OS "ssh 192.168.1.242"

<img width="509" height="244" alt="image" src="https://github.com/user-attachments/assets/60dc878f-4108-4cc7-a490-d7fe8a9ee147" />

SSH into the VM with the specific user "ssh pang@192.168.1.242"

<img width="524" height="276" alt="image" src="https://github.com/user-attachments/assets/153de8b1-16ec-42fe-ad28-f39fffdc9260" />

**Users**
---
After adding users with "sudo adduser pang" , I was able to check the number of users I have with "cat /etc/passwd" 
Which displays a complete list of all local user accounts configured on your Linux system.

<img width="575" height="650" alt="image" src="https://github.com/user-attachments/assets/aa190dbe-008f-457c-b40e-7b1340ba2eb3" />

**Downloading, Archiving, and Compressing Book Files Using Linux Commands**
---
I have gotten 3 books by using the "wget" command and stored 3 of the textfiles into a directory "mkdir Books" and create an archieve file from the directory Books with "tar cf books.tar Books" which I then compressed the file "bzip2 books.tar"

<img width="440" height="199" alt="image" src="https://github.com/user-attachments/assets/b8e75d6e-8cea-40d9-a3b1-651f8e5b74d2" />


Challenge
<img width="658" height="275" alt="image" src="https://github.com/user-attachments/assets/8546ffa7-81e7-4d82-8bd1-18ecc3fd7fe9" />


Challenge 2

<img width="626" height="290" alt="image" src="https://github.com/user-attachments/assets/99cda81a-0ee5-4e8f-9562-983638979bda" />

<img width="334" height="254" alt="image" src="https://github.com/user-attachments/assets/285bb173-ed98-4f27-a758-76250856f5df" />

<img width="340" height="249" alt="image" src="https://github.com/user-attachments/assets/41a952d7-0eac-48e1-93d7-f9df3dd3865d" />

Challenge 3

User1 to 192.168.1.242(ben)

<img width="377" height="244" alt="image" src="https://github.com/user-attachments/assets/5fb5e28c-9a73-4665-b6a0-0933e96e915e" />

192.168.1.242 to User 1 from user1 PC

<img width="349" height="161" alt="image" src="https://github.com/user-attachments/assets/ddb72dec-ead0-4329-b9a1-df387545af80" />

