#**Day2**

**Q1. What is Absolute path and relative path?**
Ans:- Absolute path: It is defined as specifying the location of a file or directory from the root directory (/). It is a complete path of a file from the start.            E.g., cat /home/sub-dir/file1.txt
       
       Relative path:- It is a path related to the present working directory. It starts with the current directory and not the root directory. E.g., 
       cat Desktop/Testfile1
       
   **Q2. What are hard and soft links?**
   Ans:- Hard links:- Files that are hard linked take the same inode number.
                      It cannot be used across file systems.
                      If the original file is removed, the link will still work as it accesses the data the original was having access to.
                      
         Soft links:- Files that are soft linked take a different inode number.
                      It can be used across file systems.
                      If the original file is removed, the link will not work as it doesn’t access the original file’s data.
                      
  **Q3. What does /srv contains and why is it empty?**
  Ans:- srv is where certain service files are kept.This directory gives users the location of data files for a particular service, such as FTP, WWW, or CVS. Data that only pertains to a specific user should go in the /home/ directory. srv is empty sometimes as the system might not be hosting any server at that moment.
  
  **Q4.How does cgroups differ from namespaces?**
  Ans:- cgroups, which stands for control groups, are a kernel mechanism for limiting and measuring the total resources used by a group of processes running on a system. For example, you can apply CPU, memory,network or IO quotas. 
  
  Namespaces are a kernel mechanism for limiting the visibility that a group of processes has of the rest of a system. For example you can limit visibility to certain process trees, network interfaces, user IDs or filesystem mounts.
  
  **Q5. In vim how can we search inside a file?**
  Ans:- In vim by pressing escape and getting into the command mode then pressing / and then typing the pattern/word that we want to search the cursor move to it.
  
  **Q6. In vim how can we search inside a file?**
  Ans:- By opening a file and pressing escape and getting into the command mode, :!rm
  
  **Q7.Difference between wq and x?**
  Ans:- The :wq command is used in vim to write and quit.
        If you :x a file in which no changes have been made, the modification time will be untouched because the file isn’t re-saved.
        
   **Q8. What are hidden files?**
   Ans:- Hidden files in Linux are the files that are not listed when the user runs ls command.Files are hidden in Linux as to make sure that users don’t accidentally modify the contents of these files or accidentaly delete these files. Or files could be hidden for privacy issues.
   To hide a file, we prepend a dot to its name.

Thus, we can create a hidden file named .hidden.sh using touch:
$ touch .hidden.sh

**Q9. How to identify which type file it is?**
Ans:- We can identify a type of file by the colour of the files which are as follow:-
Blue:- Directory
Green:- Executable or recognized data file
Cyan:- (Sky Blue) Symbolic link file
yellow with black background:- Device
Magenta:- (Pink) Graphic image file
Red:- Archive file
Red with black background:- Broken
