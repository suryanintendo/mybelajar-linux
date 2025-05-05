# 1 Study Kasus.
Introduction  
In this challenge, you will apply your knowledge of Linux user account management. You'll create new user accounts, modify existing ones, and delete users. This challenge will test your understanding of the concepts learned in the "User Account Management" lab.  

Achievements  
You'll demonstrate your ability to use:  

useradd - to create new users  
passwd - to change user passwords  
usermod - to modify user accounts  
userdel - to delete user accounts  

>>  
>>  
Creating User Accounts
In this step, you'll create several user accounts with different specifications.

Tasks
Complete the following tasks in order:

Create a user named joker.
Create a user named batman with a home directory at /home/gotham.
Requirements
Use the useradd command for all user creations.
batman has a different home directory than the default.
Example
After completing these tasks, you can verify the user information like this:

sudo grep 'joker\|batman' /etc/passwd
 Explain Code
Sample output:

joker:x:5001:5001::/home/joker:/bin/sh
batman:x:5002:5002::/home/gotham:/bin/sh
 Explain Code
