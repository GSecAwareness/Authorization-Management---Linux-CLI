#### The purpose of this lab is to show basic permission modifications in Linux CLI. In this scenario, a security professional works at an organization with the research team. The professional is tasked with ensuring that users are authorized with appropriate permissions to harden the system.  

***Step 1***  

*Check the permissions for files and subdirectories in the projects directory. Display all permissions, including hidden files.*     

![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/1%20permissions.PNG)  


The command is:  
**ls –la**  

This command (**ls**) lists all the files and subdirectories in the current working directory. The next portion (**-la**) lists the permissions of all the files, including the hidden files and subdirectories.   
The format of permissions is **rwxrwxrwx** in the order of user, group, and other. The first three (**rwx**) show that the user of the file has read, write, and execute privleges. In this specific example, the group and other also have read, write, and execute privleges. Looking at *project_m.txt*, the permissions are quite different. They are **–rw-r-----**, meaning the following:  
user: read and write  
group: read  
execute: none  

***Step 2***  

*Assume that the organization does not allow other to have write access to any files. Look at the permissions and make the appropriate changes.*  

![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/2%20permissions.PNG)

The command to use is **chmod**, meaning change mode.   
**o-w**: other, remove write access   
*project_k.txt*: this was the only file in other that had write privleges  

***Step 3***  

*The research team has archived .project_x.txt, which is why it’s a hidden file. This file should not have write permissions for anyone, but the user and group should be able to read the file. Use a command to assign .project_x.txt the appropriate authorization.*   

![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/3%20permissions.PNG)  

**Chmod**: starts the command to change the file permissions  
**u-w,g-w,g+r**: user remove write permissions, group remove write permissions, group add read permissions  
**ls –l** *.project_x.txt*: list the permissions of the hidden file project_x.txt (after we modified permissions)  

***Step 4***  

**Chmod**: starts the command to change the folder permissions  
**g-x**: removes executable permissions from group, leaving only user with access to the Drafts folder  
**ls-la**: lists the permissions of all files and folders after our modification of Drafts folder  

 This lab demonstrated basic Linux skills to change permissions on files and subdirectories to ensure proper authorization for the research team. 




