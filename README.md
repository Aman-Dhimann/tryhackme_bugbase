# tryhackme_bugbase
tryhackme reports
    Vulneversity tryhackme room
 


 





 
Successful tunnelling between the machine and kali


 
Performing aggressive scan on the machine to find out ports and web hosting port



 
Finding out squid


 




 
Some directories like /images seemed interesting but /internal turned out to be the one
 
Using gobuster to findout directories


 

 






 we need to pick up a code that would act as a reverse shell in


 
Since php is not working we can check which extension would be used to upload the reverse shell code


 
.phtml seems to be allowed


 
.phtml worked



 
We got a reverse shell from clicking the .phtml file


 



 
Checking various directories we found out that home/bill does have the root

 

By using ls -l and  
find / -perm -u=s -type f 2>/dev/null
we found out that systemctl stands odd one out so we should exploit it




 

Finally using the help of gtfobins we found out commands to give us root access by exploiting systemctl









 


