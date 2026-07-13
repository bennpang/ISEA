In this lab i had to use the snap to install certbot

I have already install certbot using snap 

<img width="306" height="251" alt="image" src="https://github.com/user-attachments/assets/7d444192-cc2f-4132-aa94-442d019e88c4" />

I tried to install certbot to configure with apache server

<img width="281" height="34" alt="image" src="https://github.com/user-attachments/assets/fdcca7e2-7e97-44ae-8f2b-b72e2430e5a3" />

Because previously in Lab 3A -1 I installed and configured Certbot with my nginx web server I did not know that i was still using the apt installation of certbot
with this command I was able to confirm that i was still using the apt.

<img width="269" height="21" alt="image" src="https://github.com/user-attachments/assets/c7262b5a-a220-4cfb-a8b5-60c5c64ee157" />

With this command apache2ctl -S i was able to check that I was only running HTTP on this website

<img width="313" height="110" alt="image" src="https://github.com/user-attachments/assets/8d0fcb30-a9eb-4d0a-9a29-72d7efb09e09" />

I had to manually set Certbot to get the certificate only 

<img width="311" height="91" alt="image" src="https://github.com/user-attachments/assets/b1b403d5-6086-4fe4-b57b-2fd3cb53e5ae" />

Since I had use this website for the previous Lab 3-1A , I decided to renew and replace to get another certificate

<img width="310" height="155" alt="image" src="https://github.com/user-attachments/assets/3e987a12-da55-4788-bc43-409f4967220c" />

After changing the configurations, I thought by just reloading the server I was able to view the website using HTTP. However I did not restart the apache server which result in a error.

<img width="308" height="119" alt="image" src="https://github.com/user-attachments/assets/26a5857c-99eb-434b-96db-cdee2a3f4163" />

After restarting and checking that the server is running and active

<img width="308" height="167" alt="image" src="https://github.com/user-attachments/assets/21990ae7-4d85-4018-be00-0a8e5a961fdf" />

I initatly thought that everything was running smoothly and i was able to view the HTTPS website. However, the error of not securing the website still presented itself to me.

<img width="313" height="157" alt="image" src="https://github.com/user-attachments/assets/d135f0ad-6153-4134-8a20-920de517ebea" />

Hence, I did some researching online and I realised that I did not configure the SSL properly.

<img width="312" height="104" alt="image" src="https://github.com/user-attachments/assets/dc9cae11-b5a7-47ab-a104-8f0b8919eace" />

Therefore I went to check out the configuations of the website and determined that SSL was not configured.

<img width="312" height="83" alt="image" src="https://github.com/user-attachments/assets/f8d11d0b-b946-4ddf-ac69-a1d3fa46b79f" />

<img width="309" height="61" alt="image" src="https://github.com/user-attachments/assets/750c14f6-b885-4576-8cc4-1374f155e3d7" />




