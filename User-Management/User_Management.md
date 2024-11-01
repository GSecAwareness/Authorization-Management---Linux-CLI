#### This section will concentrate on basic user managment in the Linux CLI. In this scenario, a new employee joins our organization. Add them to the system and continue to manage their access.
***Step 1***  

*Add the new user to the system and assign their primary group.*     

![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/User-Management/1.PNG)  

*This next command will assign their primary group*  

![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/User-Management/2.PNG)  

---
***Step 2***

*Make this employee the owner of a file related to a particular object.*

![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/User-Management/3.PNG)

---

***Step 3***

*Add the new employee to a supplementary group.*   
**usermod -a -G** *sales_team researcher9: -a* is used alongside -G in this command to add a group to the desired list. Without the addtion of -a, the -G *sales_team* would replace the current group instead of adding it. 

![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/User-Management/4.PNG)  

---

***Step 4***  

*Delete the new employee from the system.*  

![get-content](https://github.com/GSecAwareness/Authorization-Management---Linux-CLI/blob/main/User-Management/5.PNG)   


*When a user is created in Linux, a group with the same name is automatically created and the user is the only member of that group. When removing users, the group must be removed as well.*  

**sudo userdel researcher9**: deletes the user and triggers a warning about the user group researcher9  
**sudo groupdel researcher9**: deletes the user group researcher9  

---


  
