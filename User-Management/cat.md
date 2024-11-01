#### This section focuses on Linux commands that assist users with file management and command information lookup. We will cover cat, whatis, and apropos.

***Step 1***  

*Use the **whatis** command to get a short description of **cat**. **whatis** provides a one-line summary of what a command does by retrieving a description from its manual (man) page.  This command is perfect for times when you know a command’s name but want a quick reminder of its purpose. It saves time compared to reading through a full man page. It’s often used when learning new commands or refreshing your memory about less frequently used ones.*     

![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/User-Management/6%20whatis.PNG)  

---
***Step 2***  

*Get more details about **cat** and what it does.*  

![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/User-Management/7%20man%20cat.PNG)  

*The **man** command displays manual pages or documentation for commands or programs. Each command has a corresponding manual page that provides detailed information, including usage and examples.    
There are four key sections of a man page:  
**NAME** section provides a brief description of the command.  
**SYNOPSIS** shows how to use the command, including the appropriate syntax.   
**DESCRIPTION** is a detailed explanation of the purpose.   
**EXAMPLES** gives practical exmpales of the command.*  

---  

***Step 3***  

*Use apropos to focus the search and find details on the first part of a file*  


![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/User-Management/8%20apropos.PNG) 

*The **apropos** command searches the manual pages for topics or commands related to the inputted string. It will find them when you cant remember the exact name but know the general funtionality. By using the **–a** parameter, it limits results to only those commands that match all keywords you inputted.*  

*There are other commands that help the security analyst to view data. For example, the head command shows (by default) the first 10 lines of a file. To do this, input the following:*  

**Head** myfile.txt: assuming this file is in your working directory, it will display the first 10 lines of the document  

**Head –n 5** myfile.txt: this will display the first 5 lines  

---

***Step 4***

*Use the appropriate command to get help on useradd and learn about  its options.*  

a.	Which option can be used with the useradd command to set an expiration date for a temporary account?  

**man useradd** shows detailed information about useradd. From this, **-e** is the best choice. 
**sudo useradd –e** 2024-10-31 newuser sets the expiration of newuser to 10-31-2024

*Use the appropriate command to determine the difference between rm and rmdir*  

a.	Which command removes empty directories?  
**rmdir** removes directories only is the directory is empty. If it has files in it, the command will fail.  

*What command would you use to find a command to  create a new group?*  

a.  **Apropros –a** create new group  searches for a command using the specific keywords create new group. The output is **groupadd**, which creates a new user group. **groupadd** lets the analyst manage permissions and create access control for the organization. 








