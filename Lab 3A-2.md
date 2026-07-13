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

I had to configure the SSL inside apache

<img width="309" height="61" alt="image" src="https://github.com/user-attachments/assets/750c14f6-b885-4576-8cc4-1374f155e3d7" />

Here is the configuration  (HTTPS)

<img width="320" height="165" alt="Screenshot 2026-07-13 173009" src="https://github.com/user-attachments/assets/58837bfd-2a30-4f9d-9d82-627484872788" />

Then I had to enable the module for SSL

<img width="216" height="26" alt="image" src="https://github.com/user-attachments/assets/e2060c05-c79c-4ebc-b3e5-6d6883a133ab" />

I was now able to verify the SSL files
<img width="316" height="34" alt="image" src="https://github.com/user-attachments/assets/ef9d7ab3-571e-4312-847e-72267df33c18" />

I was also able to verify the Services inside of apache2ctl

<img width="316" height="111" alt="image" src="https://github.com/user-attachments/assets/99e8c138-3707-430b-8110-d08cf20967a3" />

Then I decided to test the Apache Server

<img width="308" height="89" alt="image" src="https://github.com/user-attachments/assets/da54a80e-5477-4332-aed6-bf293f4b9e5a" />

For one last check I decided that Curl command was very useful as I was able to throw the entire page on my command line

<img width="304" height="85" alt="image" src="https://github.com/user-attachments/assets/8a5971c7-d1aa-4fb0-8357-50f94911a31b" />

To double confirm myself I decided to view the webpage in a browser.

<img width="641" height="260" alt="image" src="https://github.com/user-attachments/assets/36ea95a9-6462-483f-9d83-cc189c5e0db9" />

I was able to view that I had the certificate as well and was issues by LET'S ENCRYPT

<img width="404" height="449" alt="image" src="https://github.com/user-attachments/assets/a629cc03-1fe5-40b5-801e-c7eec3aa9671" />

Renewal of Certificate

<img width="360" height="160" alt="image" src="https://github.com/user-attachments/assets/bd9b6528-82ae-412d-a697-b117a751c3e6" />





