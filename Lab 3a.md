## Lab 3a
this is lab introduces students to setting up a complete Internet-facing web presence by configuring a cloud virtual machine (VM), purchasing and linking a domain name, setting up DNS records, and hosting a website on an Apache web server. Building on top of that, we will obtain and install a free TLS certificate from Let's Encrypt using Certbot to enable HTTPS on their website. I will verify the certificate installation, ensure secure communication between clients and the server, and gain practical experience in deploying and managing a publicly accessible, secure web service with full control over its infrastructure..

Creating AWS EC2 Instance
---
Using the AWS Management Console, I first created an Ubuntu EC2 instance. I created a security group during setup that was set up to permit SSH (Port 22), HTTP (Port 80), and HTTPS (Port 443) incoming traffic. These rules were required to allow users to access the web application via both HTTP and HTTPS, as well as to enable remote server administration.

<img width="590" height="403" alt="Screenshot 2026-07-11 152110" src="https://github.com/user-attachments/assets/540c7b45-6256-4c37-b6e8-8f47905be20e" />

I was then issued a private key by AWS which enable to have access to SSH.

<img width="433" height="429" alt="image" src="https://github.com/user-attachments/assets/dd8b5a38-07fe-42be-a8fb-adda5d79672c" />

Without this key I wasn't able to access SSH

<img width="317" height="65" alt="image" src="https://github.com/user-attachments/assets/8057db28-0861-4abc-a2b2-adfe45054e41" />


From this command "ssh -i /home/ben/Desktop/ubuntu.pem ubuntu@3.107.239.196"
It tells SSH to use the private key for authentication to connect to the server at IP address 3.107.239.196 as the user ubuntu, using the private key stored in ~/ubuntu.pem.

<img width="445" height="410" alt="Screenshot 2026-07-11 151536" src="https://github.com/user-attachments/assets/8dd946bd-cac5-45e0-a3df-4881daf7117c" />

Web Server
---
Next I had to install apache web server for hosting the website

<img width="414" height="131" alt="Screenshot 2026-07-11 151838" src="https://github.com/user-attachments/assets/e45c3f23-6189-4b6c-8667-d81a398e02f5" />

Enabling the server with "systmctl start apache2"

<img width="411" height="182" alt="Screenshot 2026-07-11 152010" src="https://github.com/user-attachments/assets/3e0f18fb-ddfd-45bf-89a2-dcdc2b1dd817" />

This was the default output of the website

<img width="682" height="434" alt="Screenshot 2026-07-11 152055" src="https://github.com/user-attachments/assets/45d78cbb-47f5-408f-b5b4-a29812561eda" />

<img width="415" height="308" alt="Screenshot 2026-07-11 152250" src="https://github.com/user-attachments/assets/99383c8e-6352-495e-a8bf-3df997c10a4c" />

I decided to make my website to unique by edited the "/var/www/html/html.index" file

<img width="349" height="98" alt="Screenshot 2026-07-11 153826" src="https://github.com/user-attachments/assets/f4036f53-8f95-40d3-b8d3-4e13d01038f7" />

<img width="441" height="404" alt="Screenshot 2026-07-11 155130" src="https://github.com/user-attachments/assets/3a22917b-c768-42a0-8e9a-b3a8882c11d7" />

This was the new website front page

<img width="614" height="436" alt="Screenshot 2026-07-11 155135" src="https://github.com/user-attachments/assets/686c42ee-3e9e-405c-8db5-473add63045d" />

<img width="439" height="409" alt="Screenshot 2026-07-11 160217" src="https://github.com/user-attachments/assets/75a1df2a-aca5-4cdf-a4c5-dbd0cf9bdb0e" />

<img width="439" height="191" alt="Screenshot 2026-07-11 160343" src="https://github.com/user-attachments/assets/33643cc0-d420-4b1e-ad4b-fee1ad77ccea" />


<img width="434" height="328" alt="Screenshot 2026-07-11 160143" src="https://github.com/user-attachments/assets/f1115482-7f23-4fbf-bda2-ea01420f87de" />


<img width="320" height="110" alt="Screenshot 2026-07-11 160602" src="https://github.com/user-attachments/assets/64faddbd-3371-4a59-86a8-d59ea6808853" />

<img width="630" height="458" alt="Screenshot 2026-07-11 160610" src="https://github.com/user-attachments/assets/62fc4819-71ee-4c89-906c-b2ff36fea16c" />

<img width="332" height="166" alt="Screenshot 2026-07-11 160847" src="https://github.com/user-attachments/assets/55887e23-5f9d-4036-98ce-9d3fa7548618" />

<img width="311" height="119" alt="Screenshot 2026-07-11 161851" src="https://github.com/user-attachments/assets/e2623b30-ffa5-4368-b8ad-542d9aa8e089" />

<img width="434" height="247" alt="Screenshot 2026-07-11 162509" src="https://github.com/user-attachments/assets/f4b74fb0-cdc5-417a-8854-dacda557d895" />

<img width="440" height="189" alt="Screenshot 2026-07-11 162557" src="https://github.com/user-attachments/assets/99a43122-b851-4fb5-81ae-7e74b5723d7c" />

<img width="423" height="212" alt="Screenshot 2026-07-11 162759" src="https://github.com/user-attachments/assets/ae5a93a8-438a-43dd-846a-ed32efa83883" />


<img width="431" height="175" alt="Screenshot 2026-07-11 162948" src="https://github.com/user-attachments/assets/689d39c3-7b7c-4300-980b-c5ab5047815f" />


<img width="424" height="261" alt="Screenshot 2026-07-11 163029" src="https://github.com/user-attachments/assets/292a8cf9-f61f-4117-9fa4-9536ea3befa7" />

<img width="355" height="203" alt="Screenshot 2026-07-11 163143" src="https://github.com/user-attachments/assets/662cb00c-73ec-45d3-90a9-03d49b3ca40d" />

<img width="374" height="148" alt="Screenshot 2026-07-11 163157" src="https://github.com/user-attachments/assets/ab965591-fff6-4702-8c5c-6ae8cb094782" />

<img width="510" height="401" alt="Screenshot 2026-07-11 163448" src="https://github.com/user-attachments/assets/5c976ef0-170b-4a2f-8041-87ba258538c5" />

<img width="400" height="430" alt="Screenshot 2026-07-11 163513" src="https://github.com/user-attachments/assets/44a6372a-76df-496a-8acb-0a35e9dc2579" />

<img width="308" height="137" alt="Screenshot 2026-07-11 163601" src="https://github.com/user-attachments/assets/fe3e1e69-bbe8-4e40-b845-8506033c3051" />

<img width="440" height="85" alt="Screenshot 2026-07-11 163804" src="https://github.com/user-attachments/assets/ba4a9358-e6a9-40e8-9b97-bf84f58a25de" />

<img width="306" height="188" alt="Screenshot 2026-07-11 163816" src="https://github.com/user-attachments/assets/ccbb3678-be45-4fbb-8bf6-8848973344ff" />


