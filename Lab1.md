This lab focused on setting up a Linux environment using virtualization software. The objective was to successfully install and configure a virtual machine running Ubuntu Linux while gaining an understanding of virtualization basics, installation procedures, and network configuration.

The tools used included:

VMware Workstation (after initially attempting VirtualBox)

Ubuntu Desktop ISO

GitHub

Initially, I downloaded and installed VirtualBox to create an Ubuntu virtual machine. However, I was not familar in troubleshooting and navigation process within VirtualBox which took up alot of time and effort hence I decided to embark the rest of the journey with VMWare Workstation as I am more experienced with the software as I did boot up a handful of virtual machines with it during my Polytechnic days as a student in Computer Engineering.

<img width="440" height="289" alt="Screenshot 2026-07-04 155710" src="https://github.com/user-attachments/assets/f01d0eb0-bae1-42a0-a28d-8477f2fe4b1d" />

Firstly, installation of VMware Workstation. It is a powerful desktop virtualization application that allows you to run multiple, isolated operating systems (such as Windows, Linux, or BSD) simultaneously on a single physical PC.  It functions as a "Type 2 hypervisor," A type 2 hypervisor, or hosted hypervisor, interacts with the underlying host machine hardware through the host machine’s operating system. You install it on the machine, where it runs as an application.(AWS, n.d)

<img width="654" height="379" alt="image" src="https://github.com/user-attachments/assets/e118f17f-6463-4508-91bd-9ae2032f3792" /> (AWS, n.d)

**Downloads** 

<img width="400" height="565" alt="image" src="https://github.com/user-attachments/assets/89036726-713d-4317-8525-0c939d173ef6" />
<img width="394" height="510" alt="image" src="https://github.com/user-attachments/assets/4979b4a6-28a3-4291-820a-c1a0a0721dfa" />

**Verifying the intergrity of the ISO using SHA-256**

An ISO file, also known as an ISO image, is a single digital file that contains an exact, uncompressed copy of the contents of a physical optical disc, such as a CD, DVD, or Blu-ray (IONOS, 2022).

In this scenario, the Ubuntu ISO image will be used to create and run a virtual machine. Before using any downloaded software, it is considered best practice to verify the integrity of the file. This is done by comparing the SHA-256 hash value generated from the downloaded ISO with the official SHA-256 hash published on the Ubuntu website. If both hash values match, it confirms that the file has not been altered, corrupted, or tampered with during the download process.

SHA-256 (Secure Hash Algorithm 256-bit) is a widely used cryptographic hash function that converts data of any size into a unique 256-bit (32-byte) hash value. The resulting output is always represented as a 64-character hexadecimal string, regardless of the size of the original input (Deep, 2026).


<img width="2242" height="904" alt="image" src="https://github.com/user-attachments/assets/abfc2a89-b458-4978-9608-1fd35d9b72b0" />

**Virtual Machine Creation**

After launching VMware Workstation, crtl+N to create a new typical virtual machine inside the workstation.

<img width="637" height="625" alt="image" src="https://github.com/user-attachments/assets/ba57536a-a145-46bb-9169-8c93886b09a5" />

Depending on your host machine specifications, I am able to more allocate RAM and storage to my virtual machine without comprimising my own systems performance.

<img width="1141" height="1170" alt="image" src="https://github.com/user-attachments/assets/4ffa825a-263a-46fe-b07a-407f56b43ce2" />


<img width="2551" height="1518" alt="image" src="https://github.com/user-attachments/assets/8a2a0d65-e07a-4157-b206-b30f77a3cb73" />

**NAT vs Bridged** 

NAT's primary function is to enable virtual machines (VMs) to connect to external networks or the internet. When the virtual machine (VM) transmits traffic, VirtualBox converts its internal IP address into the host machine's IP address.(J, 2024)

<img width="411" height="279" alt="image" src="https://github.com/user-attachments/assets/4232b7ad-7a29-444b-bbee-c9b98fa90c2e" /> (J, 2024)

Bridged, enable the virtual machine (VM) functions on the network as a distinct, independent device.
Other devices on the same network can access this virtual machine because it is directly connected to the same network as your host computer. (J, 2024)

