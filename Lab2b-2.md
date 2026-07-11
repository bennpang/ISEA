This lab introduces students to basic Bash scripting and automating system tasks on Linux. Activities include filesystem commands, creating scripts, using loops and conditionals, and automating system monitoring tasks.

Directory and File Operations Completed
---

Firstly, I created a new directory called LabFiles inside my current working directory "/Documents". I then start to navigate by changing the directory with the "cd" command under LabFiles "/Documents/LabFiles". Next I created a new textfile and called contents into the file. I then displayed the information using concatenate to dump all the the text writhen onto the command line interface. I then copy the notes and created a backup. I then renamed the file with the "mv" command and changed the filename into "old_notes.txt". Following that i decided to rm the file.

<img width="446" height="226" alt="image" src="https://github.com/user-attachments/assets/3461cc18-e385-4458-864d-386a487577dc" />

Reflection Questions
---
I can create a new directory with the "mkdir" command and I view the contents of a file with the "cat" command which dumps everything onto the command line interface. The difference between the commands "cp" and "mv" is that copy creates a new file with the same content as the copied file but move replaces the existing file and transfers all content into the file without retaining any information inside the exisiting file.

Basic Bash Script Created and Run
---

<img width="370" height="265" alt="image" src="https://github.com/user-attachments/assets/51472320-9811-4168-8148-8c2e06f73f6b" />

<img width="421" height="263" alt="image" src="https://github.com/user-attachments/assets/332c9844-fb68-4b84-885b-5c645500199e" />

<img width="328" height="104" alt="image" src="https://github.com/user-attachments/assets/075efe7b-7813-425f-aff2-8ee12dca1dd7" />

Reflection Questions
---
A text file can become a runnable program instead of a read-only document by using the chmod +x command. The shebang (#!/bin/bash) at the top instructs the operating system's kernel to interpret and execute the following instructions using the particular Bash interpreter route. Use the read command to ask the user for input, store their answer in a variable, and then use echo "Hello, $variable_name!" to edit a script for personalized messaging.

Loop and Conditional Script
---
I created a second Bash script that used the "read" command to take user input. Additionally, the script displayed various messages based on user input using if, elif, and else commands. This was followed by a for loop that numbered from 1 to 5.

An image of the Bash script
<img width="512" height="342" alt="image" src="https://github.com/user-attachments/assets/c4fc767f-bed7-4cc7-a19c-69bd616b0b1f" />

Reflection Questions
---
The for loop iterates through the numbers 1 to 5 using the sequence {1..5}. During each count, it prints the current iteration number and then pauses for 1 second using the sleep 1s command before continuing to the next number.
If a user enters a number greater than 10 then program will print "Number out of range"

To ensure that the user is prompted repeatedly until they provide a valid numeric value inside the desired range, place the input prompt inside a while loop. By enabling users to edit their input without restarting the script, this improves user experience.

System Monitoring Script Created and Run
---

<img width="414" height="293" alt="image" src="https://github.com/user-attachments/assets/610f1a94-81f7-40f1-a287-db0487d9acae" />


<img width="402" height="265" alt="image" src="https://github.com/user-attachments/assets/6f9c747c-5e2d-404b-a280-69da5ad55cc2" />





