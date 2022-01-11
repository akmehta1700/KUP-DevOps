# Day 2 Questions

**Q1. Features of Kernel?**

Ans:- A Kernel is the central component of an Operating System. 

The Kernel is also said to be the heart of the Operating System. 

It is responsible for managing all the 
(1)processes 
(2)memory files
(3) Device Managment
(4)Interrupt Handling
(5)I/O Communication

It acts as an interface (bridge) between the user-level application (software) and the hardware. Therefore, the communication between the software and the hardware is done via the Kernel.

**Q2. What things Kernel Manage?**

Ans:- It basically manages operations of memory and CPU Time.
Kernel first loads first into memory when an operating system is loaded and remains into memory
until operating system is shut down again. It is responsible for various tasks such as disk managment, and memory managment.
It decides which process should be allocated to processor to execute  and which process should be kept in main memory to execute.

**Q3. Difference b/w Linux, Unix, Windows?**

Ans:- **Linux**
    • Linux is open source and id developed by Linux community of developers.
    • Linux is free to use.
    • Monolithics Kernel is used.
    • Linux is used in wide varieties from desktop, servers, smartphones to mainframes.
    • Ex:- Ubuntu, Debian GNU

        **UNIX**
    • Unix was developed by AT&T Bell labs and is not open source.
    • Unix is licensed OS.
    • Unix is mostly on Servers, Workstations or Pcs.
    • Ex:- SunOS, Solaris

           **Windows**
    •  It is a proprietary software owned by Microsoft.
    •  It is Costly.
    •  Micro Kernel is used.
    •  It filename is case-insensitive
    • Windows can be easily hacked

 **Q4. What do you mean by Opensource?**

Ans:- Open Source Software is released through a specific kind of license that makes its source code legally available to end user. 
Software is considered open if:- 
    • Its is available in source code form without additional cost => User can View the code that comprises  the software  and make any kind of changes to it they want.
    •  The source code can be repurposed into other new software =>  anyone can take the source code and distribute their own program from it.

 **Q5. Explain the output of “ls -l ” command**

Ans:- ls – ls command is used to list all the files present in a particular directory and that directory is the current directory.

First you can see that its a file or a directory (d – directory, - file).
Next is the root user and group user.
And then is size of the file or directory.
Then date and time when the directory is modified.
And last name of file or directory. 

 **Q6. How to create multiple files with single command**

Ans:- You can use touch command for it followed by the file name.These file would be empty while creation.
=> touch file1 file2 file3

 **Ques. Where are unit files located?**

Ans. Unit files are stored in the /usr/lib/systemd directory and its subdirectories, while the /etc/systemd/ directory and its subdirectories contain symbolic links to the unit files necessary to the local configuration of this host.

 **Ques. Create a service file for nginx.**

Ans. 

Save this file as /lib/systemd/system/nginx.service


[Unit]
Description=The NGINX HTTP and reverse proxy server
After=syslog.target network-online.target remote-fs.target nss-lookup.target
Wants=network-online.target

[Service]
Type=forking
PIDFile=/run/nginx.pid
ExecStartPre=/usr/sbin/nginx -t
ExecStart=/usr/sbin/nginx
ExecReload=/usr/sbin/nginx -s reload
ExecStop=/bin/kill -s QUIT $MAINPID
PrivateTmp=true

[Install]
WantedBy=multi-user.target
