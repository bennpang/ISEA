This lab's objective was to install Docker as my preferred extra server as an additional server component and set up an Ubuntu environment using WSL2 on Windows.
Applications and services can operate in isolated environments thanks to Docker's configuration as a container platform.

First I installed WSL because the lab environment needed Ubuntu running on WSL2. WSL eliminates the need for a separate virtual machine by enabling Linux distributions to run natively on Windows.

<img width="767" height="460" alt="Screenshot 2026-07-14 053317" src="https://github.com/user-attachments/assets/cdb57ea2-b29b-48a8-9281-9965aa95654f" />

The uname -a command process that I am on a Windows operating system and display the name and other system details

Before installing more sophisticated software like Docker, databases, or third-party repositories on a Debian-based Linux system (such as Ubuntu), this command installs five fundamental utilities.

<img width="862" height="222" alt="Screenshot 2026-07-14 053339" src="https://github.com/user-attachments/assets/bb07b55a-8ab6-4a1b-84cc-e22c8eaa2c70" />

After updating the system, I was able to install Docker on WSL2

<img width="848" height="314" alt="Screenshot 2026-07-14 053423" src="https://github.com/user-attachments/assets/746188c4-4fcf-45c4-ab35-99f3404fb09a" />

Here is me testing that Docker was working fine

<img width="622" height="325" alt="Screenshot 2026-07-14 053439" src="https://github.com/user-attachments/assets/18ea9425-45be-43ca-839e-07fbdefb9f61" />

made docker usable without sudo command by using the command "sudo usermod -aG docker benp"

<img width="569" height="315" alt="image" src="https://github.com/user-attachments/assets/8dc767e3-fd2c-4c10-84a0-1de10003c1ec" />