<img width="546" height="335" alt="image" src="https://github.com/user-attachments/assets/23ef5d47-41f7-4a1d-a03a-30c0447cd2f1" /> (J, 2024)

**Secure Shell Access **

To enable SSH (Secure Shell) into the virtual machine. I have to change the networking mode of the virtual machine into bridged mode in order to  give the VM an IP address.

A cryptographic network protocol called Secure Shell enables users to safely access, manage, and move files to distant devices over an unprotected network. It is the industry standard for safe remote server administration because it offers robust encryption and authentication. (Gillis, 2024)

I installed SSH into my Ubuntu Operating system
<img width="648" height="487" alt="image" src="https://github.com/user-attachments/assets/04a8cfc2-ae50-424a-8203-df97819d6504" />

Successfully SSH into my Ubuntu Virtual Machine

<img width="2068" height="1342" alt="image" src="https://github.com/user-attachments/assets/eebdfe98-ab92-4285-b80b-b209546d01b7" />

**Personal Reflection**

Even though I had experience working with virtual machines in the past, I found it difficult to start all over again while after being in National Service for 2 years and not using virtual machines. It was a challenging to setup most of the configuration and I had to google and look up at different website in order to refresh my memory of networking and linux commmands.

**LibreOffice**

I opened Firefox, and wanted to download an open source office productivity suite developed by The Document Foundation LibreOffice Writer to generate a document, I was able to familiarize myself with the Ubuntu graphical user interface as it was the same as Windows. However, I was faced by two options which is was unfamilar with RPM and DEB
<img width="911" height="545" alt="image" src="https://github.com/user-attachments/assets/66b4407a-8d88-4528-bb0e-2b5fdc53efdc" />

<img width="418" height="374" alt="image" src="https://github.com/user-attachments/assets/49c54125-b0b0-440a-829b-f94d02a21280" /> (DataFlair Team, n.d)

After I understood the difference between the two downloads I was able to choose DEB extention as I was installing it onto a Ubuntu System.

<img width="448" height="277" alt="image" src="https://github.com/user-attachments/assets/45e360ea-c00a-4f40-8f3b-fdca019966fd" />

In Windows, it was a click away from running the program, however I was unable to comprehend what was going on as it wasn't just a click to run the program. So I had look for the file inside of the directory and install the software from the command line interface (CLI).

<img width="1924" height="259" alt="image" src="https://github.com/user-attachments/assets/725a82f5-726e-4fc4-84f2-6e26db850465" />

<img width="1885" height="879" alt="image" src="https://github.com/user-attachments/assets/2826fb80-1df1-42d3-a97e-68718dd80faa" />




**Citations**

Deep, A. (2026) SHA-256 explained: Benefits and Applications, What is SHA-256? A practical guide to SHA-256 hashing. Available at: https://www.expressvpn.com/blog/what-is-sha-256/ (Accessed: 10 July 2026). 

IONOS (2022) What is an ISO file? definition and application of ISO files - IONOS, What is an ISO file? De­f­i­n­i­tion and functions. Available at: https://www.ionos.com/digitalguide/server/know-how/what-is-an-iso-file/ (Accessed: 10 July 2026). 

AWS (no date) What’s the Difference Between Type 1 and Type 2 Hypervisors? Available at: https://aws.amazon.com/ (Accessed: 10 July 2026).

Gillis, A.S. (2024) What is SSH (secure shell) and how does it work? | techtarget, https://www.techtarget.com/. Available at: https://www.techtarget.com/searchsecurity/definition/Secure-Shell (Accessed: 10 July 2026). 

J, B. (2024) Choosing the right virtualbox network adapter: Nat, host-only, or bridged? | by Bennison J | Dev Genius, Choosing the Right VirtualBox Network Adapter: NAT, Host-Only, or Bridged? Available at: https://blog.devgenius.io/choosing-the-right-virtualbox-network-adapter-nat-host-only-or-bridged-188003a260de?gi=e57eb801f265 (Accessed: 10 July 2026). 

Deb vs RPM - dataflair (no date) data-flair.training. Available at: https://data-flair.training/blogs/deb-vs-rpm/ (Accessed: 10 July 2026). 
