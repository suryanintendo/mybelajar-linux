# 5 File Contents and Comparing

- [x] 1. Creating a New User  
- [ ] 2. Creating a User with a Home Directory  
- [ ] 3. Setting a User Password  
- [ ] 4. Modifying User Properties  
- [ ] 5. Changing User Shell  
- [ ] 6. Adding a User to a Group  
- [ ] 7. Locking and Unlocking User Accounts 
- [ ] 8. Deleting a User  


 Pada praktikum kali ini akan di pandu untuk mempelajari 'dasar manajemen akun pengguna' di sistem lilux. Anda akan belajar membuat, mengubah dan menghapus user akun, serta mengatur dan mengubah katasandi. Ini adalah ketrampilan dasar untuk sistem administrasi linux.
 
 
 - [x] 1. Creating a New User (membuat user baru)
    Let's start by creating a new user account named "joker".  membuat user dengan nama "joker"
```
sudo useradd joker
```

  - [x] Changing User Shell
sudo usermod -s /bin/bash joker

  - [ ]   Summary
Congratulations! You've completed the Linux User Account Management lab. You've learned how to:

Create new user accounts
Set user passwords
Modify user properties like home directory and default shell
Add users to groups
Lock and unlock user accounts
Delete user accounts
You've also been introduced to important Linux concepts like the /etc/passwd file, home directories, shells, and user groups. These are fundamental skills for Linux system administration. Remember, in real-world scenarios, always follow your organization's security policies when managing user accounts
